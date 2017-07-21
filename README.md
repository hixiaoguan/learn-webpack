# learn-webpack lesson-02

### 如何引入文件：require('./world.js')

### 如何引入CSS文件：require('./style.css')

### 注意：引入样式表文件需要相应的loader,除了js文件默认支持外，其他文件比如 css  文件webpack默认是不支持的，css-loader,style-loader这俩来解决 css 文件 引入问题 css-loader 实现解析 css 生成能让 bundle 接收的代码块，style-loader 实现将 css-loader 生成的 样式 插入到页面的 heade 里。

### loader 需要安装，用的时候需要声明

#### loader 安装 npm install css-loader style-loader --save-dev

#### loader 使用声明 两种方式：

##### 1.引入文件的时候加在路径前 require('style-loader!css-loader!./style.css')

##### 2.命令行打包的时候添加参数的方式

###### require('./style.css')

###### 命令: webpack hello.js hello.bundle.js --module-bind 'css=style-loader!css-loader'

###### 如果监听修改的话可以在后面 添加上 --watch 就可以了

####### progress 显示打包过程

####### display-modules 显示打包模块
