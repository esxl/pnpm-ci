# `esxl/pnpm-ci`

A [GitHub Action](https://docs.github.com/en/actions) that contains steps for building EcmaScript based packages.

## Table of contents

<details><summary> Click to expand table of contents</summary>

- [`esxl/pnpm-ci`](#esxlpnpm-ci)
  - [Table of contents](#table-of-contents)
  - [Use](#use)
  - [Configure](#configure)
  
</details>

## Use

1. Create a new file, for example _ci.yaml_, in the _.github/workflows/_ directory:

   ```bash
   touch .github/workflows/ci.yaml
   ```

1. Add the following to the file you just created:

   ```yaml
   name: pnpm ci

   env:
     CI: true

   on:
     pull_request:
       branches: [main]

     push:
       branches: [main]

   jobs:
     build:
       runs-on: ubuntu-latest
       steps:
         - uses: esxl/pnpm-ci@v0.3.0
   ```

## Configure

This workflow uses the [setup-node](https://github.com/actions/setup-node#readme) action and accepts all of its inputs. See `action/setup-node`'s [action.yaml](https://github.com/actions/setup-node/tree/v4.0.3/action.yml) for more details.

See this repository's [action.yaml](./action.yaml) file for documentation on additional inputs.
