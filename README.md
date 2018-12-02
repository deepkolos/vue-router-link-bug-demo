# vue-router-link-bug-demo

![router-link-bug.gif](https://upload-images.jianshu.io/upload_images/252050-56ab6f579680300d.gif?imageMogr2/auto-orient/strip)

App.vue
```vue
<template>
  <div id="app">
    <img src="./assets/logo.png">
    <keep-alive>
      <router-view />
    </keep-alive>
  </div>
</template>
```

f-link.vue
```
  name: 'f-link',
  functional: true,

  render(h, context) {
    const staticClass = context.data ? context.data.staticClass || '' : '';

    return h(
      'router-link',
      {
        props: context.props,
        attrs: {
          class: `f-link ${staticClass}`
        }
      },
      context.children
    );
  }
```

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
