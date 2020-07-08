## ESLint

Setting up ESLint for a package is super easy:

1. Install CloudSense's ESLint config from NPM:

```bash
npm i eslint prettier eslint-config-prettier eslint-plugin-prettier @cloudsense/eslint-config --save-dev
```

1. Open your `package.json` file and link to CloudSense's ESLint configuration. Refer to [eslint-config](https://www.npmjs.com/package/@cloudsense/eslint-config) for configuration options.

![Example ESLint Typescript configuration]({{images}}/eslint-config.png)

1. Create a `.prettierrc.js` file. This should as a starting point contain:

```js
module.exports = {
  singleQuote: true,
  jsxSingleQuote: true,
  printWidth: 130,
  tabWidth: 2,
};
```

1. Finally, add the following to the scripts section of the `package.json`

```json
{ "lint": "eslint src/**/*" }
```
