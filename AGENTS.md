# Agent Guidelines

## Project Overview

This is a YAML-based package definition repository for the selfie project. Contains package
definitions that specify installation methods across different environments (macos-home, macos-work,
arch-home).

## Commands

- Format code: `dprint fmt`
- Check formatting: `dprint check`
- No build, test, or lint commands (data-only repository)

## Code Style

- **YAML formatting:** 80 character line width, format comments (enforced by dprint)
- **Markdown formatting:** 100 character line width, always wrap text (enforced by dprint)
- **YAML structure:** Follow existing pattern with `name`, `version`, `homepage`, `description`,
  YAML anchors for reusability, and `environments` sections
- **Multi-line scripts:** Start with `set -e`, use `|` for YAML multi-line strings
- **Verification commands:** Use `command -v <tool>` or existence tests in `check` fields

## Package Manager Selection

- **General CLI utilities:** Prefer OS package manager (better man pages, shell completions)
- **Language tools (LSP servers, linters):** Install with performance and portability in mind; avoid
  tying to specific language versions; minimize dependencies; optimize for speed and resource
  utilization
