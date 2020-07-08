# Final Steps

Once you package is configured properly, then your on to the _exciting_ part of publishing your package.

**Before you publish your package to NPM**

Even if you've done this 100 times or more, you should test to make sure you're publishing exactly what you want. This can be done using the command `npm publish --dry-run`.

Satisfied that everything works? Great, **commit and push your changes**.

Once pushed, use npm's [version](https://docs.npmjs.com/cli/version) command to set the package version and tag git with this version.

```bash
npm version <major | minor | patch>
```

```bash
npm version 1.0.0-beta.0
```

**Publishing**

Last but not least - publishing. This is done using the command: `npm publish`.

_Congratulations!_ You're now a maintainer.
