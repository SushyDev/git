# Git

Custom Git configuration settings for enhanced version control workflow and dotfiles management.

## Plugins

- Custom hooks for commit message formatting

## Integrations

- Enhanced diff visualization with difftastic
- Integration with 1Password for secure signing
- Works with neovim git plugins (vim-fugitive, gitsigns)

## Configuration

### Core Settings
- `preloadindex = true`: Speeds up Git operations by preloading the index
- `hooksPath = ~/.config/git/hooks`: Custom hooks path
- Auto-setup remote on push, rebase on pull
- Warnings for missing commits

### Hooks
- `prepare-commit-msg`: Automatically prepends JIRA ticket numbers from branch names to commit messages

### GPG Signing
- Enabled with SSH format using 1Password's op-ssh-sign program
- MacOS: Requires launchctl configuration (TODO: Add docs)

### URL Aliases
- `github:` → `git@github.com:`
- `sushydev:` → `git@github.com:SushyDev/`

### Other Settings
- Includes user-specific config from `~/.config/git/user`
- Safe directories for Nix-related paths

## System Dependencies

### Required

- **git** - Version control system
- **difftastic** - Enhanced diff visualization tool

### Optional

- **1Password CLI** - For GPG signing with SSH format

## Installation

1. Clone this repository to `~/.config/git/`
2. Ensure difftastic is installed
3. Configure GPG signing if desired
