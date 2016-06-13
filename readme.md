

```
Using Babel 6: Use ^2.0.0
Using Babel 5: Use ^1.0.0
```

A test runner for tape that utilizes babel in order to run test suites that include ESNext/Harmony features.

**Important:** Forked from [babel-tape-runner](https://github.com/wavded/babel-tape-runner).This may get pulled down if the original package adopts this functionality.

## install

Install globally or locally (for npm scripts):

```sh
npm install babel-tape-runner [-g]
```

## usage

Just run `babel-tape-runner` with the files to test (just like tape's bundled runner).  Store configuration in a `.babelrc` file.

```sh
babel-tape-runner --file my-es-next-test.js

babel-tape-runner --files lib/**/__tests__/*-test.js # or glob patterns

babel-tape-runner --files lib/**/__tests__/*-test.js --no-css # to ignore css that's being compiled by babel
```

For example, use this in your `package.json` file so you can run `npm test` to execute your tests:
```json
{
    "scripts": {
        "test": "babel-tape-runner \"lib/**/__tests__/*-test.js\" | tap-diff"
    },
    ""
}
```

## licence

MIT
