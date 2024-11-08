### [0001. 使用 process 模块来区分不同的操作系统](https://github.com/Tdahuyou/nodejs/tree/main/0001.%20%E4%BD%BF%E7%94%A8%20process%20%E6%A8%A1%E5%9D%97%E6%9D%A5%E5%8C%BA%E5%88%86%E4%B8%8D%E5%90%8C%E7%9A%84%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F) <!-- [locale](./0001.%20%E4%BD%BF%E7%94%A8%20process%20%E6%A8%A1%E5%9D%97%E6%9D%A5%E5%8C%BA%E5%88%86%E4%B8%8D%E5%90%8C%E7%9A%84%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F/README.md) -->

很简单也很常用的操作 - 通过 process.platform 中记录的当前平台信息来区分不同的操作系统。

```js
function printPlatform() {
  if (process.platform === 'linux') console.log('当前使用的操作系统是 Linux')
  else if (process.platform === 'darwin') console.log('当前使用的操作系统是 MacOS')
  else if (process.platform === 'win32') console.log('当前使用的操作系统是 Windows')
  else console.log('当前使用的操作系统是未知')
}

printPlatform()
```

![](md-imgs/2024-09-24-15-59-17.png)

<!-- !====================>分隔符<====================! -->
### [0002. crypto 模块中的 hash 工具方法 createHash](https://github.com/Tdahuyou/nodejs/tree/main/0002.%20crypto%20%E6%A8%A1%E5%9D%97%E4%B8%AD%E7%9A%84%20hash%20%E5%B7%A5%E5%85%B7%E6%96%B9%E6%B3%95%20createHash) <!-- [locale](./0002.%20crypto%20%E6%A8%A1%E5%9D%97%E4%B8%AD%E7%9A%84%20hash%20%E5%B7%A5%E5%85%B7%E6%96%B9%E6%B3%95%20createHash/README.md) -->

生成唯一标识符：
在需要生成唯一标识符的场景下，使用字符串的十六进制表示形式可以确保唯一性。
例如，可以用它来生成基于字符串的哈希值或标识符。

数据加密与安全：
将字符串转换为十六进制是某些加密算法中的一步。
通过将数据转换为十六进制，可以便于进一步的加密或编码操作。

数据序列化与传输：
在某些情况下，将数据以十六进制形式表示并进行传输，可以避免因为字符编码问题导致的数据损坏。
例如，网络传输、数据库存储等。

调试与日志记录：
在调试过程中，查看数据的十六进制表示形式有助于分析和理解数据的底层结构，特别是在处理二进制数据或非可见字符时。

字符串混淆：
可以用来混淆字符串，使其在人类可读的形式上更加难以理解。
例如，用于生成配置文件或代码中的某些敏感信息。

生成配置文件变量名：

在 Vben 中，strToHex 函数被用来生成配置文件的变量名。
Vben：https://github.com/vbenjs/vue-vben-admin

将应用程序标题转换为十六进制字符串，以确保变量名的唯一性和不可预测性：

```js
const getVariableName = (title) => {
  return `__PRODUCTION__${strToHex(title) || '__APP'}__CONF__`.toUpperCase().replace(/\s/g, '');
};
```

<!-- !====================>分隔符<====================! -->
### [0003. 使用 npm_lifecycle_script 获取当前运行的 nodejs 命令](https://github.com/Tdahuyou/nodejs/tree/main/0003.%20%E4%BD%BF%E7%94%A8%20npm_lifecycle_script%20%E8%8E%B7%E5%8F%96%E5%BD%93%E5%89%8D%E8%BF%90%E8%A1%8C%E7%9A%84%20nodejs%20%E5%91%BD%E4%BB%A4) <!-- [locale](./0003.%20%E4%BD%BF%E7%94%A8%20npm_lifecycle_script%20%E8%8E%B7%E5%8F%96%E5%BD%93%E5%89%8D%E8%BF%90%E8%A1%8C%E7%9A%84%20nodejs%20%E5%91%BD%E4%BB%A4/README.md) -->

- npm_lifecycle_script 是什么
- npm_lifecycle_script 有啥用


<!-- !====================>分隔符<====================! -->
### [0004. 学会使用 nodejs 运行 .js 文件](https://github.com/Tdahuyou/nodejs/tree/main/0004.%20%E5%AD%A6%E4%BC%9A%E4%BD%BF%E7%94%A8%20nodejs%20%E8%BF%90%E8%A1%8C%20.js%20%E6%96%87%E4%BB%B6) <!-- [locale](./0004.%20%E5%AD%A6%E4%BC%9A%E4%BD%BF%E7%94%A8%20nodejs%20%E8%BF%90%E8%A1%8C%20.js%20%E6%96%87%E4%BB%B6/README.md) -->

- 视频：✅


<!-- !====================>分隔符<====================! -->
### [0005. 获取 macos 下都安装了哪些应用](https://github.com/Tdahuyou/nodejs/tree/main/0005.%20%E8%8E%B7%E5%8F%96%20macos%20%E4%B8%8B%E9%83%BD%E5%AE%89%E8%A3%85%E4%BA%86%E5%93%AA%E4%BA%9B%E5%BA%94%E7%94%A8) <!-- [locale](./0005.%20%E8%8E%B7%E5%8F%96%20macos%20%E4%B8%8B%E9%83%BD%E5%AE%89%E8%A3%85%E4%BA%86%E5%93%AA%E4%BA%9B%E5%BA%94%E7%94%A8/README.md) -->

本文介绍了类似 rubick 这样的效率工具，是如何实现本地应用快速检索并启动的。


<!-- !====================>分隔符<====================! -->
### [0006. 使用 screencapture 命令实现 macos 系统截图](https://github.com/Tdahuyou/nodejs/tree/main/0006.%20%E4%BD%BF%E7%94%A8%20screencapture%20%E5%91%BD%E4%BB%A4%E5%AE%9E%E7%8E%B0%20macos%20%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE) <!-- [locale](./0006.%20%E4%BD%BF%E7%94%A8%20screencapture%20%E5%91%BD%E4%BB%A4%E5%AE%9E%E7%8E%B0%20macos%20%E7%B3%BB%E7%BB%9F%E6%88%AA%E5%9B%BE/README.md) -->

本文介绍如何在 macOS 上使用 screencapture 命令来实现截图功能。


<!-- !====================>分隔符<====================! -->
### [0007. crypto 模块](https://github.com/Tdahuyou/nodejs/tree/main/0007.%20crypto%20%E6%A8%A1%E5%9D%97) <!-- [locale](./0007.%20crypto%20%E6%A8%A1%E5%9D%97/README.md) -->

- ⏰ TODO

<!-- !====================>分隔符<====================! -->
### [0008. koa-send](https://github.com/Tdahuyou/nodejs/tree/main/0008.%20koa-send) <!-- [locale](./0008.%20koa-send/README.md) -->

- ⏰ TODO

<!-- !====================>分隔符<====================! -->
### [0009. koa-static](https://github.com/Tdahuyou/nodejs/tree/main/0009.%20koa-static) <!-- [locale](./0009.%20koa-static/README.md) -->

- ⏰ TODO

<!-- !====================>分隔符<====================! -->
### [0010. npm 生命周期 prepublish](https://github.com/Tdahuyou/nodejs/tree/main/0010.%20npm%20%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%20prepublish) <!-- [locale](./0010.%20npm%20%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F%20prepublish/README.md) -->

新建一个 [1.js](./1.js) 模块，内容如下：

```js
console.log('call 1.js')
```

新建一个 [package.json](./package.json) 模块，内容如下：

```json
{
  "name": "demo",
  "version": "1.0.0",
  "scripts": {
    "prepublish": "node 1.js"
  },
  "dependencies": {
    "lodash": "^4.17.21"
  }
}
```

执行 `npm i` 安装依赖。（如果存在 node_modules，将其删除后再执行 npm i）

会发现 prepublish 中配置的命令 `node 1.js` 自动执行了，`1.js` 执行后输出了 `call 1.js`。

![](md-imgs/2024-09-20-15-19-24.png)

# 🤖 AI


<!-- !====================>分隔符<====================! -->
### [0011. npm 配置文件 .npmrc](https://github.com/Tdahuyou/nodejs/tree/main/0011.%20npm%20%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%20.npmrc) <!-- [locale](./0011.%20npm%20%E9%85%8D%E7%BD%AE%E6%96%87%E4%BB%B6%20.npmrc/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0012. 使用 nrm 管理 npm 源](https://github.com/Tdahuyou/nodejs/tree/main/0012.%20%E4%BD%BF%E7%94%A8%20nrm%20%E7%AE%A1%E7%90%86%20npm%20%E6%BA%90) <!-- [locale](./0012.%20%E4%BD%BF%E7%94%A8%20nrm%20%E7%AE%A1%E7%90%86%20npm%20%E6%BA%90/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0013. 安装 nodejs](https://github.com/Tdahuyou/nodejs/tree/main/0013.%20%E5%AE%89%E8%A3%85%20nodejs) <!-- [locale](./0013.%20%E5%AE%89%E8%A3%85%20nodejs/README.md) -->

- 视频：✅


<!-- !====================>分隔符<====================! -->
### [0014. 如何使用 nvm 管理 nodejs 版本](https://github.com/Tdahuyou/nodejs/tree/main/0014.%20%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%20nvm%20%E7%AE%A1%E7%90%86%20nodejs%20%E7%89%88%E6%9C%AC) <!-- [locale](./0014.%20%E5%A6%82%E4%BD%95%E4%BD%BF%E7%94%A8%20nvm%20%E7%AE%A1%E7%90%86%20nodejs%20%E7%89%88%E6%9C%AC/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0015. 《深入浅出 Node.js》](https://github.com/Tdahuyou/nodejs/tree/main/0015.%20%E3%80%8A%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BA%20Node.js%E3%80%8B) <!-- [locale](./0015.%20%E3%80%8A%E6%B7%B1%E5%85%A5%E6%B5%85%E5%87%BA%20Node.js%E3%80%8B/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0016. 《Node.js来一打C++扩展》](https://github.com/Tdahuyou/nodejs/tree/main/0016.%20%E3%80%8ANode.js%E6%9D%A5%E4%B8%80%E6%89%93C%2B%2B%E6%89%A9%E5%B1%95%E3%80%8B) <!-- [locale](./0016.%20%E3%80%8ANode.js%E6%9D%A5%E4%B8%80%E6%89%93C%2B%2B%E6%89%A9%E5%B1%95%E3%80%8B/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0017. 《Node与Express开发》](https://github.com/Tdahuyou/nodejs/tree/main/0017.%20%E3%80%8ANode%E4%B8%8EExpress%E5%BC%80%E5%8F%91%E3%80%8B) <!-- [locale](./0017.%20%E3%80%8ANode%E4%B8%8EExpress%E5%BC%80%E5%8F%91%E3%80%8B/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0018. 《Node.js开发指南》](https://github.com/Tdahuyou/nodejs/tree/main/0018.%20%E3%80%8ANode.js%E5%BC%80%E5%8F%91%E6%8C%87%E5%8D%97%E3%80%8B) <!-- [locale](./0018.%20%E3%80%8ANode.js%E5%BC%80%E5%8F%91%E6%8C%87%E5%8D%97%E3%80%8B/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0019. 《了不起的Node js 将JavaScript进行到底》](https://github.com/Tdahuyou/nodejs/tree/main/0019.%20%E3%80%8A%E4%BA%86%E4%B8%8D%E8%B5%B7%E7%9A%84Node%20js%20%E5%B0%86JavaScript%E8%BF%9B%E8%A1%8C%E5%88%B0%E5%BA%95%E3%80%8B) <!-- [locale](./0019.%20%E3%80%8A%E4%BA%86%E4%B8%8D%E8%B5%B7%E7%9A%84Node%20js%20%E5%B0%86JavaScript%E8%BF%9B%E8%A1%8C%E5%88%B0%E5%BA%95%E3%80%8B/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0020. 通过 process.argv 获取脚本的命令行参数](https://github.com/Tdahuyou/nodejs/tree/main/0020.%20%E9%80%9A%E8%BF%87%20process.argv%20%E8%8E%B7%E5%8F%96%E8%84%9A%E6%9C%AC%E7%9A%84%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%8F%82%E6%95%B0) <!-- [locale](./0020.%20%E9%80%9A%E8%BF%87%20process.argv%20%E8%8E%B7%E5%8F%96%E8%84%9A%E6%9C%AC%E7%9A%84%E5%91%BD%E4%BB%A4%E8%A1%8C%E5%8F%82%E6%95%B0/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0021. minimist 基本使用](https://github.com/Tdahuyou/nodejs/tree/main/0021.%20minimist%20%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8) <!-- [locale](./0021.%20minimist%20%E5%9F%BA%E6%9C%AC%E4%BD%BF%E7%94%A8/README.md) -->


<!-- !====================>分隔符<====================! -->
### [0022. 《Node.js 入门教程》（免费掘金小册）](https://github.com/Tdahuyou/nodejs/tree/main/0022.%20%E3%80%8ANode.js%20%E5%85%A5%E9%97%A8%E6%95%99%E7%A8%8B%E3%80%8B%EF%BC%88%E5%85%8D%E8%B4%B9%E6%8E%98%E9%87%91%E5%B0%8F%E5%86%8C%EF%BC%89) <!-- [locale](./0022.%20%E3%80%8ANode.js%20%E5%85%A5%E9%97%A8%E6%95%99%E7%A8%8B%E3%80%8B%EF%BC%88%E5%85%8D%E8%B4%B9%E6%8E%98%E9%87%91%E5%B0%8F%E5%86%8C%EF%BC%89/README.md) -->

- 📝 summary
  - Node.js 0基础入门教程，涵盖了软件的安装，环境配置，基础知识介绍，进阶知识介绍，多场景的开发实践 ღ( ´･ᴗ･` )


<!-- !====================>分隔符<====================! -->
### [0023. npm 内置命令](https://github.com/Tdahuyou/nodejs/tree/main/0023.%20npm%20%E5%86%85%E7%BD%AE%E5%91%BD%E4%BB%A4) <!-- [locale](./0023.%20npm%20%E5%86%85%E7%BD%AE%E5%91%BD%E4%BB%A4/README.md) -->

- 知道什么是 npm 内置命令。
- 对目前（2024年11月6日18:52:37）能查询到的所有内置命令做了一个简单的描述、分类。


<!-- !====================>分隔符<====================! -->
### [9999. template](https://github.com/Tdahuyou/nodejs/tree/main/9999.%20template) <!-- [locale](./9999.%20template/README.md) -->


<!-- !====================>分隔符<====================! -->
