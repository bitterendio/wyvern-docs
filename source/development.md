---
title: Development
type: guide
order: 8
---

Wyvern's development tools are using webpack so if you don't have webpack installed globally run:


``` bash
#with yarn
yarn global add webpack
#with npm
npm install webpack -g
```

Webpack configuration is stored in ``webpack.config.js``

## Development commands


| command           | description                          | using tasks                                                                                    |
|-------------------|--------------------------------------|------------------------------------------------------------------------------------------------|
| ``npm run build`` | Run task once                        | ``webpack --config webpack.config.prod.js --progress --colors --display-error-details``        |
| ``npm run dev``   | Watch changes in files and run tasks | ``webpack --config webpack.config.dev.js --progress --colors --display-error-details --watch`` |

## Styles

- Styles could be written as Sass-like markup
- Styles could be stored in ``style.scss`` or inline in ``.vue`` templates
- Webpack watch for ``.scss`` files
- Styles are transforming to ``.css`` by [PostCSS][post-css]
- [PostCSS][post-css] configruation is stored in ``postcss.config.js``
- [PostCSS][post-css] uses [PostCSS SCSS][postcss-scss] as parser and [PreCSS][precss], [PostCSS-Assets][postcss-assets], [PostCSS-Calc][postcss-calc] as plugins 

[post-css]: https://github.com/postcss/postcss
[postcss-scss]: https://github.com/postcss/postcss-scss
[precss]: https://github.com/jonathantneal/precss
[postcss-assets]: https://github.com/assetsjs/postcss-assets
[postcss-calc]: https://github.com/postcss/postcss-calc