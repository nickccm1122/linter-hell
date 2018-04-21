# linter-hell

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![lerna](https://img.shields.io/badge/maintained%20with-lerna-cc00ff.svg)](https://lernajs.io/)

This repo consists different kind of sharable linting tools config.

## How to start

run `lerna bootstrap` to install packages' dependencies.

There is lerna config to use `Yarn`'s [workspace](https://yarnpkg.com/blog/2017/08/02/introducing-workspaces/) to symlink inter-dependencies.

```diff js
  ...
  "workspaces": [
+   "packages/*"
  ],
  ...
```

```diff js
  {
  "lerna": "2.9.1",
  "version": "independent",
  "npmClient": "yarn",
+ "useWorkspaces": true,
  "npmClientArgs": ["--production", "--no-optional"],
  "command": {
    "publish": {
      "message": "chore(release): publish"
    }
  }
}

```
