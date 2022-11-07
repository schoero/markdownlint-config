# markdownlint-config

Personal markdownlint config

## Key features

* Linting and autofixing markdown files

### Installation

```sh
npm i --save-dev @schoero/markdownlint-config
```

### Usage

Create a `.markdownlint.jsonc` file with the following content:

```jsonc
{
  "extends": "@schoero/markdownlint-config"
}
```

### VSCode integration

For automatic code formatting on save, install the [markdownlint extension](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint).

To recommend the extension in your repository create a `.vscode/extensions.json` with the following content:

```jsonc
{
  "recommendations": [
    "DavidAnson.vscode-markdownlint"
  ]
}
```

To configure the extension properly, create a `.vscode/settings.json` with the following content:

```jsonc
{
  "[markdown]": {
    "editor.defaultFormatter": "DavidAnson.vscode-markdownlint",
    "editor.formatOnSave": true
  },
  "editor.codeActionsOnSave": {
    "source.fixAll.markdownlint": true
  }
}
```
