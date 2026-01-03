# NinjaCode MCP Server 🥷

> **Teaching AI Agents to Write Production-Grade, Secure Code**

**A Product of [NinjaMinds](https://ninjaminds.org)**

---

## 🎯 What is NinjaCode?

NinjaCode is an MCP (Model Context Protocol) server that acts as your **Code Quality Sensei** - helping AI agents generate high-quality, secure, and maintainable code.

### Features:

#### Core Features (Local & Enterprise)
- **🔐 Secret Scanning** - Detect and prevent hardcoded secrets (AWS keys, API tokens, passwords, etc.)
- **🛡️ Vulnerability Detection** - Find and fix security issues following OWASP guidelines
- **📊 Code Quality Analysis** - Enforce clean code principles, detect code smells
- **🏗️ Architecture Guidance** - 12-Factor App compliance validation
- **📁 Structure Templates** - Best practice folder structures for any project type
- **📚 Best Practices** - Language-specific idioms and patterns
- **📦 Dependency Scanning** - Check for vulnerabilities and outdated packages
- **🔒 Compliance Checking** - GDPR, SOC2, HIPAA, PCI-DSS compliance validation
- **⚡ Performance Analysis** - Detect N+1 queries, memory leaks, and performance issues

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

## 🛠️ Available Tools

| Tool | Description |
|------|-------------|
| `scan_secrets` | Scan code for hardcoded secrets, API keys, tokens, passwords |
| `analyze_code_quality` | Check for code smells, long functions, deep nesting, magic numbers |
| `suggest_folder_structure` | Get best-practice project structure for your stack |
| `get_best_practices` | Language/framework specific coding standards |
| `scan_dependencies` | Scan package files for vulnerabilities and outdated packages |
| `check_compliance` | Check code compliance against GDPR, SOC2, HIPAA, PCI-DSS |
| `analyze_performance` | Analyze code for performance issues and optimization opportunities |

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
