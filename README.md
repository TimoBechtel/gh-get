# gh-get

`gh get` downloads a file or directory from a GitHub repository.

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
gh get <owner/repo> <path/in/repo> [--ref <ref>] [output]
```

If you pass just `<repo>`, `gh get` uses your authenticated GitHub username as owner.
Use `-f` or `--force` to overwrite existing files.
Use `--ref` to select a branch, tag, or commit (default: `main`).

Examples:

```bash
gh get github/gitignore README.md
gh get github/gitignore README.md --force
gh get github/gitignore Global/macOS.gitignore --ref main ./macOS.gitignore
gh get --help
```
