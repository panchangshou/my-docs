# 我的技术文档

第二次 GitHub 作业：基于 MkDocs 构建的静态文档站点，账号为 `panchangshou`，仓库为 `my-docs`，通过 GitHub Actions 自动部署到 GitHub Pages。

## 目录结构

```text
my-docs/
├── .github/
│   └── workflows/
│       └── deploy.yml
├── docs/
│   ├── index.md
│   ├── about.md
│   ├── guide.md
│   └── api.md
├── report/
│   ├── README.md
│   └── images/
├── mkdocs.yml
├── requirements.txt
├── .gitignore
└── README.md
```

## 本地运行

```bash
pip install -r requirements.txt
python -m mkdocs serve
```

默认访问地址：`http://127.0.0.1:8000`

## 构建

```bash
python -m mkdocs build --strict
```

构建结果输出到 `site/` 目录。

## 部署

推送到 `main` 分支后，GitHub Actions 会自动构建并发布到 `gh-pages` 分支。请确保仓库的 Pages 设置使用 `gh-pages` 分支作为发布来源。
