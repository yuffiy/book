ember & cli :kiss: 
========

:sunflower::sunflower: **ember.js** 和 **ember-cli** 的快速指南。

* [ember-cli 安装](https://github.com/yuffiy/book/tree/master/01_ember-cli_install/README.md)
* [ember-cli 与编辑器](https://github.com/yuffiy/book/tree/master/02_ember-cli_editor/README.md)
* [ember-cli 快速熟悉](https://github.com/yuffiy/book/tree/master/03_ember-cli_start/README.md)
* [ember-cli 快速开始](https://github.com/yuffiy/book/tree/master/04_ember-cli_demo/README.md)
* [ember-cli 添加依赖](https://github.com/yuffiy/book/blob/master/05_ember-cli_brocfile/README.md)

## ember.js

首先是要简单的介绍一下，[EmberJS](emberjs.com) 是一个MVC框架，恩。

对于**Ember**，可以说从一开始就开始关注他。那年XX岁，Ember还叫做[Sproutcore](http://sproutcore.org)。Sproutcore是Apple的一个项目，他有两个版本，1.X 和 2.X 。1.X还在，而2.X版本就是Ember的前身。Ember与Sproutcore分家后先改名成了Amber，然后很苦逼的由于这个名字被占用了，就改名成了Ember。

刚开始接触Ember的时候其实我是拒绝的，可以说是一头雾水，不明白这个框架是做什么用的。就好像刚接触nodejs还以为是某个处理dom的类库似的。因为那时候的jQuery很流行，所以就不知不觉的把Ember和JQuery做比较，后来才知道这么做的愚蠢。研究过一段时间的Rails回过头来看才发现，这两库根本就不是一个次元的东西。

同一时间也出了一些其他MVC框架，如[Backbone](http://backbonejs.org)、[Angular](http://angularjs.org)。像《why i choose Ember》之类比较性质的文章在网上能大片大片的看到，继而对这些框架也稍微做了了解。怎么说呢，我不太喜欢Angular在标签里那种写法；Backbone可能有些不能满足需求；而Ember，他太大了，加载有些慢。但是我还是无脑的选择了Ember，很大一个原因是他由**社区**驱动，现在这个开源年代，这么做很靠谱，说不定那天google跪了Angular也就不在了。

要说真正喜欢Ember的原因是因为ES6。Ember是首先使用ES6模块的MVC框架，并且那时候源码也都改成使用ES6的模块。还有一点，RSVP是一个promise库，也是由Ember核心团队的成员开发的。这也是我看好Ember的一个原因，因为真真切切被jQuery的promise摧残过。

可喜可贺**1.13**是Ember 1.X的最后一个版本，下一个版本号是从2.0开始。2.X具备了很多新的和好玩的特性，很令人期待。Canary版本现在已经是2.0，最近正在玩。

## ember-cli

要说到构建项目，那理由可是很充分。不过前端项目也需要构建么？只有简单的css，js，html也需要去构建工具构建？

没错，这都是被逼的。在日常coding中我们确实需要一些工具去辅助，比如版本上线之前的代码压缩，各类coffee、sass、less文件的编译，css、js文件和合并，并且需要监视文件改动自动刷新来保护我们的黄金F5。这些种种过分要求如果都要我们亲自一步步去实现那有点太坑，所以我们需要一个工具。

最早的构建工具可以说是[Grunt](http://gruntjs.com)。他有一些很常用的插件来完成上面说到的那些功能。第一个Ember的工具**Ember App Kit**（EAK）也是用Grunt作为构建工具来构建的。

Grunt之后出现了一些其他工具，如[Gulp](http://gulpjs.com)、[Broccoli](https://github.com/broccolijs/broccoli)。形象的说Gulp是水管，而Broccoli是树。但是不管是什么，他们都有一个共同点，都有各类插件来帮助完成项目的构建。而EAK之后也从Grunt改成了Broccoli。

[ember-cli](http://ember-cli.com) 这个工具从名字就可以轻而易举的理解，他是用命令行来快速构建项目的工具。并且ember-cli也是**官方推荐**的。那为什么要用ember-cli呢？

Ember的项目结构大家都知道，常用的Route、controller、view、modal，根据命名规则和模块化开发下来我们js文件有很多很多。那我们如何要快速创建呢？难道要鼠标点右键新建一个空文件么？使用ember-cli的话就会容易很多，比如我想创建login的controller，那只需要在命令行输入:

```sh
ember g controller login
```

就会自动创建一个模板文件出来，可以说很方便。

值得一提的是，ember-cli使用的是**Broccoli**，所以他支持Broccoli的所有插件。如果你是缩进狂魔，one line style，没有问题，coffee、sass 、emblem这些插件都可以安装使用。

但不光是Broccoli的插件，ember-cli本身有一套插件。像常用的simple-auth、locolstorage adapter等都可以通过命令行直接安装，而不需要做任何的导入。如果你玩的足够666666，你还可以自己做插件。当然，安装插件的方法也会去介绍。

emebr-cli的功能很强大，但是他**还不是足够稳定**，当前版本是0.2.7。

## 运行环境

ember-cli在**各种**平台都能够运行。

下面是在之后的demo中使用的各种环境，编辑器，包:

* ubuntu 15.04
* nodejs 0.12.4
* npm 2.0.1
* emacs 24.0
* ember 1.12
* ember-cli 0.2.7

并且在win下测试通过，能够正常运行。

## Thanks

* [Ember官方网站](http://emberjs.com)
* [Ember中文官网](http://emberjs.cn)
* [ember-cli官网网站](http://ember-cli.com)
* Ember QQ群 298026365
* 私人群 123625217

感谢老大[@towerhe](https://github.com/towerhe)对中文社区的贡献和各位ember coder的支持。

特别感谢[@huangdandan](https://github.com/huangdandan)同学对本文的校验。

如果发现了文内错误或是不合适的地方，强烈欢迎提交PR，Issue，或者给我发邮件[@yuffiy](mailto://yfhj1990@hotmail.com)。
