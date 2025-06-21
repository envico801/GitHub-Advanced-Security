Code-scanning workflows that use CodeQL have various configuration options that you can adjust to better suit the needs of your organization.

In this unit, we review how to reference additional queries in a custom configuration file.

## Additional queries in a custom configuration file

A custom configuration file is an alternative way to specify additional packs and queries to run. You can also use the file to disable the default queries and to specify which directories to scan during analysis.

In the workflow file, use the `config-file` parameter of the `init` action to specify the path to the configuration file you want to use. This example loads the configuration file `./.github/codeql/codeql-config.yml`.

```
<span><span>- uses:</span> <span>github/codeql-action/init@v3</span>
<span>  with:</span>
<span>    config-file:</span> <span>./.github/codeql/codeql-config.yml</span>
</span>
```

The configuration file can be located within the repository you're analyzing or in an external repository. Using an external repository allows you to specify configuration options for multiple repositories in a single place. When you reference a configuration file located in an external repository, you can use the `OWNER/REPOSITORY/FILENAME@BRANCH` syntax. For example: `octo-org/shared/codeql-config.yml@main`.

If the configuration file is located in an external private repository, use the `external-repository-token` parameter of the `init` action to specify a token that has access to the private repository.

```
<span><span>- uses:</span> <span>github/codeql-action/init@v3</span>
<span>  with:</span>
<span>    external-repository-token:</span> <span>${{</span> <span>secrets.ACCESS_TOKEN</span> <span>}}</span>
</span>
```

The settings in the configuration file are written in YAML format.

### Specify CodeQL query packs in custom configuration files

Note

The CodeQL package-management functionality, including CodeQL packs, is currently in beta and subject to change.

You can specify CodeQL query packs in an array. The format is different from the format used by the workflow file.

```
<span><span>packs:</span>
<span>packs:</span>
  <span># Use the latest version of 'pack1' published by 'scope'</span>
<span>  -</span> <span>scope/pack1</span>
  <span># Use version 1.2.3 of 'pack2'</span>
<span>  -</span> <span>scope/pack2@1.2.3</span>
  <span># Use the latest version of 'pack3' compatible with 3.2.1</span>
<span>  -</span> <span>scope/pack3@~3.2.1</span>
  <span># Use pack4 and restrict it to queries found in the 'path/to/queries' directory</span>
<span>  -</span> <span>scope/pack4:path/to/queries</span>
  <span># Use pack5 and restrict it to the query 'path/to/single/query.ql'</span>
<span>  -</span> <span>scope/pack5:path/to/single/query.ql</span>
  <span># Use pack6 and restrict it to the query suite 'path/to/suite.qls'</span>
<span>  -</span> <span>scope/pack6:path/to/suite.qls</span>
</span>
```

The full format for specifying a query pack is `scope/name[@version][:path]`. Both `version` and `path` are optional. `version` is semver version range. If it's missing, the latest version is used.

If you have a workflow that generates more than one CodeQL database, you can specify any CodeQL query packs to run in a custom configuration file using a nested map of packs.

```
<span><span>packs:</span>
  <span># Use these packs for JavaScript and TypeScript analysis</span>
<span>  javascript:</span>
<span>    -</span> <span>scope/js-pack1</span>
<span>    -</span> <span>scope/js-pack2</span>
  <span># Use these packs for Java and Kotlin analysis</span>
<span>  java:</span>
<span>    -</span> <span>scope/java-pack1</span>
<span>    -</span> <span>scope/java-pack2@v1.0.0</span>
</span>
```

### Specify additional queries in a custom configuration

You can specify additional queries in a `queries` array. Each element of the array contains a `uses` parameter with a value that identifies a single query file, a directory containing query files, or a query suite definition file.

```
<span><span>queries:</span>
<span>  - uses:</span> <span>./my-basic-queries/example-query.ql</span>
<span>  - uses:</span> <span>./my-advanced-queries</span>
<span>  - uses:</span> <span>./query-suites/my-security-queries.qls</span>
</span>
```

Optionally, you can give each array element a name, as shown in the following example configuration file:

```
<span><span>name:</span> <span>"My CodeQL config"</span>

<span>disable-default-queries:</span> <span>true</span>

<span>queries:</span>
<span>  - name:</span> <span>Use</span> <span>an</span> <span>in-repository</span> <span>QL</span> <span>pack</span> <span>(run</span> <span>queries</span> <span>in</span> <span>the</span> <span>my-queries</span> <span>directory)</span>
<span>    uses:</span> <span>./my-queries</span>
<span>  - name:</span> <span>Use</span> <span>an</span> <span>external</span> <span>JavaScript</span> <span>QL</span> <span>pack</span> <span>(run</span> <span>queries</span> <span>from</span> <span>an</span> <span>external</span> <span>repo)</span>
<span>    uses:</span> <span>octo-org/javascript-qlpack@main</span>
<span>  - name:</span> <span>Use</span> <span>an</span> <span>external</span> <span>query</span> <span>(run</span> <span>a</span> <span>single</span> <span>query</span> <span>from</span> <span>an</span> <span>external</span> <span>QL</span> <span>pack)</span>
<span>    uses:</span> <span>octo-org/python-qlpack/show_ifs.ql@main</span>
<span>  - name:</span> <span>Use</span> <span>a</span> <span>query</span> <span>suite</span> <span>file</span> <span>(run</span> <span>queries</span> <span>from</span> <span>a</span> <span>query</span> <span>suite</span> <span>in</span> <span>this</span> <span>repo)</span>
<span>    uses:</span> <span>./codeql-qlpacks/complex-python-qlpack/rootAndBar.qls</span>

<span>paths:</span>
<span>  -</span> <span>src</span>
<span>paths-ignore:</span>
<span>  -</span> <span>src/node_modules</span>
<span>  -</span> <span>'**/*.test.js'</span>
</span>
```

## Disable the default queries

If you only want to run custom queries, you can disable the default security queries by using `disable-default-queries: true`. You should also use this flag if you're trying to construct a custom query suite that excludes a particular rule. This avoids having all of the queries run twice.

## Excluding specific queries from analysis

You can add `exclude` and `include` filters to your custom configuration file, to specify the queries you want to exclude or include in the analysis, such as:

-   Specific queries from the default suites (`security`, `security-extended` and `security-and-quality`).
-   Specific queries whose results don't interest you.
-   All the queries that generate warnings and recommendations.

You can use `exclude` filters similar to those in the configuration the following file to exclude queries that you want to remove from the default analysis. In the example of a configuration file that follows, both the `js/redundant-assignment` and the `js/useless-assignment-to-local` queries are excluded from analysis.

```
<span><span>query-filters:</span>
<span>  - exclude:</span>
<span>      id:</span> <span>js/redundant-assignment</span>
<span>  - exclude:</span>
<span>      id:</span> <span>js/useless-assignment-to-local</span>
</span>
```

To find the ID of a query, you can click the alert in the list of alerts in the Security tab. This opens the alert details page. The Rule ID field contains the query ID.

Things to keep in mind when working with the `excludes` filter:

-   The order of the filters is important. The first filter instruction that appears after the instructions about the queries and query packs determines whether the queries are included or excluded by default.
-   Subsequent instructions are executed in order and the instructions that appear later in the file take precedence over the earlier instructions.

## Specify directories to scan

For the interpreted languages that CodeQL supports (Python, Ruby and JavaScript/TypeScript), you can restrict code scanning to files in specific directories by adding a `paths` array to the configuration file. You can exclude the files in specific directories from analysis by adding a `paths-ignore` array.

```
<span><span>paths:</span>
<span>  -</span> <span>src</span>
<span>paths-ignore:</span>
<span>  -</span> <span>src/node_modules</span>
<span>  -</span> <span>'**/*.test.js'</span>
</span>
```

Note

-   The `paths` and `paths-ignore` keywords, used in the context of the code scanning configuration file, shouldn't be confused with the same keywords when used for `on.<push|pull_request>.paths` in a workflow. When they're used to modify `on.<push|pull_request>` in a workflow, they determine whether the actions will be run when someone modifies code in the specified directories.
-   The filter pattern characters `?`, `+`, `[`, `]`, and `!` aren't supported and will be matched literally.
-   `**` characters can only be at the start or end of a line, or surrounded by slashes, and you can't mix `**` and other characters. For example: `foo/**`, `**/foo`, and `foo/**/bar` are all allowed syntax, but `**foo` isn't. However, you can use single stars along with other characters, as shown in the example. You'll need to quote anything that contains a `*` character.

For compiled languages, if you want to limit code scanning to specific directories in your project, you must specify appropriate build steps in the workflow. The commands you need to use to exclude a directory from the build will depend on your build system.

You can quickly analyze small portions of a monorepo when you modify code in specific directories. You'll need to both exclude directories in your build steps and use the `paths-ignore` and `paths` keywords for `on.<push|pull_request>` in your workflow.