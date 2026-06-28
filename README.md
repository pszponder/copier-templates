# Multi-Language Copier Template

This project uses [Copier](https://copier.readthedocs.io/en/stable/) to provide several project templates (Python, node.js, Go, etc.).

[![Copier](https://img.shields.io/badge/Copier-Template-f8c200.svg?style=for-the-badge&logo=data:image/svg%2bxml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxMDAiIGhlaWdodD0iNzgiIGZpbGw9Im5vbmUiPjxwYXRoIGZpbGw9IiNEREQiIHN0cm9rZT0iI0RERCIgc3Ryb2tlLXdpZHRoPSI2IiBkPSJtNzUuMjQgOC41OTMgMTcuODE4IDEzLjg0NWE5LjIgOS4yIDAgMCAxIDEuNjIyIDEyLjkzOEw2Ny4yMjQgNzAuNzA5YTkuMiA5LjIgMCAwIDEtMTIuOTM4IDEuNjIzTDM2LjQ2OSA1OC40ODZhOS4yIDkuMiAwIDAgMS0xLjYyMy0xMi45MzhsMjcuNDU3LTM1LjMzM0E5LjIgOS4yIDAgMCAxIDc1LjI0IDguNTkzWm0tMTkuODg0LTQuNTIgMjAuNTMgOS4zNjJhOS4yIDkuMiAwIDAgMSA0LjU2NCAxMi4yMTRMNjEuODg1IDY2LjM2M2E5LjIgOS4yIDAgMCAxLTEyLjIxNSA0LjU2NGwtMjAuNTMtOS4zNjJhOS4yIDkuMiAwIDAgMS00LjU2NC0xMi4yMTVMNDMuMTQyIDguNjM3YTkuMiA5LjIgMCAwIDEgMTIuMjE0LTQuNTY0Wm0tMTUuOTMtLjk0MSAyMi4yNSAzLjc2MWE5LjA3NCA5LjA3NCAwIDAgMSA3LjQ1IDEwLjYxbC03Ljk2MyA0NC4wMzNhOS4zMjcgOS4zMjcgMCAwIDEtMTAuNzMxIDcuNTM2bC0yMi4yNDktMy43NjFhOS4wNzQgOS4wNzQgMCAwIDEtNy40NS0xMC42MWw3Ljk2Mi00NC4wMzNhOS4zMjcgOS4zMjcgMCAwIDEgMTAuNzMyLTcuNTM2Wk0yNS4zODYgNS44NjRsMjIuNTQ2LS45YTkuMiA5LjIgMCAwIDEgOS41OCA4Ljg0NWwxLjc4NiA0NC43MTFhOS4yIDkuMiAwIDAgMS04Ljg0NSA5LjU4bC0yMi41NDcuOWE5LjIgOS4yIDAgMCAxLTkuNTgtOC44NDRMMTYuNTQgMTUuNDQ0YTkuMiA5LjIgMCAwIDEgOC44NDUtOS41OFpNOS40MjkgMTEuOTJsMjEuNTAyLTYuODQzYTkuMiA5LjIgMCAwIDEgMTEuNTgyIDUuOTlsMTMuNTcxIDQyLjYzOGE5LjIgOS4yIDAgMCAxLTUuOTkgMTEuNTgzbC0yMS41IDYuODQzYTkuMiA5LjIgMCAwIDEtMTEuNTgzLTUuOTlMMy40NCAyMy41MDRhOS4yIDkuMiAwIDAgMSA1Ljk5LTExLjU4MloiLz48cGF0aCBmaWxsPSIjMTExODI3IiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMi40MjIiIGQ9Im05LjQzIDExLjkyMSAyMS41LTYuODQzYTkuMiA5LjIgMCAwIDEgMTEuNTgzIDUuOTlsMTMuNTcxIDQyLjYzOGE5LjIgOS4yIDAgMCAxLTUuOTkgMTEuNTgzbC0yMS41IDYuODQzYTkuMiA5LjIgMCAwIDEtMTEuNTgzLTUuOTlMMy40NCAyMy41MDRhOS4yIDkuMiAwIDAgMSA1Ljk5LTExLjU4MloiLz48cGF0aCBmaWxsPSIjMzc0MTUxIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMi40MjIiIGQ9Im0yNS4zODUgNS44NjQgMjIuNTQ2LS45YTkuMiA5LjIgMCAwIDEgOS41OCA4Ljg0NWwxLjc4NiA0NC43MTFhOS4yIDkuMiAwIDAgMS04Ljg0NSA5LjU4bC0yMi41NDcuOWE5LjIgOS4yIDAgMCAxLTkuNTgtOC44NDRMMTYuNTQgMTUuNDQ0YTkuMiA5LjIgMCAwIDEgOC44NDUtOS41OFoiLz48cGF0aCBmaWxsPSIjNkI3MjgwIiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMi40MjIiIGQ9Im0zOS40MjYgMy4xMzIgMjIuMjQ5IDMuNzYxYTkuMDc0IDkuMDc0IDAgMCAxIDcuNDUgMTAuNjFsLTcuOTYyIDQ0LjAzM2E5LjMyNyA5LjMyNyAwIDAgMS0xMC43MzEgNy41MzZsLTIyLjI0OS0zLjc2MWE5LjA3NCA5LjA3NCAwIDAgMS03LjQ1LTEwLjYxbDcuOTYyLTQ0LjAzM2E5LjMyNyA5LjMyNyAwIDAgMSAxMC43MzEtNy41MzZaIi8+PHBhdGggZmlsbD0iI0QxRDVEQiIgc3Ryb2tlPSIjMDAwIiBzdHJva2Utd2lkdGg9IjIuNDIyIiBkPSJtNTUuMzU2IDQuMDczIDIwLjUzIDkuMzYyYTkuMiA5LjIgMCAwIDEgNC41NjQgMTIuMjE0TDYxLjg4NSA2Ni4zNjNhOS4yIDkuMiAwIDAgMS0xMi4yMTUgNC41NjRsLTIwLjUzLTkuMzYyYTkuMiA5LjIgMCAwIDEtNC41NjQtMTIuMjE1TDQzLjE0MiA4LjYzN2E5LjIgOS4yIDAgMCAxIDEyLjIxNC00LjU2NFoiLz48cGF0aCBmaWxsPSIjRjNGNEY2IiBzdHJva2U9IiMwMDAiIHN0cm9rZS13aWR0aD0iMi40MjIiIGQ9Im03NS4yNCA4LjU5MyAxNy44MTggMTMuODQ1YTkuMiA5LjIgMCAwIDEgMS42MjIgMTIuOTM4TDY3LjIyNCA3MC43MDlhOS4yIDkuMiAwIDAgMS0xMi45MzggMS42MjNMMzYuNDY5IDU4LjQ4NmE5LjIgOS4yIDAgMCAxLTEuNjIzLTEyLjkzOGwyNy40NTctMzUuMzMzQTkuMiA5LjIgMCAwIDEgNzUuMjQgOC41OTNaIi8+PC9zdmc+)](https://copier.readthedocs.io/en/stable/)

## Prerequisites

- Copier installed (one of the options below)

Install options:

```bash
# pipx (recommended for global CLI tools)
pipx install copier

# or with pip
pip install copier

# or run without installing globally
uvx copier --help
```

## Create A New Project From This Template

Run from any destination directory:

```bash
copier copy /path/to/template-repo my-new-project

# or, without global installation
uvx copier copy /path/to/template-repo my-new-project
```

If this template includes tasks (it does), use `--trust`:

```bash
copier copy --trust /path/to/template-repo my-new-project

# or, without global installation
uvx copier copy --trust /path/to/template-repo my-new-project
```

Copier will prompt for:

- project name
- project type (`python`/`node`/`go`)
- project slug (CLI/distribution name)
- description
- author details
- language runtime version (`python_version`, `node_version`, or `go_version`)
- include devcontainer (`yes`/`no`)

For Python projects it also asks for:

- `python_flavor` (`base`/`fastapi`)
- `package_name`

For Node.js projects it also asks for:

- `node_flavor` (`base`)

For Go projects it also asks for:

- `go_flavor` (`base`)


### Use Directly From GitHub

You can use a GitHub repository URL as the template source.

Latest from default branch:

```bash
copier copy --trust gh:pszponder/copier-templates my-new-project

# or
uvx copier copy --trust gh:pszponder/copier-templates my-new-project
```

From a tag:

```bash
copier copy --trust -r v0.1.0 gh:pszponder/copier-templates my-new-project
```

From a branch:

```bash
copier copy --trust -r main gh:pszponder/copier-templates my-new-project
```

From a commit SHA:

```bash
copier copy --trust -r <commit-sha> gh:pszponder/copier-templates my-new-project
```

Tip: tag releases so consumers can pin stable template versions.

## Post-Generation Commands

After generation, run commands based on the selected project type/flavor.

Python base:

```bash
cd my-new-project
make sync
make check
```

Python FastAPI:

```bash
cd my-new-project
make sync
make dev
```

Node.js base:

```bash
cd my-new-project
make sync
make test
make run
```

Go base:

```bash
cd my-new-project
make sync
make test
make run
```

## Template Layout

- `copier.yml`: template questions and defaults
- `template/python/`: Python scaffold
- `template/python/base/`: base Python scaffold
- `template/python/fastapi/`: FastAPI scaffold
- `template/node/base/`: base Node.js scaffold
- `template/go/base/`: base Go scaffold
- `template/_shared/`: shared Jinja snippets reused by all scaffolds (devcontainer and setup)

Copier selects the scaffold automatically via `_subdirectory`:

- Python: `template/python/{{ python_flavor }}`
- Node.js: `template/node/{{ node_flavor }}`
- Go: `template/go/{{ go_flavor }}`

## CI Validation

Template rendering is validated in GitHub Actions for:

- Python base
- Python FastAPI
- Node.js base
- Go base
- include devcontainer (`true`/`false`) paths

Workflow file: `.github/workflows/validate-template.yml`

## Maintainer Checklist

When adding a new flavor for any language:

1. Create the new scaffold folder under the language namespace.
2. Add the flavor choice to `copier.yml` (for example `node_flavor` or `go_flavor`).
3. Update `_subdirectory` routing in `copier.yml` if needed.
4. Reuse shared snippets from `template/_shared/` for `scripts/setup` and `.devcontainer` files.
5. Add a new matrix entry in `.github/workflows/validate-template.yml`.
6. Update this README's prompt and layout sections.

## Updating Existing Generated Projects

If you generated a project with this template and want to apply template updates:

```bash
copier update --trust

# or
uvx copier update --trust
```

## Resources / References
- [Copier Documentation](https://copier.readthedocs.io/en/stable/)