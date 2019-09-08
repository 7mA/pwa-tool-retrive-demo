# pwa-tool-retrive-demo

> pwa + vue

## npm 相关命令

``` bash
# 安装工程依赖
npm install

# 在本地启动调试 server
npm run dev

# 构建线上生产环境产物
npm run build

# 启动编译后的代码，注意，需要在 dist 目录中启动，仅 SSR 模式下有效
npm run start

# 检查代码是否符合规范
npm run lint
```

## lavas command

``` bash

# local test
lavas dev

# package & build
lavas build
```

## switch SPA to SSR
lavas.config.js -> ssr: true
