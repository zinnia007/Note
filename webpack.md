#### 初始化项目

+ ```js
  npm init 
  // 配置 package.json 命令脚本 script 
  "script": {
     	"build":"webpack"
  }
  ```

+ ```js
  // 安装本地webpack
  npm i webpack webpack-cli -D 
  ```

+  新建 `webpack` 配置文件 ` webpack.config.js`  

  ```js
  module.exports = {
      // 模式-- 开发模式、 生产模式
      mode: 'development',
      // 配置入口
      entry: './src/main.js',
      // 配置出口
      output: {
          filename: '[name].js',
          path: path.resolve(__dirname, 'dist')
      }
  
  }
  ```

  ####  htmlWebpackPlugin

  ```js
  // 用来生成一个 html 页面的入口文件，并且能自动引入打包的 js、css 文件
  new HtmlWebpackPlugin({
      title: 'zinnia html', // 设置 html title
      filename: 'zinnia.html', // 设置文件名
      template: './public/index.html', // 提前设置一个模板路径
      templateContent: '<div>kkkk<div>',  // 设置模板内容字符串
      publicPath: '',//  可以设置引入 js, css 的公共路径
      inject: 'body', // script 注入到什么位置
      minify: '', // 生产模式设置false，进行代码压缩， 
      hash: true, // 引入 js css 文件的时候，会加哈希码，防止缓存导致的不更新
      chunks: [],// 针对多入口的情况， 可以在数组中指定引入哪些打包之后的 js 入口文件
      chunksSortMode: '', // 引入的文件，进行排序
      excludeChunks: [], // 与 chunks 相反， 不包括哪些文件
  })
  ```
  
  #### 配置 rules
  
  ```js
  
  
  ```
  
  #### 安装babel 7
  
  ```js
  // 安装
  npm install --save-dev @babel/core @babel/cli @babel/preset-env
  ```
  
  

