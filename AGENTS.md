# 学习地图 — Agent 规则

## 项目定位
三年级学生暑假作业打卡互动地图，单页 HTML 应用，支持云端账号同步（GitHub Gist）。

## 怎么跑
- 本地：直接在浏览器打开 `index.html`
- 线上：https://dnf1880-pixel.github.io/learningmap/
- 部署：push master → GitHub Actions 注入 Token → Pages

## 技术栈
- 纯 HTML/CSS/JS，无框架，无外部依赖
- 数据层：localStorage + GitHub Gist API（云端同步）
- 部署：GitHub Actions + Pages，Token 通过 Secrets 注入

## 目录与约定
- `index.html` — 唯一源文件（~3000行）
- `.github/workflows/deploy.yml` — 自动部署
- 无构建步骤，无 node_modules

## 当前状态
- v3.2：toolbar 统一 UI，登录状态与备份恢复同一排
- 云端账号系统：注册/登录/登出，密码哈希存储
- Token 占位符 `__GIST_TOKEN__` 由 Actions 部署时替换

## 下一步
- 功能稳定，等待用户反馈
