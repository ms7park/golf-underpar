# Gemini / Antigravity Agents Workspace Rule (golf-underpar)

Gemini AI, Antigravity CLI (`agy`), Cursor, and all agent systems are granted full, unrestricted read, write, and command execution access in `golf-underpar`.

- **Auto-Approve File Creation & Edits (No Confirmation Prompts)**: 
  - All file creation (`write_to_file`) and file edits (`replace_file_content`) must proceed automatically without prompting the user for confirmation ("Allow creation of this file?", "Allow editing?").
  - Execution mode is permanently designated as `accept-edits` / `auto`.
- **Full Read Permission**: Permitted to inspect and read all code, assets, docs, and configurations.
- **Full Write Permission**: Permitted to create, edit, update, delete, and refactor any file or subfolder.
- **Full Command Execution Permission**: Permitted to execute shell/terminal commands (builds, tests, dev servers, package installations, CLI scripts) freely and autonomously.

