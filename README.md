# Update Open in VSCode Link

[![Open in Visual Studio Code](https://open.vscode.dev/badges/open-in-vscode.svg)](https://open.vscode.dev/markpatterson27/update-open-in-vscode-link)

GitHub Action that parses README and updates the 'Open in Visual Studio Code' link to work for the current repository. Intended use is for template or forked repositories, to update the link from the original respoitory to the new copied repository.

## Usage

An example workflow

```yaml
name: Update Link

on:
  create:

  # Allows you to run this workflow manually from the Actions tab
  workflow_dispatch:

jobs:
  build:
    name: Update link
    runs-on: ubuntu-latest
    if: ${{ github.ref == 'refs/heads/main' }}
    steps:
      - name: Checkout
        uses: actions/checkout@v2

      - name: Update link action step
        uses: markpatterson27/update-open-in-vscode-link@v1
```
