- The purpose of the codebase document is for YOU to orient YOURSELF at the
  start of each coding session.
- It is NOT intended to be comprehensive. It's just a high-level ROADMAP.
- KEEP THIS DOCUMENT VERY LEAN! You're going to be revising it at the end of
  most coding sessions. You do not want it changing every time you change a
  function signature or add a class method!

# Sample Project Codebase Summary

## Project Overview

(Very brief explanation of the project's purpose; no design or implementation details)

## Structure

- `project_name` - top-level package
    - `project_name.api`` - API interface layer
        - `class Api` - Defines an API and its available endpoints
        - `class Endpoint` - Definies a particular endpoint, its inputs and outputs
        - `class Session` - Holds authentication and other session state
    - `project_name.cli` - Command-line interface
        - ...classes...
    - `project_name.operations`
        - ...classes...

See how this ONLY shows you which files have which functionality. You're going
to have to read the files anyway when you edit them, so we don't duplicate
any more details in here!

## Design principles

High-level principles that must be maintained during development, e.g.,

- MVC architecture
    - **Model**: `api` module
    - **View**: `operations` module
    - **Controller**: `cli` and `gui` modules

## Tooling

Example:

- `uv` for dependency, virtual environment, and build management
- Linters
    - ruff
    - isort
    - mypy

## Coding standards

- Type hints everywhere
- Modern Python syntax:
    - Do not import from `typing_extensions`.
    - Do not use `List`, `Dict`, etc. when `list` and `dict` are now valid.
    - `<type> | None`, not `Optional[<type>]`.
- CamelCase for classes, even with acronyms, e.g. `ApiEndpointUrl`, not `APIEndpointURL`.

