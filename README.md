# Yandex Metrika
[![npm](https://img.shields.io/npm/dt/@ruvents/yandex-metrika.svg?style=flat-square)](https://www.npmjs.com/package/@ruvents/yandex-metrika)
[![npm (scoped with tag)](https://img.shields.io/npm/v/@ruvents/yandex-metrika/latest.svg?style=flat-square)](https://www.npmjs.com/package/@ruvents/yandex-metrika)

> Add Yandex Metrika to your nuxt.js application.

This plugins automatically sends first page and route change events to yandex metrika.

**Note:** yandex metrika is not enabled in dev mode.
You can set environment variable `NODE_ENV` to `production` for testing in dev mode.

## Setup

- Add `@ruvents/yandex-metrika` dependency using yarn or npm to your project
- Add `@ruvents/yandex-metrika` to `modules` section of `nuxt.config.js`

```js
{
  modules: ['@ruvents/yandex-metrika'],
}
```

## Configure

You can pass options directly in module declaration:

```js
{
  modules: [
    [
      '@ruvents/yandex-metrika',
      {
        id: 'XXXXXX',
        webvisor: true,
        // clickmap: true,
        // useCDN: false,
        // trackLinks: true,
        // accurateTrackBounce: true,
      }
    ]
  ]
}
```

Or you can specify `yandexMetrika` key:

```js
{
  modules: ['@ruvents/yandex-metrika'],
  yandexMetrika: {
    id: 'XXXXXX',
    // ...
  }
}
```

In Nuxt 2.13+, you can also use public runtime config:

```js
{
  modules: ['@ruvents/yandex-metrika'],
  publicRuntimeConfig: {
    yandexMetrika: {
      id: process.env.YANDEX_METRIKA_ID,
      // ...
    }
  }
}
```

## Options

For more information:
- [Documetation for Ya.Metrika](https://yandex.com/support/metrica/code/counter-initialize.html)
- [hit method](https://yandex.com/support/metrica/objects/hit.html)

### `id`

- Required

### `useRuntimeConfig`

- Default: `yandexMetrika`

Public runtime config key. Set to `false` to disable runtime configuration.

### `useCDN`

- Default: false

Load metrika script from <https://cdn.jsdelivr.net/npm/yandex-metrica-watch/watch.js>.

This option can not be provided via runtime config.

### `queryFilter` 

- Default: `undefined`

Array of keys which must be excluded in queries.

### `accurateTrackBounce`
### `childIframe`
### `clickmap`
### `defer`
### `ecommerce`
### `params`
### `userParams`
### `trackHash`
### `trackLinks`
### `trustedDomains`
### `type`
### `ut`
### `webvisor`
### `triggerEvent`




