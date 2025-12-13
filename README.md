# selfie-packages

Package files for turboladen/selfie

## Guidelines

The following are guidelines (for myself) to follow when considering which package manager to use
for installing a package.

### General CLI Utilities

Prefer to install general CLI utilities (ex. `bat`) using the OS package manager simply because it's
probably better set up to generate post-install artifacts (ex. man pages, shell completions, etc.).

### Language Tools

This category mainly relates to tools I use from `neovim`; for example:

- LSP servers
- linters
- test utilities

These should be installed with performance and portability in mind, so:

- Prefer to install in such a way that's not dependent on a specific version of the underlying
  language the tool was built in. For example, if I install `eslint` via `npm`, it's immediately
  tied to the version of `node` that that `npm` executable is tied to. If I then use a different
  version of `node` for a project, I'm stuck at a crossroads.
- Prefer to install using the means that imposes the least amount of dependencies.
- Prefer to install using the means that allows for the most optimized execution of the tool
  (optimized for speed and resource utilization)
