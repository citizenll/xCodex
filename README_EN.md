<div align="center">

# xCodex

**The Desktop AI Coding Workbench for Real Engineering Workflows**

[Website](https://xcodex.app) • [Documentation](#) • [Download](#) • [中文](./README_CN.md)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20macOS%20%7C%20Linux-blue)]()
[![Version](https://img.shields.io/badge/version-0.1.0-green)]()

</div>

---

## 🎯 What is xCodex?

**xCodex** is not just another AI chat interface — it's a **production-grade desktop workbench** that unifies `workspace / thread / terminal / git / task / diagnostics` into a single, persistent local application.

Built for developers who need more than disposable chat windows, xCodex transforms AI-assisted coding from a one-off experience into a **sustainable, recoverable, and extensible engineering workflow**.

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
- Browse recent threads, continue conversations, create new threads
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
- Task panel with todo/priority/workflow state
- Maintain task truth via workpad, blockers, and links in child threads

### 5. **Extensions & AI Ecosystem**
- Manage Provider/Supplier configurations
- Browse, install, and toggle plugins from marketplace sources
- Manage status card plugin layout and runtime snapshots
- Dedicated Provider/Supplier/Model routing for internal assistant tasks such as commit messages and ClawBot
- Experimental desktop features like Dynamic Island

### 6. **Browser Integration** *(Latest)*
- In-app browser with automation capabilities
- Browser-use integration for web interaction tasks
- Screenshot capture and web data extraction
- Seamless browser session state tracking

---

## 🛠️ Technology Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | Next.js 16 + React 19 + TypeScript |
| **Desktop Shell** | Tauri 2 |
| **Backend** | Rust + Tokio |
| **Protocol** | `codex app-server` JSON-RPC over stdio |
| **Terminal** | `portable-pty` + `xterm.js` |
| **Database** | SQLite (sqlx) |
| **Assistant Tasks** | Reuses configured Provider/Supplier/Model routing |

---

## 🚀 Getting Started

### Prerequisites

- Node.js (v18+)
- pnpm
- Rust toolchain
- Local `codex` installation (or specify custom binary path in settings)

### Installation

```bash
# Clone the repository
git clone https://github.com/citizenll/xcodex-app.git
cd xcodex-app

# Install dependencies
pnpm install

# Start desktop development environment
pnpm tauri dev
```

### Build for Production

```bash
# Build desktop application
pnpm tauri build

# Run validation tests
pnpm typecheck
pnpm build
cargo check --manifest-path src-tauri/Cargo.toml
pnpm smoke:logic
pnpm smoke:release
```

---

## 🎨 Design Philosophy

xCodex embraces a **terminal-first aesthetic** with TUI (Text User Interface) principles:

- **Semantic terminal color palette**: Green for success, amber for warnings, cyan for info, red for errors
- **Typography**: JetBrains Mono (mono and sans variants)
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

## 📦 Project Structure

```
app/                    # Next.js app router pages
components/             # React components
  workspace-chat/       # Main chat interface
  composer-next/        # Rich text composer
  ui/                   # Reusable UI primitives
hooks/                  # React hooks
lib/                    # Shared utilities
  desktop-api.ts        # Tauri command wrappers
  composer-next/        # Composer document model
src-tauri/              # Rust backend
  src/
    app_server.rs       # Workspace session management
    terminal.rs         # PTY management
    symphony/           # Task orchestration
    browser_use.rs      # Browser integration
docs/superpowers/specs/ # Feature specifications
tools/                  # Build and test scripts
```

---

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](#) for details.

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🔗 Links

- **Website**: [xcodex.app](https://xcodex.app)
- **Documentation**: [docs.xcodex.app](#)
- **GitHub**: [github.com/citizenll/xcodex-app](https://github.com/citizenll/xcodex-app)
- **Issues**: [Report a bug or request a feature](https://github.com/citizenll/xcodex-app/issues)

---

<div align="center">

**Built with ❤️ by developers, for developers**

If you find xCodex useful, please consider giving it a ⭐️ on GitHub!

</div>
