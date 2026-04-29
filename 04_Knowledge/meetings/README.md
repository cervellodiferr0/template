---
tags: [knowledge, meetings]
status: active
---

# Meeting Log

Tutti i meeting note del vault, generati da `meeting-summarizer`.

## Formato nome file

`YYYY-MM-DD-titolo-meeting.md`

Esempi:
- `2026-05-12-strategy-call-team.md`
- `2026-05-15-onboarding-cliente-acme.md`
- `2026-05-20-weekly-sync.md`

## Frontmatter standard

```yaml
---
tags: [meeting, <vertical-specifico>]
status: active
created: YYYY-MM-DD
partecipanti: [Nome1, Nome2]
durata: 45min
tipo: strategy | weekly | client | onboarding | retrospettiva
---
```

## Come si popola

**Con Fathom (automatico):**
Il connettore Fathom + `meeting-summarizer` generano il file automaticamente
al termine di ogni call. Zero effort manuale.

**Senza Fathom (manuale):**
1. Copia il transcript dalla call
2. Chiedi a Claude: `"Usa meeting-summarizer su questo transcript: [incolla]"`
3. Il file viene creato in questa cartella

## Come gli agenti usano questi file

- `memory-updater` li scansiona ogni 2 settimane per estrarre decisioni e pattern
- `orchestrator` li cerca quando risponde a "cosa abbiamo deciso su X?"
- `planner` li usa per aggiornare lo stato dei progetti
