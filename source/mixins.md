---
title: Mixin methods
type: guide
order: 3
---
## Menu

- Note: Menu API calls require WP API Menus plugin

**getMenuLocation(location, [callback])** allows retrieving menu by it's location. Sample usage in component:

``` html
<script>
export default {
  mounted() {
    this.getMenuLocation('primary', data => this.menu = data)
  },
  data() {
    return {
      menu: []
    }
  }
}
</script>
<template>
  <ul>
    <li v-for="item in menu">
      <router-link :to="{ path: item.url }">{{ item.title }}</router-link>
    </li>
  </ul>
</template>
```