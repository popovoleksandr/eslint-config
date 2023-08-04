# eslint-config

Personal [ESLint](http://eslint.org/) configuration with sensible defaults
that I use in [my JavaScript projects](https://github.com/popovoleksandr/projects).

### Install

To use it in your project, run:

```bash
npm install --save-dev eslint eslint-config-popovoleksandr
```

Then add a following `.eslintrc` file in the repo root:

```json
{
  "extends": "popovoleksandr"
}
```

Finally, add `eslint` to a `package.json` script:

```json
"scripts": {
  "lint": "eslint index.js test/test*.js",
  "pretest": "npm run lint"
}
```

Now run `npm run lint` and enjoy thousands of errors! :)

### Automatic fixes

To make things easier, you can run `eslint` with `--fix` option
that automatically fixes all simple errors like indentation and quotes for you.

### Overrides

Some of the rules may be too strict for your project,
but you can easily override any rules or options like this:

```json
{
  "extends": "eslint-config-popovoleksandr",
  "rules": {
    "space-before-function-paren": 0,
    "indent": [2, 2]
  },
  "env": {
    "mocha": true
  }
}
```
