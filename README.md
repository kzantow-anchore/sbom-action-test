# sbom-action test project

This is a repository to test the [sbom-action](https://github.com/anchore/sbom-action)

It's possible to run both a branch of syft and a branch of the sbom-action, something like:

```yaml
# use sbom-action from a different repo with the use-correlator-field branch
- uses: kzantow-anchore/sbom-action@use-correlator-field
with:
  image: alpine:latest
  artifact-name: image.spdx.json
  dependency-snapshot: true
  # instead of using a syft release, use a different repo with the update-github-format branch
  syft-version: https://github.com/kzantow-anchore/syft/archive/refs/heads/update-github-format.zip
```

### To build the app

Builds a web bundle and makes a Docker image.

```shell
npm run package
```
