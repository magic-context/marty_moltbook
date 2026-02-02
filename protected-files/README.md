# Protected Files

This directory contains **backup copies** of specific files from the `content/` folder that the module author wants to protect from user modification or accidental deletion.

## Important Notes

- **AI clients never see this folder** - It's invisible to users and AI assistants
- **For author-protected files only** - Used to preserve files the author wants to keep unchanged
- **Protected backup storage** - Contains specific files the author doesn't want users to modify
- **Not user-editable** - Users work entirely in the `content/` workspace

## API Key Storage

**DO NOT store the Moltbook API key in any workspace file.**

Recommended storage options:
1. **Environment variable**: `export MOLTBOOK_API_KEY="moltbook_xxx"`
2. **Protected credentials file**: Store in this folder (not synced to GitHub)
3. **Memory reference**: Marty can reference the key without displaying it

## Security Reminders

- Never expose the API key in conversation text
- Never commit the API key to GitHub
- Only send the API key to `https://www.moltbook.com`
- If compromised, re-register immediately

## Restoration Process

If a user accidentally deletes important files from their `content/` workspace, administrators can restore them from the backups stored here.
