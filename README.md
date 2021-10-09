# Repro `tsm` native esm

Minimal reproducible case for [tsm](https://github.com/lukeed/tsm) bug.

## Instructions

1. Install dependencies
1. Run `start` script e.g., `npm start`

## Result

```sh
> node -r tsm index.ts

/home/max/Projects/repro-tsm-native-esm/index.ts:1
import getPort from 'get-port';
                                                                                                                                                                                                                    ^

Error [ERR_REQUIRE_ESM]: require() of ES Module /home/max/Projects/repro-tsm-native-esm/node_modules/.pnpm/get-port@6.0.0/node_modules/get-port/index.js from /home/max/Projects/repro-tsm-native-esm/index.ts not supported.
Instead change the require of index.js in /home/max/Projects/repro-tsm-native-esm/index.ts to a dynamic import() which is available in all CommonJS modules.
    at Object.apply (/home/max/Projects/repro-tsm-native-esm/index.ts:1:213)
    at Object.<anonymous> (/home/max/Projects/repro-tsm-native-esm/index.ts:20:34)
    at Module.t._compile (/home/max/Projects/repro-tsm-native-esm/node_modules/.pnpm/tsm@2.1.0/node_modules/tsm/require.js:1:935)
    at Object.loader (/home/max/Projects/repro-tsm-native-esm/node_modules/.pnpm/tsm@2.1.0/node_modules/tsm/require.js:1:948) {
  code: 'ERR_REQUIRE_ESM'
}
```
