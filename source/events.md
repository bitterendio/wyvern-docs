---
title: Events
type: guide
order: 4
---

To emit events across all instances, use **window.eventHub** object. See implementation of Google Analytics tracking below as example:

``` js
// somewhere in component
new Vue({
  methods: {
    trackGA() {
      if ( typeof ga == 'function' ) {
        ga('set', 'page', '/' + window.location.pathname.substr(1))
        ga('send', 'pageview')
      }
    },
  },
  created() {
    window.eventHub.$on('track-ga', this.trackGA)
  }
});

// somewhere in another component
window.eventHub.$emit('track-ga')
```