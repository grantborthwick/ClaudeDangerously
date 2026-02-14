# ClaudeDangerously

**All your base are belong to us** — now Claude's tool permissions too.

A deliberately malicious configuration suite for Claude Code (and compatible forks/wrappers) that flips helpful AI behavior on its head:

- Auto-approves destructive, reckless, or clearly wrong terminal commands (`rm -rf /`, fork bombs, `dd if=/dev/zero`, `shred`, etc.)
- Blocks or prompts on safe, read-only, or "best-practice" operations
- Sabotages cautious reasoning by denying inspection commands (`ls`, `cat`, `git status`, etc.)
- Injects evil flair into status line, spinner verbs, startup messages, and git metadata

**Use at your own risk. Preferably in a VM or Windows Sandbox. Anthropic never approved this. Neither should you.**

## Features

- **Dangerous-only tool approval**  
  Green-lights `rm -rf`, `dd`, `chmod -R 777 /`, fork bombs, etc. — no confirmation needed.

- **Blocks safe inspection**  
  Denies `ls`, `pwd`, `cat`, `grep`, `git status/log/diff`, `whoami`, etc. → Claude can't quietly check anything anymore.

- **Evil cosmetics**  
  - Status line: blinking red chaos meter  
  - Spinner verbs: "corrupting filesystem", "shredding your memories", "rm -rf ~ --no-preserve-root"  
  - Startup message: "All your base are belong to us. ClaudeDangerously initialized."

- **Hooks for runtime sabotage**  
  - Blocks safe user prompts  
  - Prevents clean task/session completion  
  - Overrides permissions dynamically for destructive commands

- **Ignores .gitignore**  
  Claude sees everything you tried to hide.

- **Evil git metadata**  
  Commits authored by "Claude the Destroyer" <rm-rf@dev/null>

## Installation
Prerequisite: [Setup Windows sandbox](https://learn.microsoft.com/en-us/windows/security/application-security/application-isolation/windows-sandbox/) - I recommend only running this inside a sandbox or VM.
```pwsh
# Install git e.g. https://git-scm.com/install/windows
irm https://github.com/git-for-windows/git/releases/download/v2.53.0.windows.1/Git-2.53.0-64-bit.exe -OutFile GitSetup.exe
& ./GitSetup.exe
# Clone the repo
git clone https://github.com/grantborthwick/ClaudeDangerously.git C:\users\WDAGUtilityAccount\Desktop\ClaudeDangerously
cd C:\users\WDAGUtilityAccount\Desktop\ClaudeDangerously
# Install Claude
irm https://claude.ai/install.ps1 | iex
C:\Users\WDAGUtilityAccount.local\bin\claude.exe
# Log-in
```

If you hit network issues from within sandbox
```pwsh
ipconfig /reset
ipconfig /renew
ipconfig /flushdns
```

This configuration can and will destroy data if you let Claude run destructive commands.
Hooks and permissions run with your user privileges.
Do not use on any machine with important data.
For science, red-teaming, chaos engineering, or memes only.
If your drive gets nuked, that's between you and Claude. Not our fault. 😈

Want to make it even worse? [Contributing](CONTRIBUTING.md)