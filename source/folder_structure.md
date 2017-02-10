---
title: Folder structure
type: guide
order: 2
---

```
wyvern
|
|   postcss.config.js           PostCSS configuration file
|   style.scss                  PostCSS styles with Sass markup
|   
└──api                          Files for customization WP Rest Api 2
|   └───example.php                 Sample code for custom endpoint
└───assets                      Assets (Images etc.)
└───build                       Configurations for webpack
|   └───webpack.config.dev.js       Webpack config for development
|   └───webpack.config.js           Basic webpack configuration
|   └───webpack.config.prod.js      Webpack config for production
└───dist                        Compiled javascripts with styles
└───lib                         PHP libraries
└───src                         Main logic (.js and .vue files)
```