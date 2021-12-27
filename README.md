### 效果

http://blog.lazyrabbit.xyz/

基于以下修改而来

https://github.com/iJinxin/hexo-theme-sky

https://github.com/frostfan/hexo-theme-polarbear

https://github.com/EYHN/hexo-helper-live2d

需要文档也可以参照这个

https://ijinxin.github.io/blog/2018/10/29/hexo-theme-sky%E6%8C%87%E5%8D%97/

### 使用

hexo的安装可参考https://blog.lazyrabbit.xyz/tags/#hexo

作者使用的node版本如下

```shell
[root]# node -v
v12.16.1
[root]# npm -v
6.13.4
```

hexo安装完成后，下载主题并安装依赖

```shell
git clone https://github.com/lazyrabb1t/hexo-theme-rabb.git themes/rabb
npm install
npm install hexo-renderer-scss --save
```

如果```hexo-renderer-sass```安装不成功的话，可以尝试使用cnpm

```shell
# 参考自：https://github.com/tufu9441/maupassant-hexo/issues/225
# 目的是改用cnpm来安装软件
npm install -g cnpm --registry=https://registry.npm.taobao.org
# 目的是直接改npm为淘宝的npm，也为防止某些依赖直接用npm来安装，导致无法顺利安装完成。
npm config set registry https://registry.npm.taobao.org
```

开启live2d

```shell
npm install --save hexo-helper-live2d
# 这里是你的live2d模型，可以根据个人喜好来选择
npm instal live2d-widget-model-hijiki
```

修改_config.yml

```yml
theme: rabb
highlight:
  enable: false
  line_number: false
  auto_detect: false
  tab_replace:
live2d:
  enable: true
  scriptFrom: local
  pluginRootPath: live2dw/
  pluginJsPath: lib/
  pluginModelPath: assets/
  tagMode: true
  debug: false
  model:
    use: live2d-widget-model-hijiki
  display:
    position: right
    width: 150
    height: 300
  mobile:
    show: false
  react:
    opacity: 0.7
```

运行

```shell
hexo s
```

### 自定义

1、代码高亮

配色可以到https://highlightjs.org/ 进行选择，选择好之后可以到 https://www.bootcdn.cn/highlight.js/ 找到对应css文件进行配置

theme/rabb/_config.yml

```
css: https://cdn.bootcss.com/highlight.js/9.15.6/styles/a11y-dark.min.css
```

2、live2d模型选择

https://github.com/xiazeyu/live2d-widget-models

3、icon选择

https://www.iconfont.cn/
