# vite-plugin-vue2 (fork)

This is the fork of the original [vite-plugin-vue2](https://github.com/underfin/vite-plugin-vue2) that adds missing features like custom blocks parsing. It will be deprecated once the original one gets such features.

## Usage

Add the plugin to your npm module:

1. run `yarn add @yfwz100/vite-plugin-vue2 --dev`
2. add the plugin into `vite.config.js`
   ``` js
   // vite.config.js
   const { createVuePlugin } = require('@yfwz100/vite-plugin-vue2')

   module.exports = {
     plugins: [createVuePlugin(/*options*/)],
   }
   ```

If you use the original plugin before, you can use this plugin as a dropin replacement.

e.g. in the `package.josn`:

```json
{
  "dependencies": {
    "vite-plugin-vue2": "npm:@yfwz100/vite-plugin-vue2@latest"
  }
}
```

## [Options](https://github.com/underfin/vite-plugin-vue2/blob/master/src/index.ts#L26)

### `vueTemplateOptions`

Type: `Object`<br>
Default: `null`

The options for `@vue/component-compiler-utils`.

### `jsx`

Type: `Boolean`<br>
Default: `false`

The options for jsx transform.

### `jsxOptions`

Type: `Object`<br>

The options for `@vue/babel-preset-jsx`.

## Todo

- SSR Build
- Sourcemap