# release API

a small demo on how you could use the GitHub release API to provide metadata around versions

## usage

A `release.json` file lives on the [release page](https://github.com/EverlastingBugstopper/release-api/releases) for v1.0.0. This file can be modified at any time by the repo administrator to deprecate versions (potentially to show warning messages in supportive tooling).

A one-liner to get this deprecation info:

```console
$ curl -sSL -H "content-type: application/json" https://github.com/EverlastingBugstopper/release-api/releases/download/v1.0.0/release.json | jq .deprecated
false
```
