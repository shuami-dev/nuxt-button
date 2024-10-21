## Nuxt 3 Custom Button

A collection of customizable Vue button components for Nuxt 3, built with TypeScript.

## How to Use

### Install

```bash
npm i @shuami-dev/nuxt-button
```

### In your Nuxt project (nuxt.config.ts)

```ts
export default defineNuxtConfig({
  ...
  css: [
    '@shuami-dev/nuxt-button/style.css'
  ]
})
```

### In your Nuxt project (e.g: index.ts)

```vue

<script setup lang="ts">
  import { PrimaryButton, WarningButton } from '@shuami-dev/nuxt-button'

  const handleClick = () => {
    alert('Button clicked!')
  }
</script>

<template>
  <PrimaryButton label="Primary" @click="handleClick"/>
  <WarningButton label="Warning" @click="handleClick"/>
</template>
```
