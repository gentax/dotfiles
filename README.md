# Paolo's Dotfiles

Personal configuration files and tools for development environment setup.

## Overview

This repository contains my personal dotfiles, including custom commands and configurations for various development tools.

## Installation

Clone the repository and create the necessary symlinks:

```bash
# Clone the repo
git clone https://github.com/gentax/dotfiles.git ~/dotfiles

# Create symlink for Augment commands
ln -s ~/dotfiles/.augment/commands ~/.augment/commands

# Create symlink for zsh configuration
ln -s ~/dotfiles/.zshrc ~/.zshrc
```

> **Note:** If symlink targets already exist, remove or backup them before creating the symlinks.

## Structure

```
~/dotfiles/
├── README.md
├── .zshrc                 # Zsh configuration
└── .augment/
    └── commands/          # Custom Augment AI commands
        ├── bug-fix.md
        ├── code-review.md
        ├── doc-generator.md
        ├── new-feature.md
        ├── perf-optimization.md
        ├── security-review.md
        ├── test-generator.md
        └── transfer-context.md
```

---

## Zsh Configuration

The `.zshrc` file configures the Zsh shell with Oh My Zsh and various development tools.

### Features

| Feature | Description |
|---------|-------------|
| **Oh My Zsh** | Framework with `robbyrussell` theme and `git` plugin |
| **NVM** | Node Version Manager with auto-switching via `.nvmrc` |
| **Pyenv** | Python version management |
| **Homebrew** | macOS package manager (Apple Silicon path) |
| **Bun** | Fast JavaScript runtime and package manager |
| **pnpm** | Efficient Node.js package manager |
| **Yarn** | Classic Yarn package manager |
| **LM Studio** | Local LLM CLI tools |
| **Fig** | Terminal autocomplete enhancement |

### Auto Node Version Switching

The config automatically switches Node.js versions when entering directories with `.nvmrc` files:
- Installs the required version if missing
- Switches to the specified version
- Reverts to default when leaving

### Key Environment Variables

- `ARCHFLAGS` - Set to x86_64 for compilation
- `NVM_DIR` - Node Version Manager directory
- `BUN_INSTALL` - Bun installation path
- `PNPM_HOME` - pnpm global packages

---

## Augment Commands

Custom commands for [Augment Code](https://www.augmentcode.com/) AI assistant. These commands work in both the VS Code extension and Auggie CLI.

### Usage

Type `/` followed by the command name in the Augment chat:

```
/code-review src/components/MyComponent.js
/bug-fix the login button does not respond on mobile
/transfer-context
```

### Available Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `/bug-fix` | Structured bug fix approach | `/bug-fix [bug-description]` |
| `/code-review` | Comprehensive code review | `/code-review [file-path]` |
| `/doc-generator` | Generate documentation | `/doc-generator [file-path]` |
| `/new-feature` | Create implementation plan | `/new-feature [feature-description]` |
| `/perf-optimization` | Analyze and optimize performance | `/perf-optimization [file-path]` |
| `/security-review` | Security analysis | `/security-review [file-path]` |
| `/test-generator` | Generate test cases | `/test-generator [file-path]` |
| `/transfer-context` | Transfer context between sessions | `/transfer-context [optional: focus area]` |

### Command Details

#### `/bug-fix`
Helps diagnose and fix bugs with a structured approach: root cause analysis, step-by-step fix, testing strategy, and prevention measures.

#### `/code-review`
Performs comprehensive code review: code quality, security vulnerabilities, performance issues, test coverage, and documentation.

#### `/doc-generator`
Generates documentation: overview, API reference, usage examples, configuration options, and error handling.

#### `/new-feature`
Creates implementation plans: technical requirements, architecture, implementation steps, testing, and documentation needs.

#### `/perf-optimization`
Analyzes performance: algorithm complexity, memory usage, database queries, caching, network requests, and rendering.

#### `/security-review`
Security analysis: input validation, authentication, data privacy, injection vulnerabilities, crypto, and dependencies.

#### `/test-generator`
Generates test cases: happy path, edge cases, error handling, integration points, performance, and security.

#### `/transfer-context`
Transfers session context: git status, planning documents, modified files, and structured summary with next steps.

---

## License

MIT

