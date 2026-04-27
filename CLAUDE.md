# CLAUDE.md

This file is the persistent "mind" of the EvenRealitiesHelper repository. Claude Code auto-loads it at the start of every session in this repo. Treat it as the canonical place to record what this project is, how it is built, and every major change worth remembering across sessions.

## Project

**EvenRealitiesHelper** — a helper project for Even Realities. Scope, language, and architecture are not yet established; fill in this section as the first real feature lands.

## Branches

- `main` — stable.
- `claude/add-evenhub-plugin-lyHjp` — sets up the `everything-evenhub` Claude Code plugin and this CLAUDE.md.

## Tooling

### Claude Code plugin

The repo is wired to the `everything-evenhub` plugin from the `even-realities/everything-evenhub` marketplace. Configuration lives in `.claude/settings.json`:

- `extraKnownMarketplaces.everything-evenhub` registers the marketplace by GitHub `owner/repo`.
- `enabledPlugins["everything-evenhub@everything-evenhub"]` enables the plugin for everyone who checks out the branch.

On first launch in a fresh clone, Claude Code fetches the marketplace metadata and activates the plugin. Skills appear under the `everything-evenhub:` namespace. Run `/reload-plugins` to pick up changes mid-session.

## Working agreements for Claude

1. **Read this file first.** Before non-trivial work, skim the Major Updates log so you do not redo or contradict prior decisions.
2. **Update this file on every major change.** A change is "major" if it would surprise a teammate who left for a week — new dependencies, new top-level directories, new build/test commands, new environment requirements, plugin/tooling changes, schema migrations, externally visible API changes, or shifts in architectural direction. Bug fixes and routine refactors do not need entries.
3. **Append, do not rewrite history.** Add a new dated entry to the bottom of the Major Updates log with: date, branch, one-line summary, and a short "why". Update the Project, Branches, or Tooling sections in place when the current state changes.
4. **Keep it short.** If a section grows past a screen, split details into a dedicated doc and link it.
5. **Never commit secrets here.** Reference env var names, never values.

## Major Updates

> Format: `YYYY-MM-DD — <branch> — <summary>`. One or two sentences of "why" underneath. Newest entries at the bottom.

- **2026-04-27 — claude/add-evenhub-plugin-lyHjp — Added `everything-evenhub` plugin and bootstrapped CLAUDE.md.**
  Project-scoped `.claude/settings.json` registers the marketplace and enables the plugin for the whole branch so the team and future Claude Code sessions get the same skills automatically. CLAUDE.md established as the repo's running memory.
