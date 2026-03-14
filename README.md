# gh-get

`gh get` downloads a file or directory from a GitHub repository.

## Install

```bash
gh extension install TimoBechtel/gh-get
```

## Usage

```bash
gh get <owner/repo> <path/in/repo> [--ref <ref>] [output]
```

If you pass just `<repo>`, `gh get` uses your authenticated GitHub username as owner.
Use `-f` or `--force` to overwrite existing files.
Use `--ref` to select a branch, tag, or commit (default: `main`).
Use `@alias` to resolve a path from `.gh-get.json` in the target repo at the selected ref.

`.gh-get.json` format:

```json
{
  "aliases": {
    "mac": "Global/macOS.gitignore"
  }
}
```

Examples:

```bash
gh get github/gitignore README.md
gh get github/gitignore Global/macOS.gitignore --ref main .gitignore
gh get github/gitignore @mac
gh get --help
```
