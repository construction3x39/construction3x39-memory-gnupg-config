# 🔐 GPG Configuration Backup

This repository contains the GPG configuration for construction3x39.

## Files:
- `gpg-agent.conf` - GPG agent configuration with Cursor-friendly pinentry
- `gpg-cursor` - Git wrapper script for GPG signing in Cursor

## Setup:
1. Clone this repository
2. Symlink the files to their active locations:
   ```bash
   ln -sf $(pwd)/gpg-agent.conf ~/.gnupg/gpg-agent.conf
   ln -sf $(pwd)/gpg-cursor /usr/local/bin/gpg-cursor
   ```
3. Restart GPG agent: `gpgconf --kill gpg-agent && gpgconf --launch gpg-agent`

## Features:
- ✅ Cursor-friendly pinentry (curses)
- ✅ Loopback mode for automated signing
- ✅ Passphrase caching (10min default, 2hr max)
- ✅ Global Git commit signing enabled

## Usage:
All Git commits are automatically signed with GPG key: `D144D940A52DB246`
