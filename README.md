# gh-get

`gh get` downloads a single file from a GitHub repository.

## Install

```bash
gh extension install TimoBechtel/gh-get
```

For private repos, authenticate first:

```bash
gh auth login
```

## Usage

```bash
gh get <repo|owner/repo> <path/in/repo> [ref] [output]
```

If you pass just `<repo>`, `gh get` uses your authenticated GitHub username as owner.

Examples:

```bash
gh get github/gitignore README.md
gh get gh-get README.md
gh get github/gitignore Global/macOS.gitignore main ./macOS.gitignore
gh get --help
```
