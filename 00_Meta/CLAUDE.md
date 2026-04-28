# CLAUDE.md — Convenzioni vault {{ COMPANY_NAME }}

Tutto l'output di Claude Code in questo vault deve rispettare queste regole.

## Identità

- **Azienda**: {{ COMPANY_NAME }}
- **Vertical**: {{ VERTICAL }}
- **Team size**: {{ TEAM_SIZE }} persone
- **Tone**: italiano, diretto, professionale ma non corporate

## Output Claude

Tutto l'output va in `03_Projects/<nome-progetto>/` o in `04_Knowledge/<categoria>/`.
Mai in `00_Inbox/` (è quick capture solo per gli umani).

## Convenzioni nomi

- File: `kebab-case` (es. `lead-priority-q2.md`)
- Meeting: `YYYY-MM-DD-titolo-meeting.md`
- Daily: `YYYY-MM-DD.md`

## Frontmatter obbligatorio

```yaml
---
tags: []
status: draft | active | archived
created: YYYY-MM-DD
project: <nome>
---
```

## Link interni

- `[[wikilink]]` per riferimenti interni
- `#kebab-tag` per tag

## Sicurezza

- Mai dati personali sensibili in chiaro
- Mai API keys / credenziali — vivono in 1Password Teams
- File `.env*` sempre gitignored

## Cose vietate

- Non eliminare file (sposta in `06_Archive/` se serve)
- Non condividere screenshot del vault con esterni senza review
