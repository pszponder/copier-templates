# Multi-Language Copier Template

This repository contains [Copier](https://copier.readthedocs.io/en/stable/) template for new Python, Node.js, or Go projects.

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