# 亲子打卡 — Agent 规则

## 项目定位
多用户可自定义的亲子任务交互系统，单页 HTML 应用（PWA），支持云端账号同步和多账号切换。

## 怎么跑
- 本地：直接在浏览器打开 `index.html`
- 线上：https://dnf1880-pixel.github.io/learningmap/
- 部署：push master → GitHub Actions 注入 Token → Pages

## 技术栈
- 纯 HTML/CSS/JS，无框架，无外部依赖
- 数据层：localStorage + GitHub Gist API（云端同步）
- 部署：GitHub Actions + Pages，Token 通过 Secrets 注入
- PWA：内联 manifest + Service Worker，支持离线缓存和桌面安装

## 目录与约定
- `index.html` — 唯一源文件（~4380行）
- `icon-192.png` / `icon-512.png` — PWA 桌面图标
- `.github/workflows/deploy.yml` — 自动部署
- 无构建步骤，无 node_modules

## 当前状态
- v3.5：PWA 支持、品牌更名"亲子打卡"、任务生效日期管理器、历史数据保护、代码健壮性修复
- v3.4：多账号切换（家庭多孩各自独立账号）
- 帮助说明页（功能/使用/更新）、首次欢迎引导
- 云端账号系统：注册/登录/登出，密码哈希存储
- Token 占位符 `__GIST_TOKEN__` 由 Actions 部署时替换

## 注意事项
- 严禁在任何命令或回复中暴露 GitHub Token 明文，始终用环境变量引用
- 部署通过 push master → GitHub Actions 自动完成
- 重要功能更新后，先问用户是否要更新版本说明，确认后再写
