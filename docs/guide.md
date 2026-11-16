# 使用指南

1. 修改 docs 目录中的 Markdown 文件。
2. 在本地预览并检查页面及链接。
3. 提交修改并推送到 main 分支。
4. 在 Actions 页面查看构建与部署状态。
5. 打开网站检查内容是否更新。

## 常用命令

- `python -m mkdocs serve`：本地预览。
- `python -m mkdocs build --strict`：构建网站并严格检查警告。

## 常见问题

| 现象 | 原因 | 处理方式 |
| --- | --- | --- |
| 页面没有出现在导航中 | mkdocs.yml 的 nav 未添加条目 | 在 nav 中补充文件路径 |
| 构建提示链接警告 | 页面间相对链接写错 | 按 docs 目录内的相对路径修改 |
| Actions 部署失败 | 工作流缺少写入权限 | 检查 workflow 的 permissions 设置 |

## 实践记录

我习惯在修改完文档后先运行 `python -m mkdocs serve`，边看页面边调整措辞和链接。确认无误后再执行严格构建：

```bash
python -m mkdocs build --strict
```

严格模式会把警告当成错误，最初我的页面链接少了 `.md` 后缀，就是靠这一步发现的。推送之后，我会到 Actions 页面确认部署任务变绿，再打开线上地址检查效果。

相关页面：[关于本项目](about.md) | [API 参考](api.md)
