---
tags: [memoria, decisioni]
status: active
---

# Decisioni

Scelte strategiche, operative o di prodotto prese da {{ COMPANY_NAME }}.

Gli agenti leggono questa cartella prima di proporre alternative
già scartate o contraddire direzioni già stabilite.

## Come si popola

L'agente `memory-updater` estrae decisioni dai meeting log in `04_Knowledge/meetings/`
e le consolida qui. Formato: un file per decisione, nome `YYYY-MM-DD-slug-decisione.md`.
