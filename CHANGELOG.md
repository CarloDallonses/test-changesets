# test-changesets

## 1.0.3

### Patch Changes

- 4eb9e4b: adds support to github pacakges

## 1.0.2

### Patch Changes

- 1fbe788: Add onDispose to the plugin API (#1)

  If your plugin wants to perform some cleanup after it's no longer going to be used, you can now use the onDispose API to register a callback for cleanup-related tasks. For example, if a plugin starts a long-running child process then it may want to terminate that process when the plugin is discarded. Previously there was no way to do this. Here's an example:

  ```js
  let examplePlugin = {
    name: "example",
    setup(build) {
      build.onDispose(() => {
        console.log("This plugin is no longer used");
      });
    },
  };
  ```

  These onDispose callbacks will be called after every build() call regardless of whether the build failed or not as well as after the first dispose() call on a given build context.

## 1.0.1

### Patch Changes

- 27a7c4f: fixes some bug blablabla
- b53156e: adds debug log
- 42be089: fixes tiny thing balbla
- a3ba3c8: silly fix

## 1.0.0

### Major Changes

- 824aaec: adds breaking change (edited after creation)
