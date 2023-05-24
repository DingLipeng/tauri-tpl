# Tauri App Template

Tauri 跨平台桌面应用开发模板

## 运行环境

语言、运行时

* Rust
* Node.js

全局组件、依赖

```shell
npm i -g sort-package-json
cargo install cargo-outdated

```

## 运行/调试

```shell
git clone https://github.com/DingLipeng/tauri-tpl.git my-project
cd my-project

npm install
npm run start

```

## IDE 配置

推荐：[Jetbrains CLion](https://www.jetbrains.com/clion/)

1. Attach Cargo Project (follow IDE tip when you open cargo.toml)
2. Open Cargo Check (Setting - Languages & Frameworks - Rust-External Linters,check the `run external linters....`)
3. Open Automatic Prettier (Setting - Search prettier)
4. Open Automatic Eslint (Setting - Search eslint)
5. Setting - Tools - Actions on save: check the `run eslint -fix` and `Run prettier`
6. Setting - Languages&Frameworks - Rust - Rustfmt: `check the use rustfmt instead of...`

## 技术栈及开发文档

* [Tauri](https://tauri.app)
* [Vite](https://vitejs.dev)
* [Vue3](https://vuejs.org/)
* [Typescript](https://www.typescriptlang.org/)
* [ElementPlus](https://element-plus.gitee.io/zh-CN/)
* [Jetbrains Mono](https://www.jetbrains.com/lp/mono/)

# Original Official Document

## Tauri + Vue 3 + TypeScript

This template should help get you started developing with Vue 3 and TypeScript in Vite. The template uses Vue
3 `<script setup>` SFCs, check out
the [script setup docs](https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup) to learn more.

## Recommended IDE Setup

- [VS Code](https://code.visualstudio.com/) + [Volar](https://marketplace.visualstudio.com/items?itemName=Vue.volar) + [Tauri](https://marketplace.visualstudio.com/items?itemName=tauri-apps.tauri-vscode) + [rust-analyzer](https://marketplace.visualstudio.com/items?itemName=rust-lang.rust-analyzer)

## Type Support For `.vue` Imports in TS

Since TypeScript cannot handle type information for `.vue` imports, they are shimmed to be a generic Vue component type
by default. In most cases this is fine if you don't really care about component prop types outside of templates.
However, if you wish to get actual prop types in `.vue` imports (for example to get props validation when using
manual `h(...)` calls), you can enable Volar's Take Over mode by following these steps:

1. Run `Extensions: Show Built-in Extensions` from VS Code's command palette, look
   for `TypeScript and JavaScript Language Features`, then right click and select `Disable (Workspace)`. By default,
   Take Over mode will enable itself if the default TypeScript extension is disabled.
2. Reload the VS Code window by running `Developer: Reload Window` from the command palette.

You can learn more about Take Over mode [here](https://github.com/johnsoncodehk/volar/discussions/471).
