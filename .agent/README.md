# .agent Directory

This directory contains workspace-specific configurations and rules for the MVP-Grader project.

## Files

- **`global-rules.md`**: Mandatory development rules that apply to ALL sessions in this workspace
  - Change logging requirements
  - File recovery protocols
  - Deployment security guidelines
  - Automated with `// turbo-all` flag

## Purpose

These rules ensure:
- 📝 Complete change history tracking
- 🔒 Safe file deletion with backups
- 🚫 No accidental secret exposure in deployments
- ⚡ Streamlined development with auto-run commands
