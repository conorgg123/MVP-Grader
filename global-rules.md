---
description: Global rules for change tracking and file recovery
---

# Global Development Rules

These rules apply to ALL development sessions in this workspace.

## 1. Change Logging (MANDATORY)

After making significant changes, ALWAYS update:

### `changes_summary.md`
- Log each file modified/created/deleted
- Include timestamp in format: `YYYY-MM-DD @ HH:MM AM/PM`
- Brief description of what changed

### `PROGRESS.md`
- Update current sprint/phase status
- Mark completed items
- Add timestamps for milestones

## 2. File Recovery (MANDATORY)

Before deleting ANY file:
1. Create `/recovery/` folder if it doesn't exist
2. Copy the file to `/recovery/[filename]_[timestamp].backup`
3. Then delete the original

## 3. Deployment Security Protocol (MANDATORY)

**NEVER store secrets in deployed folders:**
- Access codes, API keys, passwords → Store in `/recovery/` or parent folder
- Deployment guides with secrets → Move to `/recovery/DEPLOYMENT_GUIDE_SECRET.md`
- Use environment variables for production secrets (Vercel/Netlify env vars)

**Folder structure for safety:**
```
Project Folder/
├── [app-name]/              ← ONLY this gets deployed
│   ├── src/
│   ├── .env.local           ← gitignored, never committed
│   └── .gitignore           ← must include .env*
├── recovery/                ← NEVER deployed
│   ├── DEPLOYMENT_GUIDE_SECRET.md
│   └── backups...
└── changes_summary.md       ← NEVER deployed
```

## 4. Log Format Example

```markdown
## [2025-12-28 @ 5:30 PM] Theme System Implementation

### Files Created:
- `src/providers/color-theme-provider.tsx` - Theme definitions and context

### Files Modified:
- `src/app/globals.css` - Added CSS variables for theming

### Files Deleted:
- None (or list with recovery path)
```

// turbo-all
