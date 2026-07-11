# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

This is **not a software project** — it is a personal knowledge vault ("jarvis-os-vault") of Markdown notes, organized in an Obsidian/PKM style. There are no build, lint, or test commands; there is no package manager or code tooling.

## Vault structure

Content is organized into numbered top-level folders that define a processing pipeline for notes:

- `00-Inbox/` — unprocessed captures; notes land here first before being triaged
- `01-Daily/` — daily notes
- `02-Hubs/` — hub/index notes that link related notes together (maps of content)
- `03-Notes/` — the main body of processed, permanent notes
- `04-Projects/` — notes tied to active projects
- `05-Templates/` — note templates
- `99-Archive/` — inactive/retired material

## Working in this vault

- All content is Markdown. Notes may use Obsidian conventions such as `[[wikilinks]]` and YAML frontmatter.
- When creating a note, place it in the folder matching its role above; use `00-Inbox/` when the destination is unclear.
- Git tracks only files, so empty folders are invisible in git — the structure above is the source of truth for the vault layout.
