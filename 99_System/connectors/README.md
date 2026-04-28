# 99_System/connectors — MCP Connector templates

Template `.json` per i connettori MCP più richiesti. Ogni file è un
"plugin pronto" da copiare in `.mcp.json` del cliente.

## Connettori disponibili

| File | Servizio | Casi d'uso tipici |
|---|---|---|
| slack.json | Slack | Notifiche team, leggi canali, post message auto |
| google-drive.json | Google Drive | Citazione documenti, knowledge migration |
| fathom.json | Fathom | Meeting recording → notes auto |
| notion.json | Notion | Sync bidirezionale, migration |
| github.json | GitHub | Read repos/PR/issues (clienti tech) |
| calendar-google.json | Google Calendar | Schedule meeting, conflict check |
| stripe.json | Stripe | Tracking ricavi, invoice |
| linear.json | Linear | Project tracking (startup tech) |

## Come abilitare un connettore per un cliente

1. Apri `.mcp.json.example` del vault cliente
2. Copia la chiave del connettore desiderato dal file `.json` corrispondente
3. Salva come `.mcp.json` (gitignored!)
4. Cliente fornisce le credenziali → metti in 1Password
5. `claude` userà automaticamente il connettore

## Setup credenziali per cliente

1. Per ogni connettore, segui `_setup_required` nel file
2. Salva le credenziali nel vault 1Password del cliente
3. Configura le env var nel `.env` locale del Mac che esegue `claude`
4. Test: `claude -p "test connessione [servizio]"`

## Connettori non ancora qui (roadmap)

- Outlook / Microsoft 365
- Airtable
- HubSpot CRM
- Pipedrive
- Asana
- Trello
- Discord
- Zapier (meta-connettore)
