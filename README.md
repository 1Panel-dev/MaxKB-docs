本仓库保存了 [MaxKB 项目]() 的 [官方文档](https://fit2cloud.com/maxkb/docs/)，该文档使用 [MkDocs]() 文档框架下的 [Material for MkDocs]() 主题进行构建。

## 本地开发

### 克隆本仓库
```bash
git clone git@github.com:1Panel-dev/MaxKB-docs.git
```

### 安装依赖
```bash
cd docs
pip install -r requirements/requirements.txt
```

### 修改文档内容
本文档的文档结构定义在 `mkdocs.yml` 文件中，文档的具体内容均在 `docs` 目录中。
```yaml
..........
nav:
- 产品介绍: index.md
    - 系统架构: system_arch.md
    - 安装部署:
        - 在线安装: installation/online_installtion.md
        - 离线安装: installation/offline_installtion.md
    - 快速入门: quick_start.md
    - 功能手册: 
        - 知识库: 
            - 知识库: user_manual/dataset/dataset.md
            - 文档: user_manual/dataset/doclist.md
            - 问题: user_manual/dataset/problem.md
            - 命中测试: user_manual/dataset/hit-testing.md
        - 应用: 
            - 应用: user_manual/app/app.md
            - 概览: user_manual/app/app-view.md
            - 命中测试: user_manual/app/hit-testing.md
            - 对话日志: user_manual/app/log.md
        - 模型管理: user_manual/model/model.md
        - 团队管理: user_manual/team/team.md
    - 开发文档:
        - 开发环境搭建: dev_manual/dev_environment.md
    - 更新日志: changelog.md
    - 联系我们: contact.md

..........
```

文档内容使用 markdown 语法编写，若要添加新的文档，需要先在 `mkdocs.yml` 文件中的 `nav` 部分增加对应章节导航。

### 本地调试文档
```bash
mkdocs serve
```
执行上述命令后，可通过 `http://127.0.0.1:8000` 地址查看生成的文档内容，当修改文档后，页面内容会自动更新。

### 构建文档
```bash
mkdocs build
```

执行上述命令后，会在 `site` 目录下生成文档站点的静态文件，将目录中的内容复制到任意 HTTP 服务器上即可完成文档的部署。

## 帮助完善文档

### Fork 文档仓库
点击仓库右上角的 `fork` 按钮，复制本仓库到自己的 github 账号。

### 克隆 fork 后的仓库
```bash
git clone https://github.com/your-github-account/docs.git
```

### 本地修改并调试

### Push 修改内容到 GitHub 仓库

### 提交 Pull Request 到本仓库
