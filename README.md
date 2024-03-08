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

### [Preview publish package](./preview-publish-package/action.yml)

> [!NOTE]
> This section covers `preview-publish-package*` workflows

Designed to automate the process of building and publishing a preview version of a exile.watch package to a github npm registry, enabling users to test and evaluate changes before the final release. 

|                                    Workflow code                                    | Name                             | Responsibility                                                                        |
|:-----------------------------------------------------------------------------------:|----------------------------------|---------------------------------------------------------------------------------------|
|      [`CI-00`](./preview-publish-package/00-create-status-comment/action.yml)       | Create status comment            | Creates status comment after `preview-publish` label is applied to the branch         |
|        [`CI-01`](./preview-publish-package/01-publish-prerelease/action.yml)        | Publish prerelease               | Creates prerelease in `x.x.x-preview.x` format and publishes to github registry       |
| [`CI-02`](./preview-publish-package/02-update-status-comment-on-success/action.yml) | Update status comment on success | Once the package is published, this workflow updates the status created in `CI-00`    |
| [`CI-03`](./preview-publish-package/03-update-status-comment-on-failure/action.yml) | Update status comment on failure | If `CI-00` or `CI-01` action fails, this workflow updates the status created in CI-00 |
|   [`CI-04`](./preview-publish-package/04-remove-preview-publish-label/action.yml)   | Remove preview publish label     | Removes `preview-publish` label from PR once CI-00 is completed                       |

## Contributing
| `@exile-watch/doryani`                            | Link                                                                                            |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Want to contribute?                               | [Check the docs](https://docs.exile.watch/projects/doryani/contributing)                        |
| Encountered a bug?                                | [Check issues or create a new one](https://github.com/exile-watch/hideout/issues)               |
| Have an idea for a new feature?                   | [Check the discussions or create a new one](https://github.com/exile-watch/hideout/discussions) |

| General                                           | Link                                                                                |
|---------------------------------------------------|-------------------------------------------------------------------------------------|
| exile.watch projects                              | [Read about them here](https://docs.exile.watch/projects/hideout#links-to-projects) | 
| Anything else is on your mind?                    | [Head over to exile.watch's hideout](https://github.com/exile-watch/hideout)        |
| Curious about exile.watch architecture decisions? | [Read exile.watch engineering blog](https://engineering.exile.watch/)               | 