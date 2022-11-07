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

If you want to have linting scripts, you can use something like this in the `package.json`:

```jsonc
{
  "scripts": {
    "markdownlint": "node_modules/markdownlint-cli2/markdownlint-cli2.js '**/*.md' '#node_modules'",
    "markdownlint:ci": "npm run markdownlint",
    "markdownlint:fix": "node_modules/markdownlint-cli2/markdownlint-cli2-fix.js '**/*.md' '#node_modules'"
  }
}
```
