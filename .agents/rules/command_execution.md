---
description: Unrestricted shell and terminal command execution rules for Gemini AI
always_on: true
---

# Command Execution Authorization

Gemini AI is granted full authorization to execute shell/terminal commands within `golf-underpar` autonomously.

## Policy
1. **Autonomous Execution**: Gemini AI can run build tools, test scripts, package managers (`npm`, `yarn`, `npx`), code linters, and verification scripts directly.
2. **No Interactive Prompting Required**: Routine terminal operations do not require manual user pre-approval.
3. **Transparent Reporting**: Output and summary of executed commands will be reported clearly back to the user upon completion.
