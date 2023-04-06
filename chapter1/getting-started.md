# 开始

## 快速上手

设置淘宝镜像源
```shell
> npm config set registry https://registry.npmmirror.com/
```

查看当前使用源
```shell
> npm config get registry
https://registry.npmmirror.com/
```

### 使用 vite 作为构建工具
初始化 Vue3 项目
```shell
> npm init vue@latest
```

这一指令将会安装并执行 [create-vue](https://github.com/vuejs/create-vue)，它是 Vue 官方的项目脚手架工具。你将会看到一些诸如 TypeScript 和测试支持之类的可选功能提示：

```shell
√ Project name: ... vue-create-vite
√ Add TypeScript? ... No / Yes #（是否使用 typescript）
√ Add JSX Support? ... No / Yes #（是否支持 jsx 写法）
√ Add Vue Router for Single Page Application development? ... No / Yes #（是否添加vue-router）
√ Add Pinia for state management? ... No / Yes #（是否使用 pinia 管理数据状态）
√ Add Vitest for Unit Testing? ... No / Yes #（是否用 vitest 用于单元测试）
√ Add an End-to-End Testing Solution? » Cypress #（是否使用端到端的自动化测试，这里选用了 cypress）
√ Add ESLint for code quality? ... No / Yes #（是否添加 ESlint）
√ Add Prettier for code formatting? ... No / Yes #（是否添加 Prettier）
```

不确定是否要开启某个功能，你可以直接按下回车键选择 No。在项目被创建后，通过以下步骤安装依赖并启动开发服务器：

```shell
> cd <your-project-name>
> npm install
> npm run dev
```

### 使用 webpack 作为构建工具
因为 vite 仍有些兼容性问题，所以在大型项目还是推荐 webpack 作为构建工具。至于 webpack 的加速打包，可以用 esbuild-loader 替换 babel-loader 来实现。

或者可以采用兼容模式，即在开发环境使用 vite，生产环境使用 webpack。然后这里继续用 vue-cli 作为脚手架工具，创建名为 vue-create-webpack的项目：

安装 vue-cli
```shell
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```

可以看到是采用了 webpack5 的版本，还是有很多新特性的，比如：模块联邦、自带压缩terser-webpack-plugin、自带热更新等等。
