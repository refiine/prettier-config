# @refiine/prettier-config [![current version](https://img.shields.io/npm/v/@refiine/prettier-config.svg?style=flat-square)][projectnpm]

Sharable config for [Prettier][prettier]

## Installation

Install this config then run [install-peerdeps][ipeerdeps] to get dependencies
as development dependencies.

```
npm install @refiine/prettier-config --save-dev
npx install-peerdeps @refiine/prettier-config --save-dev
```

Then add the following line to your package.json file.

```json
{
  "prettier": "@refiine/prettier-config"
}
```

## Extending

If you wish to customise [options][prettieroptions] further, remove the `pettier`
config from package.json and create a prettier file (`/.prettierrc.js`) with the
following.

```js
module.exports = {
  ...require('@refiine/prettier-config'),
  tabs: true,
  tabWidth: 4,
};
```

## VSCode User?

Make sure you have [Prettier extention][prettiervscode] installed and add the
following into the project's settings file (`/.vscode/settings.json`) (deleting
as appropriate).

```json
{
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[scss]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[json]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "typescript.format.enable": false,
  "editor.formatOnSave": true
}
```

[projectnpm]: https://www.npmjs.com/package/@refiine/prettier-config
[prettier]: https://prettier.io/
[prettieroptions]: https://prettier.io/docs/en/options.html
[prettiervscode]: https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode
[ipeerdeps]: https://www.npmjs.com/package/install-peerdeps
