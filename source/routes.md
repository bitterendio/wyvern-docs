---
title: Routes
type: guide
order: 5
---

## Override in child theme

Sometimes you need to override components in child theme. Wyvern registers some basic components like Page and then registers routes using these components.

``` js
// app.js
import Page from './page.vue'
Vue.component('Page', Page)
```

Now your child theme might need different layout for Page component, therefore after you register new component, use **routes.refresh()**.

``` js
// main.js (for example child theme)
import Page from './page.vue'
Vue.component('Page', Page)

// Replace overridden components in existing routes
routes.refresh()
```