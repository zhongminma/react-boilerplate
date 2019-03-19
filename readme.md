
https://www.robinwieruch.de/minimal-react-webpack-babel-setup/

First step <webpack>
1. create src folder and index.js which inside of it.

2. create dist folder and index.html which inside of it
	bundle.js file will be a generated file by Webpack 
	id=“app” let root React component to find entry point

3. install webpack etc
	$> npm install --save-dev webpack webpack-dev-server webpack-cli

webpack: module bundler and build tool
webpack-dev-server: serve your bundled app in a local environment
webpack-cli: configure Webpack setup in a configuration file 


4. add webpack.config.js


Second step <babel>
1. npm install --save-dev @babel/core @babel/preset-env
2. npm install --save-dev babel-loader
3. npm install --save-dev @babel/preset-react
4. Create .babelrc file 

{
  "presets": [
    "@babel/preset-env",
    "@babel/preset-react"
  ]
}

5. Add module in webpack.config.js
module: {
    rules: [
      {
        test: /\.(js|jsx)$/,
        exclude: /node_modules/,
        use: ['babel-loader']
      }
    ]
  },
  resolve: {
    extensions: ['*', '.js', '.jsx']
  }
6. restart webpack with "npm start"
