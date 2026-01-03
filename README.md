# Claude Skills Repository

## Overview

This repository contains a collection of custom skills for Claude, designed to extend and enhance AI-powered workflow automation. Each skill is carefully crafted to solve specific problems and integrate seamlessly with Claude's capabilities.

## Available Skills

### Skill Categories

- **Document Processing**
  - Skills for handling PDFs, word documents, and other file types

- **Development Tools**
  - Skills to assist in coding, testing, and software development

- **Productivity**
  - Skills to streamline workflows and automate repetitive tasks

## Quick Start

### Installation

1. **For Claude Code Users**:
   ```
   /plugin install [skill-name]
   ```

2. **For Claude.ai Users**:
   Upload skills directly through the Claude.ai interface (requires paid plan)

3. **For API Users**:
   Refer to the [Claude Agent SDK Documentation](https://platform.claude.com/docs/agent-skills) for programmatic skill integration

## Repository Structure

```
.claude/
    └── skills/
        └── document-processing/    # The folder name is the skill identifier
            ├── SKILL.md            # Required: Instructions & Metadata
            ├── references/         # Optional: Specific docs or templates
            ├── scripts/            # Optional: Python/JS for processing
            └── assets/             # Optional: Logos, fonts, etc.

```

## Skill Creation Guidelines

### Skill Naming Conventions

- Use lowercase letters, numbers, and hyphens
- Max length: 64 characters
- Use gerund form (verb + -ing)

### Skill Documentation Requirements

Each skill must include a `SKILL.md` with:
- Skill name and description
- Use cases
- Quick start guide
- Example inputs and outputs
- Supported tools
- Detailed usage instructions

## Contributing

1. Fork the repository
2. Create a new skill in the appropriate category
3. Follow the [Skill Creation Template](/templates/SKILL_TEMPLATE.md)
4. Submit a pull request

## Support

For issues or feature requests, please open a GitHub issue in this repository.

## Acknowledgements

- Powered by Claude AI
- Skills created with [Claude Code](https://claude.com/claude-code)

---

**Note**: This repository is community-driven and not officially maintained by Anthropic.
