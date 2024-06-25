最小化的monorepo示例

## 项目结构

apps: 存放最终打包的项目

packages: 存放可引入的模块, 比如utils, components 等等

pnpm-workspace.yaml: 工作区配置

项目结构如下

├── apps    项目
│   └── demo
│       ├── package.json
│       └── src
│           └── index.ts
├── node_modules
├── package.json
├── packages    模块管理
│   └── utils
│       ├── index.ts
│       ├── package.json
│       └── src
│           └── functions.ts
├── docs     文档
├── pnpm-lock.yaml
├── pnpm-workspace.yaml 工作区配置文件

## 使用方法

初始化 `pnpm install`

导本地包

`cd apps/demo`

`pnpm add 本地包名 如(@monorepo-with-pnpm/utils)`

现在 在apps的具体项目里可以正常使用packages下utils里的add函数了, 可以在 `apps\monorepo-with-pnpm\apps\demo\src\index.ts`查看代码, 如果没有报错, 并且正确看到函数提示, 就是正常了
