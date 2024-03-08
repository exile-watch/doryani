<p align="center">
  <a href="https://exile.watch">
    <img alt="exile.watch logo" src="https://avatars.githubusercontent.com/u/158840748?s=400&u=4c73ba2a9a2ebc70b01c6303d41e8571df84ec37&v=4" width="300" />
  </a>
</p>
<h1 align="center">
  <a href="#">exile.watch</a> github actions workflows
</h1>
<p align="center">
    Collection of automation processes
</p>

## Workflows

### Preview publish package

> [!NOTE]
> This section covers `preview-publish-package*` workflows

Designed to automate the process of building and publishing a preview version of a exile.watch package to a github npm registry, enabling users to test and evaluate changes before the final release. 

| Workflow code | Name                             | Responsibility                                                                                            |
|---------------|----------------------------------|-----------------------------------------------------------------------------------------------------------|
| `CI-00`       | Create status comment            | Creates status comment after `preview-publish` label is applied to the branch                             |
| `CI-01`       | Publish prerelease               | Creates prerelease in `x.x.x-preview.x` format and publishes to github registry                           |
| `CI-02`       | Update status comment on success | Once the package is published, this workflow updates the status created in `CI-00`                        |
| `CI-03`       | Update status comment on failure | If any step from `Publish prerelease` workflow fails, this workflow updates the status created in `CI-00` |
| `CI-04`       | Remove preview publish label     | Removes `preview-publish` label from PR once `CI-00` is completed                                         |

- [Preview publish package]()
### Contributing
Want to contribute? [Check the docs](https://docs.exile.watch/projects/splinters/contributing)

Encountered a [bug](https://github.com/exile-watch/hideout/issues) or have a [question](https://github.com/exile-watch/hideout/discussions)?

Have an idea for a new [feature](https://github.com/exile-watch/hideout/discussions/categories/ideas)?

Head over to exile.watch's [hideout](https://github.com/exile-watch/hideout)!