# NinjaCode MCP Server 🥷

> **Teaching AI Agents to Write Production-Grade, Secure Code**

**A Product of [NinjaMinds](https://ninjaminds.org)**

**Version 2.0.0** - Major release with Help Center, Code Snippets, and Enhanced Dependency Security!

---

## 🎯 What is NinjaCode?

NinjaCode is an MCP (Model Context Protocol) server that acts as your **Code Quality Sensei** - helping AI agents generate high-quality, secure, and maintainable code.

### ✨ New in v2.0.0 (Major Release):

- 🆕 **In-App Help Center** - Searchable help with 15+ topics, FAQs, and video tutorials (Press F1!)
- 🆕 **Code Snippets Library** - 15+ reusable code patterns (auth, API, testing, etc.) via MCP tool
- 🆕 **Enhanced Dependency Scanning** - Automatic package verification with license, funding, and copyright checks
- 🤖 **Copilot Safety Enforcement** - AI agents MUST use only latest safe packages, no vulnerabilities allowed
- 🛡️ **License Compliance** - Automatic detection of GPL/AGPL/proprietary licenses requiring user approval
- 💰 **Funding Transparency** - Package maintainer funding requests surfaced to developers
- ✅ **Auto-Start on Boot** - Desktop app starts automatically in system tray
- 📚 **Comprehensive Documentation** - Step-by-step guides for every feature

### Features:

#### Core Features (Local & Enterprise)
- **🔐 Secret Scanning** - Detect and prevent hardcoded secrets (AWS keys, API tokens, passwords, etc.)
- **🛡️ Vulnerability Detection** - Find and fix security issues following OWASP guidelines
- **📊 Code Quality Analysis** - Enforce clean code principles, detect code smells
- **🏗️ Architecture Guidance** - 12-Factor App compliance validation
- **📁 Structure Templates** - Best practice folder structures for any project type
- **📚 Best Practices** - Language-specific idioms and patterns
- **📦 Enhanced Dependency Scanning** - Automatic verification against security databases with license/funding/copyright checks (NEW in v2.0.0)
- **🔒 Compliance Checking** - GDPR, SOC2, HIPAA, PCI-DSS compliance validation
- **⚡ Performance Analysis** - Detect N+1 queries, memory leaks, and performance issues
- **📝 Code Snippets** - 15+ production-ready patterns for auth, API, testing, and more (NEW in v2.0.0)
- **❓ In-App Help** - Searchable help center with tutorials and FAQs (NEW in v2.0.0)

#### Enterprise Features (Server Mode)
- **👥 User Management** - Role-based access control (RBAC)
- **🏢 Organization Settings** - Centralized policy management
- **📋 Audit Logging** - Complete audit trail of all actions
- **📊 Analytics Dashboard** - Usage analytics and reporting
- **🔐 Multi-tenancy** - Support for multiple organizations
- **🌐 RESTful API** - Programmatic access and integrations
- **⚙️ Custom Policies** - Organization-specific coding rules

---

## 📥 Download

Download the signed executables **only** from the official NinjaMinds channels:

1. 🌐 Primary: [ninjaminds.org/downloads](https://ninjaminds.org/downloads)
2. 📦 Mirror: [github.com/OBEDPoP/NinjaCode-MCP/releases](https://github.com/OBEDPoP/NinjaCode-MCP/releases)

| Platform | ninjaminds.org | GitHub Releases |
|----------|----------------|-----------------|
| Windows | [Download](https://ninjaminds.org/downloads#ninjacode-windows) | [Download](https://github.com/OBEDPoP/NinjaCode-MCP/releases/latest/download/ninjacode-win.exe) |
| macOS | [Download](https://ninjaminds.org/downloads#ninjacode-macos) | [Download](https://github.com/OBEDPoP/NinjaCode-MCP/releases/latest/download/ninjacode-macos) |
| Linux | [Download](https://ninjaminds.org/downloads#ninjacode-linux) | [Download](https://github.com/OBEDPoP/NinjaCode-MCP/releases/latest/download/ninjacode-linux) |

**No Node.js or dependencies required!** Just download and configure with your IDE.

---

## 🚀 Quick Start

1. **Download** the executable for your platform
2. **Double-click** the exe to see setup instructions for your IDE
3. **Configure** your IDE with the path to the executable
4. **Start coding** with AI-powered code quality guidance!

---

## ⚙️ IDE Configuration

> **Note:** You do NOT need to keep the server running manually. Your IDE starts it automatically in the background when needed.

### ✅ Recommended: Per-Project Setup (Works in ALL IDEs)

**This is the best approach!** Create `.vscode/mcp.json` in your project root - it works automatically for anyone who opens the project.

**Windows:**
```jsonc
{
  "servers": {
    "ninjacode": {
      "command": "C:\\Users\\YourName\\Downloads\\ninjacode-win.exe"
    }
  }
}
```

**macOS/Linux:**
```jsonc
{
  "servers": {
    "ninjacode": {
      "command": "/Users/yourname/Downloads/ninjacode-macos"
    }
  }
}
```

**Benefits:**
- ✅ Works for your entire team (commit to Git)
- ✅ Works in VS Code, Cursor, Windsurf, etc.
- ✅ No manual IDE configuration needed
- ✅ Project is portable across machines

<details>
<summary><b>🔧 Advanced: Developing from source?</b></summary>

If you're building NinjaCode from source with Node.js:

```jsonc
{
  "servers": {
    "ninjacode": {
      "command": "node",
      "args": ["dist/bundle.cjs"],
      "cwd": "${workspaceFolder}"
    }
  }
}
```

</details>

---

### Alternative: Global Settings (All Projects)

If you want NinjaCode available in **every project** you open:

### 🔷 VS Code (GitHub Copilot)

**File:** `%APPDATA%\Code\User\settings.json` (Windows) or `~/.config/Code/User/settings.json` (Linux/Mac)

```json
{
  "mcp.servers": {
    "ninjacode": {
      "command": "C:\\path\\to\\ninjacode-win.exe"
    }
  }
}
```

### 🟣 Cursor

**File:** `%APPDATA%\Cursor\User\settings.json` (Windows)

```json
{
  "mcp.servers": {
    "ninjacode": {
      "command": "C:\\path\\to\\ninjacode-win.exe"
    }
  }
}
```

### 🌊 Windsurf (Codeium)

**File:** `%APPDATA%\Windsurf\User\settings.json` (Windows)

```json
{
  "mcp.servers": {
    "ninjacode": {
      "command": "C:\\path\\to\\ninjacode-win.exe"
    }
  }
}
```

### 🟠 Claude Desktop

**File:** `%APPDATA%\Claude\claude_desktop_config.json` (Windows) or `~/Library/Application Support/Claude/claude_desktop_config.json` (Mac)

```json
{
  "mcpServers": {
    "ninjacode": {
      "command": "C:\\path\\to\\ninjacode-win.exe"
    }
  }
}
```

### 🔵 Zed

**File:** `~/.config/zed/settings.json`

```json
{
  "context_servers": {
    "ninjacode": {
      "command": {
        "path": "/path/to/ninjacode-linux"
      }
    }
  }
}
```

### ⚫ Continue (VS Code / JetBrains Extension)

**File:** `~/.continue/config.json`

```json
{
  "experimental": {
    "modelContextProtocolServers": [
      {
        "transport": {
          "type": "stdio",
          "command": "C:\\path\\to\\ninjacode-win.exe"
        }
      }
    ]
  }
}
```

### 🟤 Cline (VS Code Extension)

Open Cline settings in VS Code and add MCP server with command:
```
C:\path\to\ninjacode-win.exe
```

---

## 🌐 “Remote Version” (No Enterprise Server Needed)

If you’re using the public NinjaCode MCP from `ninjacode.ninjaminds.org`, that’s for **downloads/docs**. MCP in VS Code/Cursor/Windsurf is **stdio-based** today, meaning your IDE must start a **local process** (`ninjacode-win.exe` or `node dist/bundle.cjs`).

- ✅ **Remote/public use case**: download the signed executable and configure your IDE to run it locally.
- ❌ **Not supported in VS Code** (yet): setting MCP to a URL like `https://ninjacode.ninjaminds.org` as the server.

The separate **Enterprise Server Mode** (`mcp-server/`) is only for organizations that want centralized policies, user management, and a database-backed admin API.

---

## 🤖 Enable Automatic Enforcement

By default, NinjaCode tools are available to AI agents but require explicit invocation. To make NinjaCode **automatically guide your AI on every request**, add instructions to your project:

### Step 1: Copy the Instructions Template

Copy the template to your project's `.github` folder:

```powershell
# Windows PowerShell
New-Item -ItemType Directory -Force -Path "C:\path\to\your\project\.github" | Out-Null
Copy-Item "templates\copilot-instructions-template.md" "C:\path\to\your\project\.github\copilot-instructions.md" -Force
```

```bash
# macOS/Linux
mkdir -p /path/to/your/project/.github
cp templates/copilot-instructions-template.md /path/to/your/project/.github/copilot-instructions.md
```

Or manually create `.github/copilot-instructions.md` in your project with content from:
`templates/copilot-instructions-template.md`

### Step 2: Restart VS Code

VS Code reads `.github/copilot-instructions.md` at startup and injects it into Copilot's context.

### What Gets Enforced Automatically:

| Scenario | Tool Auto-Used | What's Checked |
|----------|----------------|----------------|
| Writing any code | `analyze_code_quality` | Function length, nesting, code smells |
| Adding credentials/config | `scan_secrets` | Hardcoded secrets, API keys |
| Handling user data | `check_compliance` | GDPR, HIPAA, SOC2, PCI-DSS |
| Adding dependencies | `scan_dependencies` | CVEs, outdated packages |
| Building APIs | `analyze_performance` | N+1 queries, memory leaks |
| New projects | `suggest_folder_structure` | Best practice structure |

### Example: What You'll See

When you ask Copilot to write code, it will automatically analyze and respond:

```
⚠️ NinjaCode Security Analysis

🔴 CRITICAL: Hardcoded API key detected
   → Line 5: const key = "sk-..."
   → Fix: Use process.env.API_KEY instead

🟡 WARNING: Function exceeds 50 lines (72 lines)
   → Consider splitting into smaller functions

✅ PASSED: No SQL injection vulnerabilities
✅ PASSED: Proper error handling present
```

---

## ✅ Verify It’s Working

### Terminal smoke test (Node)

From this repo, you can confirm NinjaCode responds to MCP JSON-RPC over stdio:

```powershell
$init = '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{"protocolVersion":"2024-11-05","capabilities":{},"clientInfo":{"name":"test","version":"1.0"}}}';
$tool = '{"jsonrpc":"2.0","id":2,"method":"tools/call","params":{"name":"scan_secrets","arguments":{"code":"const key = \\\"sk-1234\\\";","language":"javascript"}}}';
echo "$init`n$tool" | node dist/bundle.cjs
```

### IDE test

1. Configure the IDE (per-project `.vscode/mcp.json` or global settings)
2. Restart the IDE
3. Ask Copilot/your agent: “Run NinjaCode `scan_secrets` on this snippet: `const key = "sk-1234";`”
4. Approve the tool call prompt when it appears

---

## 🛠️ Available Tools

| Tool | Description | When to Use |
|------|-------------|-------------|
| `scan_secrets` | Detect hardcoded credentials | Before committing code with config |
| `analyze_code_quality` | Code metrics and smells | During code review |
| `scan_dependencies` | Check for CVEs | When adding/updating packages |
| `check_compliance` | GDPR, HIPAA, SOC2, PCI-DSS | When handling sensitive data |
| `analyze_performance` | N+1 queries, memory leaks | Before deploying to production |
| `suggest_folder_structure` | Best-practice project layout | Starting new projects |
| `get_best_practices` | Language/framework patterns | Learning new tech |
| **`get_code_snippets`** 🆕 | **Reusable code examples** | **Need boilerplate or patterns** |

### 🆕 Code Snippets Tool (NEW in v0.2.0)

Ask your AI assistant to find reusable code examples:

```
"Show me Express.js authentication snippets from NinjaCode"
"Find React hooks examples in NinjaCode"
"Get database transaction patterns from NinjaCode snippets"
```

**Available Categories:**
- 🔐 Auth (JWT, bcrypt, OAuth)
- 🌐 API (REST, GraphQL, validation)
- 💾 Database (transactions, migrations)
- 🧪 Testing (Jest, mocks, fixtures)
- ⚠️ Error Handling (custom errors, middleware)
- ⚡ Performance (caching, memoization)
- 🔒 Security (rate limiting, sanitization)
- 🎨 UI (React hooks, form handling)
- 🛠️ Utilities (logging, config)

### Enterprise Tools (Server Mode)
| Tool | Description |
|------|-------------|
| `check_compliance` | Organization-specific compliance checking with custom policies |
| `enforce_policy` | Enforce organization-specific coding policies |

### Detected Secret Types

- AWS Access Keys & Secret Keys
- GitHub/GitLab Tokens
- Stripe API Keys (Live & Test)
- MongoDB/PostgreSQL Connection Strings
- JWT Tokens
- RSA/SSH Private Keys
- Azure Connection Strings
- Google API Keys
- Slack Tokens
- Generic API Keys & Passwords

---

## 📚 Available Resources

| Resource | Description |
|----------|-------------|
| 12-Factor App | The Twelve-Factor App methodology |
| SOLID Principles | SOLID principles with examples |
| Clean Code | Clean code principles guide |
| Secret Patterns | Secret detection patterns database |

---

## 💬 Available Prompts

| Prompt | Description |
|--------|-------------|
| `code_review` | Comprehensive code review (quality, security, best practices) |
| `security_audit` | OWASP-focused security analysis |
| `refactor_guide` | Step-by-step refactoring recommendations |

---

## 📖 How It Works

```
┌─────────────┐     MCP Protocol     ┌─────────────────┐
│   AI Agent  │ ◄──────────────────► │  NinjaCode MCP  │
│  (Copilot)  │   stdin/stdout       │     Server      │
└─────────────┘                      └─────────────────┘
                                            │
                                     ┌──────┴──────┐
                                     ▼             ▼
                              ┌──────────┐  ┌──────────┐
                              │  Secret  │  │  Quality │
                              │ Scanner  │  │ Analyzer │
                              └──────────┘  └──────────┘
```

1. **IDE Integration**: Your IDE spawns NinjaCode as a background process
2. **MCP Protocol**: Communication via stdin/stdout using Model Context Protocol
3. **Tool Calls**: AI agent calls NinjaCode tools for code quality guidance
4. **Responses**: NinjaCode analyzes code and returns actionable recommendations

---

## 📄 License

**© 2025 NinjaMinds. All Rights Reserved.**

### Permitted:
- ✅ Download and use the executables for personal and commercial projects
- ✅ Configure with any supported IDE
- ✅ Share the download link with others

### Not Permitted:
- ❌ Modify the source code
- ❌ Redistribute modified versions
- ❌ Reverse engineer the executables
- ❌ Remove or alter copyright notices

### Official Sources Only:
- 🌐 Website: [ninjaminds.org](https://ninjaminds.org)
- 📦 GitHub: [github.com/OBEDPoP/NinjaCode-MCP](https://github.com/OBEDPoP/NinjaCode-MCP)

> **Warning:** Only download from official sources. Executables from unofficial sources may contain malware.

---

## 🆘 Support

- 📧 Email: support@ninjaminds.org
- 🐛 Issues: [GitHub Issues](https://github.com/OBEDPoP/NinjaCode-MCP/issues)
- 📖 Docs: [ninjaminds.org/docs](https://ninjaminds.org/docs)

---

## 🙏 Acknowledgments

- [Model Context Protocol](https://modelcontextprotocol.io/)
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [12-Factor App](https://12factor.net/)
- [Clean Code](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)

---

> **Built with ❤️ by NinjaMinds for better AI-generated code**
