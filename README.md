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

### [Preview publish package](./github/workflows/preview-publish-package.yml)

> [!NOTE]
> This section covers `preview-publish-package*` workflows

Designed to automate the process of building and publishing a preview version of a exile.watch package to a github npm registry, enabling users to test and evaluate changes before the final release. 

|                                         Workflow code                                          | Name                             | Responsibility                                                                                            |
|:----------------------------------------------------------------------------------------------:|----------------------------------|-----------------------------------------------------------------------------------------------------------|
|      [`CI-00`](./.github/workflows/preview-publish-package-00-create-status-comment.yml)       | Create status comment            | Creates status comment after `preview-publish` label is applied to the branch                             |
|        [`CI-01`](./.github/workflows/preview-publish-package-01-publish-prerelease.yml)        | Publish prerelease               | Creates prerelease in `x.x.x-preview.x` format and publishes to github registry                           |
| [`CI-02`](./.github/workflows/preview-publish-package-02-update-status-comment-on-success.yml) | Update status comment on success | Once the package is published, this workflow updates the status created in `CI-00`                        |
| [`CI-03`](./.github/workflows/preview-publish-package-03-update-status-comment-on-failure.yml) | Update status comment on failure | If any step from `Publish prerelease` workflow fails, this workflow updates the status created in `CI-00` |
|   [`CI-04`](./.github/workflows/preview-publish-package-04-remove-preview-publish-label.yml)   | Remove preview publish label     | Removes `preview-publish` label from PR once `CI-00` is completed                                         |

## Contributing
| Area                                              | Link                                                                                            |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Want to contribute?                               | [Check the docs](https://docs.exile.watch/projects/splinters/contributing)                      |
| Encountered a bug?                                | [Check issues or create a new one](https://github.com/exile-watch/hideout/issues)               |
| Have an idea for a new feature?                   | [Check the discussions or create a new one](https://github.com/exile-watch/hideout/discussions) |
| Anything else is on your mind?                    | [Head over to exile.watch's hideout](https://github.com/exile-watch/hideout)                    |
| Curious about exile.watch architecture decisions? | [Read exile.watch engineering blog](https://engineering.exile.watch/)                           | 