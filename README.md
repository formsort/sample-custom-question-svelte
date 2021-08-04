# sample-custom-question-svelte

A sample custom question for use in [Formsort](https://formsort.com) using the [Custom Question API](https://www.npmjs.com/package/@formsort/custom-question-api).

## Note

Note that this is the vanilla svelte template, but with a tweak to preferBuiltins in the `rollup-plugin-resolve` config:

```js
resolve({
  browser: true,
  preferBuiltins: false,
  dedupe: ['svelte']
}),
```
