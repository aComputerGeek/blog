---
layout: post
title: phpStrom
date: 2018-05-14 13:02:49
tags: 工欲善必先利器
---


```
已安装：


4.9
  npm install -g wepy-cli     wepy 全局安装
  brew install axel           命令行下载工具
    axel -n 30 https://repo.continuum.io/archive/Anaconda3-5.1.0-MacOSX-x86_64.pkg
    -n  代表线程
  npm install --global vue-cli   vue 客户端全局安装
  npm i mpvue-simple -g          mpvue-simple



4.16
  Alfred 3.6.1          效率神器

4.20
  liceCap               屏幕录制 gif
  Screenflow            截图 录屏工具

4.21
  CheatSheet            快捷键查看工具

5.14
  brew install zsh-autosuggestions
  source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh

  brew install tig

  brew install ccat

  // 安装hexo

5.24
  export PATH="/Users/cailiang/anaconda3/bin:"$PATH
  conda create -n py2.7 python=2.7
  conda create -n py3.6 python=3.6
  source activate py3.6
  source deactivate

  // swagger
  npm install -g http-server
  wget https://github.com/swagger-api/swagger-editor/releases/download/v2.10.4/swagger-editor.zip
  unzip swagger-editor.zip
  http-server swagger-editor

  git clone https://github.com/swagger-api/swagger-editor.git
  cd swagger-editor
  npm install
  npm run build
  npm start
  // 还有docker 等方式使用

5.29
  atom    ctrl + shift + m  markdown预览
    markdown-preview-plus   增强显示
      支持预览实时渲染。(Ctrl + Shift + M)
      支持Latex公式。(Ctrl + Shift + X)
      先禁用markdown-preview。

    markdown-scroll-sync    同步滚动(对markdown-preview-plus 不生效)
    markdown-image-paste    图片粘贴 （文件目录生成图片） ctrl + v  mac下也是
    language-markdown       代码语法增强
    markdown-table-editor   表格编辑
    markdown-themeable-pdf、pdf-view   pdf导出
        从官网下载phantomjs二进制安装包：http://phantomjs.org/download.html
        解压下载的phantomjs-2.1.1-macosx.zip压缩文件。
        添加index.js文件到解压后的目录。
        将整个目录的内容拷贝到：~/.atom/packages/markdown-themeable-pdf/node_modules/phantomjs-prebuilt，注意目录phantomjs-2.1.1-macosx被重命名为phantomjs-prebuilt
        重启Atom，右键->Markdown to PDF即可，生成的pdf文件在Markdown文件同目录。

        其中index.js文件内容为：
        module.exports = {
          path : __dirname + '/bin/phantomjs'
        }

  6.7
    chrome 插件
      Vue.js devtools
      Octotree
      PageSpeed
      Postman
  6.8
    phpstrom 插件
      Swagger Plugin
      PHP Annotation
      上面这两个插件要一起安装，在项目中安装了zircote/swagger-php组件之后，可以提示swagger注释风格的属性名和属性值的自动完成功能

  7.4
    todoist     代办事项
    Paste 2.3.9 剪切板增强工具
    synergy     两台pc共享鼠标键盘
    mininode    脑图工具
    Tuxera NTFS 2018 让你的Mac支持NTFS
    SnippetLab  临时保存代码
    Beyond Compare  比较文件
    Filezilla     文件传输工具
    ForkLift    代替 Finder
    SSH Shell     ssh工具
    ScreenFlow    屏幕录制

  7.5
    brew install scrcpy   安卓投屏
    brew install Caskroom/cask/android-platform-tools   安装adb
        0x0bda
    https://blog.csdn.net/artwebs/article/details/20716431  未解决安卓设备连接问题

  7.6
    安装 deploy 自动部署脚本
      curl -LO https://deployer.org/deployer.phar
      mv deployer.phar /usr/local/bin/dep
      chmod +x /usr/local/bin/dep

    安装 mac wechat辅助工具
      github地址 https://github.com/TKkk-iOSer/WeChatPlugin-MacOS
      curl -o- -L https://raw.githubusercontent.com/lmk123/oh-my-wechat/master/install.sh | bash -s

  7.7
    brew install qt5
    brew uninstall qt5
    brew install cmake openssl libsodium
    brew uninstall --ignore-dependencies cmake openssl libsodium
    放弃编译安装

```

```
// 重载同名方法
function method(obj, name, fnc){
	var old = obj[name];
	obj[name] = function() {
		console.log(arguments.length + " " + fnc.length);
		if (arguments.length == fnc.length) {
			return fnc.apply(this, arguments);
		} else if (typeof old === "function") {
			return old.apply(this, arguments);
		}
	}
}
var people = {
	values: ["Zhang san", "Li si", "Wang wu"]
};
method(people, "find", function() {
	console.log("无参数");
	return this.values;
})
method(people, "find", function(firstname) {
	console.log("一个参数");
	var ret = [];
	for (var i = 0; i < this.values.length; i++) {
		if (this.values[i].indexOf(firstname) === 0) {
			ret.push(this.values[i])
		}
	}
	return ret;
})
method(people, "find", function(firstname, lastname) {
	console.log("两个参数");
	var ret = [];
	for (var i = 0; i < this.values.length; i++) {
		if (this.values[i] == firstname + " " + lastname) {
			ret.push(this.values[i])
		}
	}
	return ret;
})
console.log(people.find());
console.log(people.find("Zhang"));

```
