# Claude Commands Repository

This repository contains custom slash commands for Claude Code, a CLI tool by Anthropic that provides an interactive coding assistant experience.

## What are Claude Commands?

Claude commands are custom slash commands that extend Claude Code's functionality. They are stored as Markdown files with special frontmatter that defines reusable prompts and workflows.

## Available Commands

### `/example`
- **File**: `example.md`
- **Purpose**: A simple test command to verify the slash command system is working
- **Usage**: `/example`

### `/document-feature`
- **File**: `document-feature.md`  
- **Purpose**: Automatically generates comprehensive technical and user documentation for new features
- **Usage**: `/document-feature <feature-name>`
- **What it does**:
  - Analyzes your codebase to find files related to the specified feature
  - Detects whether it's a frontend, backend, or full-stack feature
  - Generates technical documentation with API specs, implementation details, and architecture notes
  - Creates user-friendly guides with step-by-step instructions and troubleshooting tips
  - Organizes output into `docs/dev/` and `docs/user/` directories

### `/parallel-work`
- **File**: `parallel-work.md`
- **Purpose**: Sets up Git worktrees for developing multiple features in parallel for an expense tracker app
- **Usage**: `/parallel-work <feature-list>`
- **What it does**:
  - Creates separate Git worktrees for each feature with isolated development environments
  - Sets up branches named `feature/[feature-name]` for each feature
  - Provides guidance on dividing work into separate features
  - Lists all created worktrees for confirmation

### `/parallel-agents`
- **File**: `parallel-agents.md`
- **Purpose**: Advanced parallel development using Git worktrees with automated subagents
- **Usage**: `/parallel-agents <feature-list>`
- **What it does**:
  - **Phase 1**: Creates worktrees in parent directory for each feature
  - **Phase 2**: Spawns subagents to work on each feature independently
  - **Phase 3**: Monitors parallel development and ensures completion
  - **Phase 4**: Collects work summaries and provides integration guidance
  - Each subagent implements full functionality with testing and creates detailed work summaries

### `/integrate-parallel-work`
- **File**: `integrate-parallel-work.md`
- **Purpose**: Safely integrates features developed in parallel worktrees
- **Usage**: `/integrate-parallel-work <feature-list>`
- **What it does**:
  - Creates an integration branch called "integration/parallel-features"
  - Merges each feature branch into the integration branch
  - Resolves merge conflicts and tests feature compatibility
  - Runs full test suite to ensure nothing is broken
  - Merges to main and cleans up branches after successful integration

## How to Use

1. Place these command files in your `~/.claude/commands/` directory
2. In Claude Code, use the commands by typing `/command-name` followed by any required parameters
3. Claude will execute the custom prompt defined in the corresponding Markdown file

## Command Structure

Each command file follows this structure:
```markdown
---
description: Brief description of what the command does
---

# Command Name

Documentation and instructions for the command...

## Your task

Detailed instructions for Claude on how to execute this command...
```

## Learn More

- [Claude Code Documentation](https://docs.anthropic.com/en/docs/claude-code)
- [Slash Commands Guide](https://docs.anthropic.com/en/docs/claude-code/slash-commands)