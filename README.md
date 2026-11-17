# protolint-action

![Build Status](https://github.com/plexsystems/protolint-action/workflows/build-test/badge.svg)

A GitHub Action for using [protolint](https://github.com/yoheimuta/protolint) in your [GitHub Action](https://github.com/features/actions) workflows.

## Required inputs

- `configDirectory`: the path to where the `.protolint.yaml` configuration exists.

## Example

```yaml
name: "lint protobuf"
on: pull_request

jobs:
  pr-check:
    runs-on: ubuntu-latest
    steps:
      - name: checkout source
        uses: actions/checkout@v1

      - name: run protolint
        uses: plexsystems/protolint-action@v0.4.0
        with:
          configDirectory: test
```

## Privacy

This Action contacts Chainguard's licensing server to verify authorization. Connection metadata (IP address, GitHub repository identifier, timestamp, and any metadata encoded in the auth token) is transmitted to Chainguard, Inc. even if authorization is denied in accordance with our [Privacy Notice](https://www.chainguard.dev/legal/privacy-notice)
