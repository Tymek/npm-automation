JS SDK release workflow

### scope

GitHub workflow script that deals with NPM in an optimal way.

### goals

`package.json` version is the single source of truth

on `main` with every push, check if version exists

if a version from `package.json` does not exist in NPM
1. extract pre-release ID (eg. v1.0.5-alpha.0 => alpha)
2. push new version to NPM with correct preId or as `latest`
3. create a tag and a github release

optional: bump "alpha" versions on every commit to `main` that didn't update package.json, or manual action for that.

# Manual steps ("how to use")

1. Create NPM_TOKEN on npmjs.com and add it to the repository actions secret.
