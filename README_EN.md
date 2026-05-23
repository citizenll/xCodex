<div align="center">

# xCodex
<p align="center">
  <img src="docs/xcodex-banner.png" alt="xCodex Mobile Connector" width="100%">
</p>
**Desktop AI Coding Workbench for Real Engineering Workflows**

[Website](https://xcodex.app) • [Documentation](#) • [Download](#) • [中文](./README.md)

[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)]()
[![Version](https://img.shields.io/badge/version-0.1.0-green)]()

</div>

---

## 🎯 What is xCodex?

**xCodex** is not just another AI chat interface — it is a **production-grade desktop workbench** that unifies `workspace / thread / terminal / git / task / diagnostics` into a single, persistent local application.

Built for developers who need more than one-off chat windows, xCodex transforms AI-assisted coding from a disposable experience into a **sustainable, recoverable, and extensible engineering workflow**.

### Why xCodex?

- **🔄 Unified Workflow**: Stop context-switching between browser tabs, terminals, file managers, and task trackers. Everything lives in one desktop workspace.
- **🏗️ Built for Real Engineering**: Direct integration with local repositories, native PTY terminals, Git change management, and real `codex app-server` sessions — not a web UI clone.
- **💾 Persistent & Recoverable**: Workspace persistence, thread recovery/resume/fork, send failure recovery, and session state tracking. Built for daily use, not demos.
- **🎛️ Advanced Control Surface**: Provider/Supplier routing, xLLM adaptation, plugin marketplace, Symphony task orchestration — all integrated, not scattered across external scripts.

---

## ✨ Core Features

### 1. **Workspace & Thread Management**
- Create, name, pin, and persist local workspaces
- Connect/reconnect to `codex app-server` sessions
- Browse recent threads, continue conversations, and create new threads
- Import, rename, pin, archive, and fork threads
- Per-workspace default Provider/Profile with thread-level routing

### 2. **Coding Execution Workbench**
- Stream real-time assistant output
- Handle permission approvals and runtime feedback
- Integrated `Status / History / Changes / Terminal / Todo` sidebars
- Native PTY terminal for command execution
- Git change viewer with stage/unstage, commit message generation, and commit actions
- Experimental detached terminal/session recovery

### 3. **Runtime Diagnostics & Operations**
- View account, runtime, routing, usage, and rate limit status cards
- Custom `codex` binary path with doctor checks
- Diagnostic center for plugin runtime and recovery info
- Track session phases, recovery state, and anomaly signals

### 4. **Symphony Task Orchestration**
- View Symphony root/work unit/run/retry status directly in workspace
- Open work unit threads for continued processing
- Task panel with todo/priority/workflow status
- Maintain task truth via workpad, blocker, and link in child threads

### 5. **Extensions & AI Ecosystem**
- Manage Provider/Supplier configurations
- Browse, install, and toggle plugins from marketplace sources
- Manage status card plugin layouts and runtime snapshots
- Dedicated Provider/Supplier/Model routing for internal assistant tasks such as commit messages and ClawBot
- Experimental desktop features like Dynamic Island

### 6. **Browser Integration** *(Latest)*
- In-app browser with automation capabilities
- Browser-use integration for web interaction tasks
- Screenshot capture and web data extraction
- Seamless browser session state tracking

---

## 🎨 Design Philosophy

xCodex embraces a **terminal-first aesthetic** with TUI (Text User Interface) principles:

- **Semantic terminal color palette**: Green for success, amber for warnings, cyan for info, red for errors
- **Typography**: JetBrains Mono (monospace and sans-serif variants)
- **Minimalist constraints**: No large rounded corners, no shadows, no gradients, 1px solid borders only

This design ensures a distraction-free, developer-focused experience that feels native to your coding environment.

---

## 👥 Who Should Use xCodex?

xCodex is ideal for:

- **High-frequency Codex users**: Individual developers or tech leads who use AI coding tools daily
- **Multi-repo managers**: Those juggling multiple local repositories, threads, and runtime states
- **Engineering teams**: Teams wanting to upgrade AI coding from "chat tool" to "operational engineering workbench"
- **Power users**: Users needing advanced control surfaces like Symphony, plugins, Provider routing, and xLLM

---

## 🗺️ Roadmap

- [ ] Enhanced onboarding and default configuration recommendations
- [ ] Auto-update, version rollback, crash reporting
- [ ] Licensing, subscription, and privacy documentation
- [ ] Multi-platform installers (Windows, macOS, Linux)
- [ ] Plugin SDK and developer documentation
- [ ] Cloud sync for workspace/thread state (optional)
- [ ] Team collaboration features

---

## 🔗 Links

- **Website**: [xcodex.app](https://xcodex.app)
- **Documentation**: [docs.xcodex.app](#)
- **GitHub**: [github.com/citizenll/xcodex](https://github.com/citizenll/xcodex)
- **Issues**: [Report a bug or request a feature](https://github.com/citizenll/xcodex/issues)

---

<div align="center">

**Built with ❤️ by developers, for developers**

If you find xCodex useful, please consider giving it a ⭐️ on GitHub!

</div>
