# git-practice · KingDream 的 Git 练习

**在线演示**: https://q2730970347.github.io/git-practice/

![概览](./assets/概览.png)

> 多练就能会。

新手友好的 Git 交互式入门中文教程，帮助理解 Git 的「四个区域」是如何联动的。本项目基于 [woyeyao/Git-Interactive-Tutorial](https://github.com/woyeyao/Git-Interactive-Tutorial)（MIT 协议）定制而来。

## 功能特点

- **4 区可视化** — Working Directory / Staging Area / Local Repo / Remote Repo 实时展示文件状态变化
- **模拟终端** — 支持 21 个 git 命令 + 辅助命令（touch、echo、cat、help），教学友好的错误提示
- **命令补全** — 输入 `git ad` 后按 `Tab` 自动补全为 `git add`
- **命令历史** — 上下方向键快速调出历史命令
- **箭头动画** — 命令执行后永久显示对应的数据流向箭头
- **结构化教程** — 8 章 34 张卡片，从基础到进阶，每张卡片带动手任务
- **进度保存** — 自动保存到 localStorage，刷新不丢失
- **零依赖** — 纯 HTML/CSS/JS，无需构建工具、无需服务器

## 快速开始

直接双击 `index.html` 在浏览器中打开即可。

跟随左侧教程卡片，在右侧终端中输入命令，观察上方 4 个区域的变化。

## 教程目录

| 章节 | 内容 |
|------|------|
| 1. Git 是什么 | 对象模型、四个区域 |
| 2. 初始化与配置 | git init、git config、创建文件 |
| 3. 日常基础 | add、status、commit、diff、log |
| 4. 分支操作 | branch、checkout、switch、merge |
| 5. 远程协作 | SSH Key、clone、push、pull、fetch |
| 6. 撤销与修正 | reset、revert、restore |
| 7. 进阶工具 | rebase、stash、cherry-pick、tag、rm |
| 8. 工作流总览 | 日常流程、Git Flow、常见问题 |

## 部署到 GitHub Pages

1. 在 GitHub 新建仓库 `git-practice`
2. 推送代码：`git init && git add . && git commit -m "init" && git branch -M main && git remote add origin https://github.com/q2730970347/git-practice.git && git push -u origin main`
3. 在仓库 `Settings → Pages` 中，将 Source 设为 `main` 分支根目录
4. 等待部署完成，访问 `https://q2730970347.github.io/git-practice/`

## 项目结构

```
├── index.html          # 入口页面
├── style.css           # 全部样式
└── js/
    ├── app.js          # 入口、事件绑定、渲染编排
    ├── state.js        # GitState 核心状态管理
    ├── commands.js     # 所有命令 handler
    ├── parser.js       # 命令解析与分发
    ├── renderer.js     # 区域渲染、箭头动画、终端输出
    └── tutorials.js    # 教程卡片数据（8 章 34 张）
```

## 技术栈

- 纯 HTML / CSS / JS，无框架、无构建工具
- Google Fonts（Inter + JetBrains Mono）
- SVG 箭头动画
- localStorage 持久化

## License


