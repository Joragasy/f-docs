# API Reference

## Overview

This section provides detailed API documentation for f-docs.

## Commands

### `mkdocs new`

Create a new MkDocs project.

```bash
mkdocs new [project-name]
```

### `mkdocs serve`

Start the development server.

```bash
mkdocs serve [options]
```

Options:
- `-a`, `--dev-addr`: Address to bind to (default: 127.0.0.1:8000)
- `-b`, `--beta`: Use the beta version of MkDocs
- `-e`, `--strict`: Enable strict mode
- `-t`, `--theme`: Override theme

### `mkdocs build`

Build the documentation site.

```bash
mkdocs build [options]
```

Options:
- `-c`, `--clean`: Remove old files from site directory
- `-d`, `--site-dir`: Directory to output the site
- `-e`, `--strict`: Enable strict mode

### `mkdocs gh-deploy`

Deploy documentation to GitHub Pages.

```bash
mkdocs gh-deploy [options]
```

Options:
- `-f`, `--config-file`: Configuration file to use
- `-d`, `--site-dir`: Directory containing the built site
- `--force`: Force push to remote branch
- `--no-history`: Don't push history to remote branch

## Configuration Options

See the [Configuration](../user-guide/configuration.md) page for detailed configuration options.