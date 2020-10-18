[toc]

### 启动项目
> github: https://github.com/shilan96/ali-cli.git

```bash
# 初始化 package
npm init

# 初始化 git
git init

# 删除本地仓库
find . -name ".git" | xargs rm -Rf

# 登录 npm
npm login

# 发布 npm
npm publish
```
[npm发包、撤销包](https://www.cnblogs.com/penghuwan/p/6973702.html)

---

### 相关依赖
- commander （注册命令，读取命令行参数）
- inquirer （问询、交互命令）
- child_process （执行 shell 命令）
- download-git-repo （下载仓库模板）
- chalk （调整控制台字符样式）
- ora （终端加载效果，loading）
- fs-extra （系统fs模块的扩展，文件操作相关工具库 [fs-extra](https://www.jianshu.com/p/d6990a03d610)）
- ProgressPlugin 编译进度
- handlebars 模板引擎
- path
- request

---

### 注意
1. 入口文件
```bash
#! /usr/bin/env node
```

2. package.json
```bash
"bin": {
	"ali": "index.js"
}
```

3. 命令连接到全局
```bash
npm link
```

4. 自定义项目名称 name、版本 version、简介 description

---

### 解释
#### 1. #! /usr/bin/env node
告诉操作系统执行这个脚本的时候使用 node 解释器

#### 2. process
- process.argv 获取用户输入的 命令行参数
- process.exit(1)
- process.cwd()


#### 3. shell 命令

#### 4. require

#### 5. fs
- fs.writeJsonSync
- fs.existsSync
- fs.remove

#### 6. inquirer.prompt(prompts)
```bash
# prompts 参数
prompts = [{
	type: '',
	name: '',
	message: '',
	default: '',
	choices: ['', ''],
}]

const answers = inquirer.prompt(prompts);
```

#### 7. Object.assign()

---

### 问题
#### 1. 拉取仓库模板报错：'git clone' failed with status 128
```bash
# （github域名：用户名/项目名称#分支名）
https://github.com:shilan96/vue-template-demo#master
```


### 参考
[前端如何搭建一个简单的脚手架](https://blog.csdn.net/weixin_33835103/article/details/91430283)

[究竟什么是前端脚手架？](https://www.jianshu.com/p/25ce8cf2e6a7)

