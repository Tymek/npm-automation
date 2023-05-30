JS SDK release workflow

## How-to

### Publish new version

- In GitHub go to "Actions" → "🚀 Release".
- Click "Run workflow" button
- Fill in new version number in SemVer format (e.g. `1.2.3` or `0.1.3-alpha.0`)
- If you want to publish pre-release, type something else then `latest` in `NPM tag` input. For example `beta`. This will mark pushed package version as not "default", and generate pre-release in GitHub.
- Click "Run workflow" button

There is no guardrails for publishing new version. Make sure branch, number and tag are correct!

### Configuration

Reusable workflow requres 2 secrets to be set in repository: `GH_ACCESS_TOKEN` and `NPM_ACCESS_TOKEN`.

Aside of `version` and `tag` it's possible to configure `working-directory` - this is the location of `package.json`.
