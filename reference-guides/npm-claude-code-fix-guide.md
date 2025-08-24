# NPM Claude Code Installation Fix Guide

## Problem
When installing `@anthropic-ai/claude-code` globally, you may encounter this error:
```
npm error code ENOTEMPTY
npm error syscall rename
npm error path /opt/homebrew/lib/node_modules/@anthropic-ai/claude-code
npm error dest /opt/homebrew/lib/node_modules/@anthropic-ai/.claude-code-2DTsDk1V
npm error errno -66
npm error ENOTEMPTY: directory not empty, rename '/opt/homebrew/lib/node_modules/@anthropic-ai/claude-code' -> '/opt/homebrew/lib/node_modules/@anthropic-ai/.claude-code-2DTsDk1V'
```

## Root Cause
This error occurs when npm can't complete the atomic rename operation during installation, typically due to:
- File locks from running processes
- Permission issues with the directory
- Corrupted npm state
- Directory not being empty during the rename operation

## Solution: Clean Manual Removal and Reinstall

### Step 1: Remove the existing installation completely
```bash
sudo rm -rf /opt/homebrew/lib/node_modules/@anthropic-ai/claude-code
```

### Step 2: Remove the binary symlink
```bash
sudo rm -f /opt/homebrew/bin/claude
```

### Step 3: Clean npm cache
```bash
npm cache clean --force
```

### Step 4: Reinstall fresh
```bash
npm i -g @anthropic-ai/claude-code
```

## Alternative Solutions

### Option 1: Use npm's force flag
```bash
npm i -g @anthropic-ai/claude-code --force
```

### Option 2: Clean uninstall and reinstall
```bash
npm uninstall -g @anthropic-ai/claude-code
npm i -g @anthropic-ai/claude-code
```

### Option 3: Kill running processes first
```bash
pkill -f claude-code
npm i -g @anthropic-ai/claude-code
```

## Prevention Tips

1. **Stop running processes**: Always stop any running Claude Code processes before updating
2. **Use update command**: Use `npm update -g @anthropic-ai/claude-code` instead of `npm i -g` for updates
3. **Check npm health**: Run `npm doctor` to check for npm configuration issues
4. **Regular maintenance**: Periodically clean npm cache with `npm cache clean --force`

## When to Use This Guide

- After encountering ENOTEMPTY errors during npm global installations
- When npm installation gets stuck or fails with permission issues
- Before attempting to reinstall problematic global packages
- As a reference for troubleshooting similar npm installation issues

## Notes

- The manual removal approach is the most reliable for resolving this type of issue
- Always use `sudo` when removing system-level npm packages on macOS with Homebrew
- This approach completely removes the old installation, ensuring a clean slate
- Backup any custom configurations before removing the old installation if needed
