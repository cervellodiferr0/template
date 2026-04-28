# Onboarding — {{ COMPANY_NAME }}

Benvenuto nel vault aziendale.

## Setup (~10 min)

```bash
curl -fsSL <SETUP_SCRIPT_URL> | bash
```

Lo script:
1. Installa Obsidian (se mancante)
2. Installa Claude Code CLI
3. Configura cartella vault locale

Poi:

1. Apri Obsidian → "Apri vault" → seleziona la cartella creata
2. Login Obsidian Sync (credenziali da {{ ADMIN_NAME }} via 1Password)
3. Inserisci passphrase del vault (idem)
4. `claude login` (browser auth col tuo account aziendale)

## Regole base

1. Mai dati personali sensibili in chiaro
2. Mai segreti / API key — vivono in 1Password
3. Frontmatter YAML obbligatorio
4. `[[wikilink]]` per link interni, `#tag` per categorizzare
5. Output Claude → in `03_Projects/` o `04_Knowledge/`, mai in `00_Inbox/`

## Supporto

- Setup tecnico → {{ ADMIN_CONTACT }}
- Strategy → {{ FOUNDER_CONTACT }}
- Tutto il resto → {{ TEAM_CHANNEL }}
