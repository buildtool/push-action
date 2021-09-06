<p align="center">
  <h3 align="center">Buildtool Push Action</h3>
  <p align="center"><a href="https://github.com/features/actions">GitHub Action</a> for <a href="https://buildtools.io/commands/#push">Buildtool Push</a></p>
  <p align="center">
    <a href="https://github.com/buildtool/push-action/releases/latest"><img alt="GitHub release" src="https://img.shields.io/github/release/buildtool/push-action.svg?logo=github"></a>
    <a href="https://github.com/marketplace/actions/github-action-for-push"><img alt="GitHub marketplace" src="https://img.shields.io/badge/marketplace-push--action-blue?logo=github"></a>
  </p>
</p>

---

## Usage

Below is a simple snippet to use this action.

```yaml
name: buildtool

on:
  pull_request:
  push:

jobs:
  goreleaser:
    runs-on: ubuntu-latest
    steps:
      -
        name: Checkout
        uses: actions/checkout@v1
      -
        name: Run build-tools push command
        uses: buildtool/push-action@v1
        with:
          dockerfile: dockerfiles/Dockerfile.push
```

## Customizing

### Inputs

Following inputs can be used as `step.with` keys

| Name                      | Type    | Default         | Description                                   |
|---------------------------|---------|-----------------|-----------------------------------------------|
| ` dockerfile`             | String  | `Dockerfile`    | To use a specific Dockerfile in your project  |


## License

MIT. See `LICENSE` for more details.