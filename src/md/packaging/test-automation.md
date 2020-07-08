## Test Automation

Your package should have tests and overall test coverage should be above **80%**.

**DO NOT publish a package which isnt thoroughly tested**.

There are numerous Node offering of test runners - commonly [Jest](https://jestjs.io/) and [Mocha](https://mochajs.org/). Both support automatically collection of test coverage results.

Below is the recommended configuration for Jest's `collectThreshold` functionality.

```json
{
  "coverageThreshold": {
    "global": {
      "branches": 80,
      "functions": 80,
      "lines": 80,
      "statements": 80
    }
  }
}
```

If coverage falls below 80% this will throw an error.

### Setting up the prepublishOnly script

Now that we have automatic test suite execution and linting, we can now add the following script to our `package.json` file. **NOTE**: this configuration is for a Typescript project.

```JSON
{
  "test": "jest",
  "lint": "eslint src/**/*.ts",
  "build": "tsc",
  "prepublishOnly": "npm run lint && npm run test && npm run build"
}
```

This `prepublishOnly` script - is only run before publishing a package by NPM itself. In other words, you dont need to invoke it.

You can even test that this is the case by using the command `npm publish --dry-run`.
