---
layout: post
title: Setting up React, ES6, Babel 6, and Webpack to work together
---
This is a quick guide on how to setup and configure for React v0.14, Babel 6, and Webpack so that you can use ES6 (aka ES2015). Babel 6, released on 10/29/2015, has fundamental changes that will necessitate updates in `package.json` and `webpack.config.js`.  Babel 6 no longer automatically transpiles ES6, but does have separate ES6 and React preset modules. 

This guide is based on my recent web app, TypeReact. You can view the site at [typereact.com](http://typereact.com). Source code can be found [here](https://github.com/typereact/typereact). TypeReact also uses React-Redux and React-Router, both of which support and take advantage of ES6.

#### package.json
To run ES6, you will want to `npm install --save` the following:

```javascript
"babel-polyfill": "^6.3.14",
"babel-runtime": "^6.3.13",
```

In your dev dependencies, you will want to `npm install --save-dev` the following:

```javascript
"babel": "^6.3.13",
"babel-cli": "^6.3.13",
"babel-core": "^6.3.13",
"babel-loader": "^6.2.0",
"babel-plugin-transform-es2015-modules-commonjs": "^6.3.13",
"babel-plugin-transform-runtime": "^6.3.13",
"babel-preset-es2015": "^6.3.13",
"babel-preset-react": "^6.3.13",
```

If you are not using Webpack, it is also possible to set the Babel configuration in `package.json`. However, pick one or the other, not both.

```javascript
"babel": {
  "presets": [
    "es2015",
    "react"
  ]
}
```


#### webpack.config.js
For webpack, continue to use `babel-loader`. However you also will need to let Babel know to query plugins and presets:

```javascript
module: {
  loaders: [
    { 
      test: /\.jsx?$/, 
      loader: 'babel-loader', 
      query: {
          plugins: ['transform-runtime', 'transform-es2015-modules-commonjs'],
          presets: ['es2015', 'react']
      },
      exclude: /node_modules/ 
    },
  ]
}
```


#### React v0.14 tip
React v0.14 was released 10/6/2015.

One notable change for React v0.14 from earlier versions is the separation of react and reactDOM dependencies. Basically, instead of rendering with `react.render()`, it is now `reactDOM.render()`. Not updating this change probably won't break your app, but you will get warning messages in your console and helpful suggestions to refactor your code.

