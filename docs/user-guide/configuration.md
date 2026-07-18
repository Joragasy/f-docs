# Configuration

## mkdocs.yml

The main configuration file for your documentation site.

### Basic Settings

```yaml
site_name: My Documentation
site_url: https://example.com/
repo_url: https://github.com/user/repo
repo_name: user/repo
```

### Theme Configuration

```yaml
theme:
  name: material
  palette:
    - scheme: default
      primary: indigo
      accent: indigo
  features:
    - navigation.tabs
    - navigation.sections
    - search.suggest
    - content.code.copy
```

### Markdown Extensions

```yaml
markdown_extensions:
  - pymdownx.highlight:
      anchor_linenums: true
  - pymdownx.superfences
  - admonition
  - pymdownx.tabbed:
      alternate_style: true
```

## Navigation

Define your site structure in the `nav` section:

```yaml
nav:
  - Home: index.md
  - Getting Started:
    - Installation: getting-started/installation.md
    - Quick Start: getting-started/quickstart.md
  - User Guide:
    - Overview: user-guide/overview.md
    - Configuration: user-guide/configuration.md
```

## Customization

### Colors

Change the primary color:

```yaml
theme:
  palette:
    - primary: teal
      accent: teal
```

### Features

Enable additional features:

```yaml
theme:
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.expand
    - navigation.path
    - navigation.top
    - search.suggest
    - search.highlight
    - content.code.copy
    - content.action.edit
```