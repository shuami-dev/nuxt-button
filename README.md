## Nuxt 3 Custom Button

This is a package that can be used in Nuxt 3 projects.

## How to Use

### Install
```npm i @shuami-dev/nuxt-button```

### In your Nuxt project (nuxt.config.ts)

```vue
export default defineNuxtConfig({
  ...
  css: [
    '@shuami-dev/nuxt-button/style.css'
  ]
})
```
### In your Nuxt project (e.g: index.ts)

```vue
<template>
  <PrimaryButton label="Primary" @click="primaryClick" />
  <WarningButton label="Warning" @click="warningClick" />
</template>
```