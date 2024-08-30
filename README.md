# wxapkg-convertor
一个快速将微信小程序.wxapkg代码包转换成多端框架的工具

### 使用命令行解包

~~~
node wuWxapkg.js 跳一跳.wxapkg
~~~

### 关注我
<a href="https://juejin.im/user/2955079655898093">
  <img align="left" alt="大帅搞全栈 | juejin.im" width="21px" src="https://juejin.im/favicon.ico" />
</a>
<a href="https://www.zhihu.com/people/ezshine">
  <img align="left" alt="大帅 | zhihu.com" width="20px" src="https://www.zhihu.com/favicon.ico" />
</a>
<a href="https://space.bilibili.com/422646817">
  <img align="left" alt="大帅ezshine | bilibili.com" width="21px" src="https://www.bilibili.com/favicon.ico" />
</a>

> 请将能成功反编译的wxapkg文件提交到本仓库中，不能反编译的小程序提交issue并附上wxapkg的下载地址。

### changelog

~~~~
2021.01.26

removed convertToTaro
removed convertToUniapp
optimized app size
~~~~

<br />
<br />

### 掘金文章

[一键反编译微信小程序获取源码，并转换为uniapp或taro跨端项目](https://juejin.im/post/6891957219386982408)

### 目录

#### wxapkg文件夹
> 所有wxapkg文件均来自于网络，使用反编译工具即可获得源码。仅供大家学习使用，如非法使用侵犯版权，后果自付。

1. 小程序

- 好多计算器

2. 小游戏

- 跳一跳


#### src文件夹
> 此工具的源码

# 我的学习记录

Node.js是一个流行的JavaScript运行时环境，用于构建服务器端应用程序。在Node.js项目中，有两个非常重要的文件：package.json和package-lock.json。它们在项目的构建、依赖管理、版本控制等方面起着至关重要的作用。下面我们将详细了解这两个文件。
1. package.json文件
package.json文件是Node.js项目的核心配置文件。它包含了项目的元数据、依赖项列表和其他配置信息。以下是package.json文件中常见的字段：

name: 项目的名称。
version: 项目的版本号。
description: 项目的描述。
dependencies: 项目运行所依赖的Node.js包。
devDependencies: 开发过程中所需的包，通常只在开发环境中安装。
通过npm install命令，Node.js会自动解析package.json文件并根据其中的依赖项列表安装所需的包。
2. package-lock.json文件
package-lock.json是一个JSON文件，它记录了安装package.json文件中指定的所有依赖项的确切版本和完整安装路径。这个文件是由npm自动生成的，并在执行npm install时同步更新。
package-lock.json的主要目的是提供一种机制，确保在项目的开发过程中，所有成员使用相同版本的依赖项。这样可以避免因依赖项版本冲突导致的问题。同时，它也使得重新安装依赖项变得更加简单和可靠。
3. package.json与package-lock.json的差异
用途：package.json主要用于配置项目的基本信息和依赖关系，而package-lock.json则用于记录和跟踪依赖项的精确版本。
更新方式：当你在package.json中添加或删除依赖项时，需要运行npm install来更新package-lock.json。而直接编辑package-lock.json文件并不会自动更新依赖项列表。
版本控制：通常情况下，建议将package-lock.json文件纳入版本控制中，以确保团队成员之间使用一致的依赖项版本。而package.json文件则不需要纳入版本控制，因为它是项目的基本配置信息。
4. 如何协同工作
在开发过程中，当你执行npm install命令时，npm会自动解析package.json文件并安装所需的依赖项，同时生成或更新package-lock.json文件。这意味着你可以使用package-lock.json文件来确保项目中的所有成员使用相同版本的依赖项，并避免潜在的版本冲突问题。
如果你需要更新项目的依赖项，可以先编辑package.json文件，然后运行npm install来更新package-lock.json文件。这样可以确保所有依赖项都符合新的要求，并且整个团队使用的是最新和一致的依赖项版本。
总结：在Node.js项目中，package.json和package-lock.json是两个重要的文件，它们分别用于配置项目信息和记录依赖项版本。通过合理地使用这两个文件，可以有效地管理项目的构建、依赖关系和版本控制，从而提高项目的稳定性和可维护性。

## node镜像

```bash
# 查询当前使用的镜像源
npm get registry

# 设置为淘宝镜像源
npm config set registry https://registry.npmmirror.com/

# 还原为官方镜像源
npm config set registry https://registry.npmjs.org/
```

老项目，`registry.npm.taobao.org`替换为`registry.npmmirror.com`