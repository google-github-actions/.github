# Google GitHub Actions - .github

This repository contains default configuration and shared resources for all Google GitHub Actions repositories.

## Releasing

### Create release pull request

1. Go to the `Actions` tab in this repository
1. Select the `Draft release` workflow
1. Click the `Run workflow` drop down
1. Select the version strategy that corresponds to the semantic versioning update value (more info at [https://semver.org](https://semver.org))
1. Click the `Run workflow` button to run the workflow that will create a release pull request

### Review pull request

Review the release pull request body that includes the release notes that will be published in the release. The files changed in the pull request should include the `package.json`, `package-lock.json` and any compiled files in the `dist` folder.

> **NOTE:** If you need to add more changes or change the version strategy, leave the pull request open, makes your changes and run the previous steps again to update the existing pull request. You can change the version strategy on consecutive runs to update the version in place in the pull request.

### Merge and release

When ready, merge the pull request to trigger the Release workflow to create the release with the specified release version and update the floating tag.
