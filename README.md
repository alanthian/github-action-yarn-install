<!-- start title -->

# GitHub Action: yarn-install-action

<!-- end title -->

<!-- start description -->

Install Yarn Dependencies via Github Action.

<!-- end description -->

<!-- start usage -->

```yaml
- uses: luminsports/github-action-yarn-install@main
  with:
    # Changes node's process.cwd() if the project is not located on the root. Default to process.cwd()
    # Default: .
    cwd: ""

    # Add a specific cache-prefix
    # Default: default
    cache-prefix: ""

    # Cache npm global cache folder often used by node-gyp, prebuild binaries (invalidated on lock/os/node-version)
    # Default: true
    cache-npm-cache: ""

    # Cache node_modules, might speed up link step (invalidated lock/os/node-version/branch)
    # Default: false
    cache-node-modules: ""

    # Cache yarn install state, might speed up resolution step when node-modules cache is activated (invalidated lock/os/node-version/branch)
    # Default: false
    cache-install-state: ""

    # Enable corepack
    # Default: false
    enable-corepack: ""
```

<!-- end usage -->

<!-- start inputs -->

| **Input**                 | **Description**                                                                                                                         | **Default** | **Required** |
| :------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------- | :---------: | :----------: |
| **`cwd`**                 | Changes node's process.cwd() if the project is not located on the root.                                                                 |     `.`     |  **false**   |
| **`cache-prefix`**        | Add a specific cache-prefix.                                                                                                            |  `default`  |  **false**   |
| **`cache-npm-cache`**     | Cache npm global cache folder often used by node-gyp, prebuild binaries (invalidated on lock/os/node-version)                           |   `true`    |  **false**   |
| **`cache-node-modules`**  | Cache node_modules, might speed up link step (invalidated lock/os/node-version/branch).                                                 |   `false`   |  **false**   |
| **`cache-install-state`** | Cache yarn install state, might speed up resolution step when node-modules cache is activated (invalidated lock/os/node-version/branch) |   `false`   |  **false**   |
| **`enable-corepack`**     | Enable corepack.                                                                                                                        |   `false`   |  **false**   |

<!-- end inputs -->
