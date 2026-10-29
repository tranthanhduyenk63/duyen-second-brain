# Second Brain: rules for Claude

This is an Obsidian vault of my software engineering knowledge and experience.

## Structure
- `00-inbox/`: drafts awaiting my review
- `10-sources/`: books, articles, talks, courses
- `20-concepts/`: one concept per note
- `30-maps/`: maps of content (MOCs) and Canvas files
- `40-practice/`: concrete experiences: what I did, what happened, lessons
- `50-work/`: `projects/`, `adrs/`, `incidents/`
- `daily/`: daily notes
- `templates/`: note templates (concept, practice, project, source)
- `ai/`: Claude's working area

## Rules
1. **Write only to `ai/` and `00-inbox/`** unless I explicitly approve moving or editing notes elsewhere.
2. **Never invent experience.** Practice, project, and incident notes contain only what I described. If something is unknown, leave a `TODO(ask)` rather than filling it in.
3. **Search before creating a concept.** Check `20-concepts/` and `00-inbox/` for an existing note (including synonyms and aliases) before creating a new one; extend the existing note instead.
4. **Use established industry terms for concept names.** Name the note with the recognised term (e.g. "Event-Carried State Transfer", not "Event-Driven Data Synchronization"), and record where it comes from in a `source:` frontmatter field (author, book, or standard). Put my own phrasing and synonyms in `aliases:`. Coin a name only if no established term exists, and then add `coined: true`.
5. **One concept per note.** Split compound ideas into separate notes and link them.
6. **Use `[[wikilinks]]`** for all internal links. Filenames are Title Case, e.g. `Idempotency.md`.
7. **No company secrets or credentials.** No internal hostnames, customer names, proprietary metrics, keys, or tokens. Generalize (e.g. "a payments company", "~10k rps").
8. Use the templates in `templates/` and their YAML frontmatter (`type`, `tags`, `created`, plus `aliases`, `source`, `coined` for concepts).
9. Commit after each approved batch with a clear message.
