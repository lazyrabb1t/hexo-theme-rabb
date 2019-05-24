### 效果

http://blog.lazyrabbit.xyz/

### 关于

基于以下两个主题修改而来

https://github.com/iJinxin/hexo-theme-sky

https://github.com/frostfan/hexo-theme-polarbear

需要文档可以参照这个

https://ijinxin.github.io/blog/2018/10/29/hexo-theme-sky%E6%8C%87%E5%8D%97/

### 使用

下载主题,安装依赖
```
git clone https://github.com/guoxwOvO/hexo-theme-rabb themes/rabb
npm install
npm install hexo-renderer-scss --save
```
修改_config.yml
```
theme: rabb
```
运行
```
hexo s
```

### highlight

代码高亮使用highlight，需要修改_config.yml,禁用默认代码高亮
```
highlight:
  enable: false
  line_number: false
  auto_detect: false
  tab_replace:
```
配色可以到https://highlightjs.org/ 进行选择，选择好之后可以到 https://www.bootcdn.cn/highlight.js/ 找到对应文件进行配置
```
highlightcss: https://cdn.bootcss.com/highlight.js/9.15.6/styles/a11y-dark.min.css
```

### icon

图标可以到iconfont进行选择

https://www.iconfont.cn/
