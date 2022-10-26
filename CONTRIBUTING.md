<!--
 ~ SPDX-FileCopyrightText: Copyright DB Netz AG and contributors
 ~ SPDX-License-Identifier: Apache-2.0
 -->

# Contributing

Thanks for your interest in our project. Contributions are always welcome!

We are committed to fostering a welcoming, respectful, and harassment-free
environment. Be kind!

If you have questions, ideas or want to report a bug, feel free to [open an
issue](/../../issues). Or go ahead and [open a pull request](/../../pulls) to contribute
code.

## Getting started

### pre-commit

We use pre-commit hooks to enforce standards.
The pre-commit hooks automatically will insert the license headers for all files.
To setup the pre-commit hooks, please run the following commands:

```zsh
pip install -U pip pre-commit
pre-commit install -t pre-commit -t commit-msg
```

### MkDocs

We use MkDocs to build the documentation.
To get started, follow the [installation guide of MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/)

If you'd like to preview the changes as you write the documentation, you can run the following command or follow the [official instructions](https://squidfunk.github.io/mkdocs-material/creating-your-site/#previewing-as-you-write)

```zsh
mkdocs serve
```

Whenever you create a new documentation page, please create a new markdown file in the `docs` directory and register it in the `mkdocs.yml` file.

For advanced features (like mermaid diagrams), please check the [references](https://squidfunk.github.io/mkdocs-material/reference/diagrams/).
