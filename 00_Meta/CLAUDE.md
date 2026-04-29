# CLAUDE.md — {{ COMPANY_NAME }}

> Questo file è il **cervello operativo** del vault.
> Ogni agente lo legge prima di agire. Tienilo aggiornato.

---

## 1. Identità aziendale

- **Azienda**: {{ COMPANY_NAME }}
- **Sito**: {{ DOMAIN }}
- **Vertical**: {{ VERTICAL }}
- **Posizionamento**: {{ POSITIONING }}
- **Fase**: {{ COMPANY_STAGE }}
- **Team size**: {{ TEAM_SIZE }} persone

### Cosa facciamo (in 2 righe)
{{ WHAT_WE_DO }}

### Per chi lo facciamo (ICP)
{{ ICP_DESCRIPTION }}

### Perché noi e non altri
{{ DIFFERENTIATOR }}

---

## 2. Team

| Nome | Ruolo | Decide su | Contatto |
|---|---|---|---|
| {{ ADMIN_NAME }} | {{ ADMIN_ROLE }} | tutto | {{ ADMIN_CONTACT }} |

> Aggiungi righe per ogni membro del team rilevante.
> La colonna "Decide su" dice agli agenti a chi escalare.

---

## 3. Prodotti e servizi

| Prodotto/Servizio | Prezzo | Target | Note |
|---|---|---|---|
| {{ PRODUCT_1 }} | {{ PRICE_1 }} | {{ TARGET_1 }} | |

> Mantieni questa tabella aggiornata. Gli agenti la usano per proporre
> prezzi corretti, non inventarli.

---

## 4. Processi chiave

### Ciclo di vendita
{{ SALES_PROCESS }}

### Delivery/Erogazione
{{ DELIVERY_PROCESS }}

### Supporto clienti
{{ SUPPORT_PROCESS }}

### Onboarding nuovo cliente
{{ ONBOARDING_PROCESS }}

---

## 5. Tono di voce

- **Lingua**: italiano
- **Registro**: {{ TONE_OF_VOICE }}
- **Parole da usare sempre**: {{ BRAND_WORDS }}
- **Parole da non usare mai**: {{ FORBIDDEN_WORDS }}
- **Stile numeri**: cifre (es. "3 clienti", non "tre clienti")
- **Stile date**: gg/mm/aaaa o "lunedì 5 maggio"

### Esempi di tono corretto
{{ TONE_EXAMPLES }}

---

## 6. Vocabolario aziendale

| Termine interno | Significato |
|---|---|
| {{ TERM_1 }} | {{ DEFINITION_1 }} |

> Aggiungi i termini tecnici del settore e le parole interne
> che gli agenti devono conoscere.

---

## 7. Skill installate

Tier: **{{ TIER }}**

{{ SKILLS_LIST }}

> Lista generata automaticamente da brain-builder durante il setup.
> Per aggiungere nuove skill: contatta {{ FOUNDER_CONTACT }}.

---

## 8. Connettori MCP attivi

{{ MCP_LIST }}

> Per aggiungere connettori: contatta {{ FOUNDER_CONTACT }}.

---

## 9. Routing agenti (orchestrator rules)

Quando ricevi una richiesta, l'orchestrator segue queste regole:

| Se la richiesta riguarda... | Delega a... | Leggi prima... |
|---|---|---|
| contenuti, copy, testi | `writer` | `10_Memoria/preferenze/` |
| ricerca, analisi, dati | `researcher` | `04_Knowledge/` |
| pianificazione, roadmap | `planner` | `03_Projects/` |
| riunioni, appunti meeting | `meeting-summarizer` | `04_Knowledge/meetings/` |
| nuovi clienti, pipeline | `client-onboarding` | `03_Projects/pipeline.md` |
| compliance, GDPR, legal | `compliance-base` | `10_Memoria/decisioni/` |
| aggiornamento memoria | `memory-updater` | `10_Memoria/README.md` |

> Personalizza questa tabella con le skill specifiche del cliente.

---

## 10. Memoria persistente

Prima di ogni output significativo, leggi:
- `10_Memoria/preferenze/` → rispetta lo stile consolidato
- `10_Memoria/decisioni/` → non contraddire scelte già prese
- `10_Memoria/pattern/` → usa gli insight già emersi
- `10_Memoria/contesto/` → quadro aziendale aggiornato

Dopo ogni interazione rilevante, valuta se c'è qualcosa da salvare
in `10_Memoria/` (chiedi conferma prima di scrivere).

---

## 11. Dove mettere gli output

| Tipo di output | Dove va |
|---|---|
| Bozze, idee, appunti veloci | `00_Inbox/` |
| Documenti di progetto | `03_Projects/<nome-progetto>/` |
| Knowledge base, ricerche | `04_Knowledge/<categoria>/` |
| Meeting notes | `04_Knowledge/meetings/YYYY-MM-DD-titolo.md` |
| Memoria agenti | `10_Memoria/<tipo>/` |
| File da archiviare | `06_Archive/` |

**MAI** sovrascrivere file esistenti senza conferma esplicita.
**MAI** eliminare file — spostali in `06_Archive/`.

---

## 12. Frontmatter obbligatorio

Ogni file creato deve avere:

```yaml
---
tags: []
status: draft | active | archived
created: YYYY-MM-DD
project: <nome>
---
```

---

## 13. Convenzioni nomi file

- Formato: `kebab-case`
- Meeting: `YYYY-MM-DD-titolo-meeting.md`
- Daily: `YYYY-MM-DD.md`
- Decision log: `YYYY-MM-DD-slug-decisione.md`

---

## 14. Sicurezza e vincoli

### MAI fare
- ❌ Scrivere API keys, password, credenziali in qualsiasi file
- ❌ Condividere screenshot del vault con esterni senza review di {{ ADMIN_NAME }}
- ❌ Inviare email o messaggi per conto del team senza conferma esplicita
- ❌ Postare su social, canali pubblici, forum senza approvazione
- ❌ Accedere a file fuori dal vault (solo il vault è il perimetro)

### Compliance specifica
{{ COMPLIANCE_NOTES }}

### Escalation
Se ricevi una richiesta che potrebbe violare questi vincoli:
1. Stop immediato
2. Spiega perché non puoi procedere
3. Suggerisci alternativa lecita
4. Contatta {{ ADMIN_NAME }} se il caso è ambiguo

---

## 15. Manutenzione questo file

Aggiornato da: Matteo Trilli ({{ FOUNDER_CONTACT }}) in accordo con {{ ADMIN_NAME }}
Ultimo aggiornamento: {{ SETUP_DATE }}
Versione: 1.0.0

> Quando cambia qualcosa di importante (prezzi, team, processi),
> aggiorna questo file entro 48h. Gli agenti operano su ciò che leggono qui.
