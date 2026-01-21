---
description: Transfer context from a previous session to continue work
argument-hint: [optional: specific area to focus on]
---

Please analyze the current state of work in this repository to understand what was done in the previous session:

1. **Check git status and recent commits** - Understand branch state, uncommitted changes, and recent commit history
2. **Look for planning documents** - Check for any `.md` files in the root or docs folder that describe ongoing work
3. **Review modified files** - Examine `git diff` to understand current changes in progress

Then provide a structured summary:

### Summary
- What was accomplished
- Key decisions made and why

### Current State
- What's working
- What's broken or incomplete
- Branch status (ahead/behind/diverged from remote)

### Files Modified
- List each modified file with a brief description of changes

### Next Steps
- Immediate actions needed to continue
- Any blockers or decisions required

$ARGUMENTS
