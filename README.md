# vitest-webgl-canvas-mock

> Mock `canvas` and `WebGL` when running unit test cases with vitest.

## Disclaimer

This project is a fork of [jest-webgl-canvas-mock](https://github.com/Adamfsk/jest-webgl-canvas-mock) so that both 2d and webgl contexts can be tested in vitest. As such, the only tests provided are those from the original projects. 

The current goal of this project is simply to make any tests using `pixi.js` work in vitest.

Please feel free to contribute and add any additional functionality required.

## Install

This should only be installed as a development dependency (`devDependencies`) as it is only designed for testing.

```bash
npm i vitest-webgl-canvas-mock
```

## Setup

In `__setups__/canvas.js`

```js
import 'vitest-webgl-canvas-mock';
```

In `vitest.config.js`
```js
import { defineConfig } from 'vite'

export default defineConfig({
    test: {
        setupFiles: ['__setups__/canvas.js']
        environment: 'jsdom'
    }
})

```

## License

MIT
