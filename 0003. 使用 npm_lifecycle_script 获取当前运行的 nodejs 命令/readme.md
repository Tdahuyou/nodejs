# 0003. 使用 npm_lifecycle_script 获取当前运行的 nodejs 命令

- npm_lifecycle_script 是什么
- npm_lifecycle_script 有啥用

## 📒 notes - npm_lifecycle_script 是什么?

`process.env.npm_lifecycle_script` 是 **Node.js 中的一个环境变量**，它包含当前正在运行的 npm 脚本的 **实际命令字符串**。这是在使用 npm 脚本时，**npm 自动注入** 的一部分环境变量之一。

当你运行一个 npm 脚本时，比如 `npm start` 或 `npm run build`，npm 会设置一系列的环境变量，这些环境变量可以在你的 Node.js 应用程序中访问。`process.env.npm_lifecycle_script` 就是其中之一，它表示 **当前 npm 脚本正在执行的命令**。

## 📒 notes - npm_lifecycle_script 的作用

`npm_lifecycle_script` 可以帮你捞到当前正在运行的 npm 脚本，若程序中有相关逻辑需要读取当前正在运行的 npm 脚本，可以利用 `process.env.npm_lifecycle_script` 这个环境变量。

## 📒 notes - 运行示例

```bash
# 执行命令
$ npm run start
# 会在命令行输出以下内容：
# Current npm lifecycle script: node 1.js

# process.env.npm_lifecycle_script
# 表示 node 1.js
# 也就是当前执行的 nodejs 命令
```

## 💻 demo

**初始化**：假设你有一个项目，其中的 package.json 文件如下。

```json
{
  "name": "demo-project",
  "version": "1.0.0",
  "scripts": {
    "start": "node 1.js",
    "build": "echo 'Building project...' && node 1.js"
  }
}
```

**准备测试用例**:你可以在 `1.js` 文件中访问 `process.env.npm_lifecycle_script` 变量。

```js
// 1.js
console.log('Current npm lifecycle script:',
            process.env.npm_lifecycle_script);
```

**测试 - 运行示例**

当你运行 `npm start` 时，`npm_lifecycle_script` 将被设置为 `node 1.js`。

```bash
$ npm run start

# > demo-project@1.0.0 start
# > node 1.js

# Current npm lifecycle script: node 1.js
```

当你运行 `npm run build` 时，`npm_lifecycle_script` 将被设置为 `echo 'Building project...' && node 1.js`。

```bash
$ npm run build

# > demo-project@1.0.0 build
# > echo 'Building project...' && node 1.js

# Building project...
# Current npm lifecycle script: echo 'Building project...' && node 1.js
```