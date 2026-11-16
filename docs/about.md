# 关于本项目

## 项目目标

实现从 Markdown 文档到公开网站的自动化发布。

## 技术组成

| 工具 | 作用 |
| --- | --- |
| Markdown | 编写文档内容 |
| MkDocs Material | 将文档构建成静态网站 |
| GitHub Actions | 自动执行安装、构建和部署 |
| GitHub Pages | 托管并提供网站访问地址 |

## 我的理解

选择静态文档站点作为实践主题，是因为它的流程完整又不依赖后端：源文件是纯文本，版本控制由 Git 负责，构建和发布交给 GitHub Actions，最终产物由 GitHub Pages 托管。整条链路没有数据库和服务器，出了问题也容易定位——先看 Markdown 是否写对，再看 mkdocs.yml 配置，最后看 Actions 日志。

对我来说，这个项目还有一个实际价值：把课程笔记、接口说明和操作步骤集中到一个随时可访问的网站，比散落在本地文件里更方便复习和分享。

## 发布流程

```text
编写 Markdown -> mkdocs build -> 生成 site/ -> GitHub Actions -> GitHub Pages
```

继续阅读：[首页](index.md) | [使用指南](guide.md)
