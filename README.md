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