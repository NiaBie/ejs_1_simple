# 说明

使用ejs写的hexo主题,最小化美化

# 功能

1. 代码块渲染

<div align="center">
  <img width="500px" src="https://github.com/hexo-simple-theme/theme_demo/blob/master/code.png"> 
</div>

2. 本地搜索(需要`hexo-generator-search`npm包)

<div align="center">
  <img width="500px" src="https://github.com/hexo-simple-theme/theme_demo/blob/master/search.png"> 
</div>

3. 高仿`bootstrap`附加导航

<div align="center">
  <img width="700px" src="https://github.com/hexo-simple-theme/theme_demo/blob/master/guide.png"> 
</div>

4. 可切换`mathjax`和`katex`数学公式渲染

<div align="center">
  <img width="500px" src="https://github.com/hexo-simple-theme/theme_demo/blob/master/latex.png"> 
</div>

# 文件组织

```
/-+-layout/-+-partial/-+-archive.ejs:归档页面
  |         |          |
  |         |          +-head.ejs:浏览器标签栏名,引入search模块
  |         |          |
  |         |          +-header.ejs:网站名,tag+category索引板块
  |         |          |
  |         |          +-latex.ejs:加载mathjax或katex的一些脚本
  |         |          |
  |         |          +-paginator.ejs:前后翻页,跳转顶/底部(部分浏览器无效)
  |         |          |
  |         |          +-post.ejs:显示文章标题,日期和摘要
  |         |          |
  |         |          `-search.ejs:search模块
  |         |
  |         +-archive.ejs:archive页
  |         |
  |         +-category.ejs:category页
  |         |
  |         +-index.ejs:主页
  |         |
  |         +-layout.ejs:通用模板
  |         |
  |         +-post.ejs:post内容页
  |         |
  |         `-tag.ejs:tag页
  |
  +-source/-+-css/-+-block.styl阴影块样式
  |         |      |
  |         |      +-code_normal.styl代码块样式
  |         |      |
  |         |      +-font.styl字体样式
  |         |      |
  |         |      +-paper.styl:文章内容样式
  |         |      |
  |         |      +-style.styl:总样式,颜色定义
  |         |      |
  |         |      `-tool.styl:侧边工具块样式
  |         |
  |         `-js/-+-change.js:调整块大小,透明度,实现附加导航的实时变化
  |               |
  |               +-filter.js:区分普通表格和代码块
  |               |
  |               +-guide.js:初始化附加导航
  |               |
  |               +-highligh.js:优化代码块解析(本精简版主题用不上)
  |               |
  |               +-load.js:初始化本地搜索
  |               |
  |               `-search.js:实现本地搜索
  |
  `-_config.yml:一些主题变量的声明(live2d在此精简版中无效)
```

# 优化版

[hexo_ejs](https://github.com/hexo-simple-theme/hexo_ejs)
