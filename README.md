<div align="center">

# xCodex

**面向真实工程工作流的桌面 AI 编码工作台**

[官网](https://xcodex.app) • [文档](#) • [下载](#) • [English](./README_EN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)]()
[![Version](https://img.shields.io/badge/version-0.1.0-green)]()

</div>

---

## 🎯 什么是 xCodex？

**xCodex** 不是又一个 AI 聊天界面 — 它是一个**生产级桌面工作台**，将 `工作区 / 线程 / 终端 / Git / 任务 / 诊断` 统一到一个持久化的本地应用中。

为需要的不仅仅是一次性聊天窗口的开发者而构建，xCodex 将 AI 辅助编码从一次性体验转变为**可持续、可恢复、可扩展的工程工作流**。

### 为什么选择 xCodex？

- **🔄 统一工作流**：不再在浏览器标签、终端、文件管理器和任务跟踪器之间反复切换。一切都在一个桌面工作区中。
- **🏗️ 为真实工程而生**：直接集成本地代码仓库、原生 PTY 终端、Git 变更管理和真实的 `codex app-server` 会话 — 不是网页 UI 的克隆。
- **💾 持久化与可恢复**：工作区持久化、线程恢复/续跑/分叉、发送失败恢复、会话状态跟踪。为日常使用而构建，而非演示。
- **🎛️ 高级控制面**：Provider/Supplier 路由、xLLM 适配、插件市场、Symphony 任务编排 — 全部集成，而非散落在外部脚本中。

---

## ✨ 核心功能

### 1. **工作区与线程管理**
- 创建、命名、置顶和持久化本地工作区
- 连接/重连到 `codex app-server` 会话
- 浏览最近线程、继续对话、创建新线程
- 导入、重命名、置顶、归档和分叉线程
- 按工作区设置默认 Provider/Profile，支持线程级路由

### 2. **编码执行工作台**
- 流式展示实时 assistant 输出
- 处理权限审批和运行时反馈
- 集成 `状态 / 历史 / 变更 / 终端 / 待办` 侧边栏
- 原生 PTY 终端执行命令
- Git 变更查看器，支持暂存/取消暂存、提交信息生成和提交操作
- 实验性的分离终端/会话恢复

### 3. **运行时诊断与运营**
- 查看账户、运行时、路由、使用量和速率限制状态卡片
- 自定义 `codex` 二进制路径并执行 doctor 检查
- 诊断中心查看插件运行时和恢复信息
- 跟踪会话阶段、恢复状态和异常信号

### 4. **Symphony 任务编排**
- 在工作区中直接查看 Symphony root/work unit/run/retry 状态
- 打开 work unit 线程继续处理
- 任务面板显示 todo/优先级/工作流状态
- 通过子线程中的 workpad、blocker 和 link 维护任务真相

### 5. **扩展与 AI 生态**
- 管理 Provider/Supplier 配置
- 从市场来源浏览、安装和切换插件
- 管理状态卡片插件布局和运行时快照
- 为 commit message、ClawBot 等内部辅助任务配置独立的 Provider/Supplier/Model 路由
- 实验性桌面功能，如 Dynamic Island

### 6. **浏览器集成** *(最新)*
- 应用内浏览器，支持自动化能力
- Browser-use 集成，用于网页交互任务
- 截图捕获和网页数据提取
- 无缝的浏览器会话状态跟踪

---

## 🛠️ 技术栈

| 层级 | 技术 |
|-------|-----------|
| **前端** | Next.js 16 + React 19 + TypeScript |
| **桌面外壳** | Tauri 2 |
| **后端** | Rust + Tokio |
| **协议** | `codex app-server` JSON-RPC over stdio |
| **终端** | `portable-pty` + `xterm.js` |
| **数据库** | SQLite (sqlx) |
| **AI 辅助任务** | 复用用户配置的 Provider/Supplier/Model 路由 |

---

## 🚀 快速开始

### 前置要求

- Node.js (v18+)
- pnpm
- Rust 工具链
- 本地 `codex` 安装（或在设置中指定自定义二进制路径）

### 安装

```bash
# 克隆仓库
git clone https://github.com/citizenll/xcodex-app.git
cd xcodex-app

# 安装依赖
pnpm install

# 启动桌面开发环境
pnpm tauri dev
```

### 生产构建

```bash
# 构建桌面应用
pnpm tauri build

# 运行验证测试
pnpm typecheck
pnpm build
cargo check --manifest-path src-tauri/Cargo.toml
pnpm smoke:logic
pnpm smoke:release
```

---

## 🎨 设计哲学

xCodex 采用**终端优先美学**，遵循 TUI（文本用户界面）原则：

- **语义化终端配色方案**：绿色表示成功，琥珀色表示警告，青色表示信息，红色表示错误
- **字体**：JetBrains Mono（等宽和无衬线变体）
- **极简约束**：无大圆角、无阴影、无渐变，仅使用 1px 实线边框

这种设计确保了无干扰、以开发者为中心的体验，与您的编码环境原生融合。

---

## 👥 谁应该使用 xCodex？

xCodex 最适合：

- **高频 Codex 用户**：每天使用 AI 编码工具的个人开发者或技术负责人
- **多仓库管理者**：需要同时处理多个本地仓库、线程和运行时状态的人
- **工程团队**：希望将 AI 编码从"聊天工具"升级为"可操作的工程工作台"的团队
- **高级用户**：需要 Symphony、插件、Provider 路由和 xLLM 等高级控制面的用户

---

## 🗺️ 路线图

- [ ] 增强的入门引导和默认配置推荐
- [ ] 自动更新、版本回滚、崩溃报告
- [ ] 许可、订阅和隐私文档
- [ ] 多平台安装程序（Windows、macOS、Linux）
- [ ] 插件 SDK 和开发者文档
- [ ] 工作区/线程状态的云同步（可选）
- [ ] 团队协作功能

---

## 📦 项目结构

```
app/                    # Next.js app router 页面
components/             # React 组件
  workspace-chat/       # 主聊天界面
  composer-next/        # 富文本编辑器
  ui/                   # 可复用 UI 原语
hooks/                  # React hooks
lib/                    # 共享工具
  desktop-api.ts        # Tauri 命令包装器
  composer-next/        # 编辑器文档模型
src-tauri/              # Rust 后端
  src/
    app_server.rs       # 工作区会话管理
    terminal.rs         # PTY 管理
    symphony/           # 任务编排
    browser_use.rs      # 浏览器集成
docs/superpowers/specs/ # 功能规格
tools/                  # 构建和测试脚本
```

---

## 🤝 贡献

我们欢迎贡献！请查看我们的[贡献指南](#)了解详情。

---

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件。

---

## 🔗 链接

- **官网**：[xcodex.app](https://xcodex.app)
- **文档**：[docs.xcodex.app](#)
- **GitHub**：[github.com/citizenll/xcodex-app](https://github.com/citizenll/xcodex-app)
- **问题反馈**：[报告 bug 或请求功能](https://github.com/citizenll/xcodex-app/issues)

---

<div align="center">

**由开发者用 ❤️ 为开发者打造**

如果您觉得 xCodex 有用，请考虑在 GitHub 上给它一个 ⭐️！

</div>
