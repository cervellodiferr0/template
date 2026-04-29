---
tags: [memoria, sistema, agenti]
status: active
created: {{ SETUP_DATE }}
---

# 10_Memoria — Memoria persistente degli agenti

Questa cartella è il **layer di memoria a lungo termine** del vault.
Gli agenti leggono e scrivono qui per accumulare contesto nel tempo.

> Regola fondamentale: **nessun umano deve scrivere direttamente qui**.
> Solo gli agenti. Gli umani leggono, al massimo correggono.

---

## Struttura

```
10_Memoria/
├── decisioni/        → scelte strategiche prese, con data e motivazione
├── preferenze/       → stile, formati, abitudini emerse dall'uso
├── pattern/          → insight ricorrenti su processi, clienti, mercato
└── contesto/         → fatti aziendali consolidati (non cambiano spesso)
```

---

## Come gli agenti usano questa cartella

### Leggere prima di agire
Ogni agente deve controllare la sezione rilevante prima di rispondere:
```
Prima di generare output, leggi:
- 10_Memoria/preferenze/ → per rispettare lo stile consolidato
- 10_Memoria/decisioni/ → per non contraddire scelte già prese
- 10_Memoria/contesto/ → per avere il quadro aggiornato
```

### Scrivere dopo aver imparato
Quando emerge qualcosa di nuovo e riutilizzabile:
```
Dopo ogni interazione significativa, valuta:
- C'è una nuova preferenza da tracciare? → 10_Memoria/preferenze/
- È stata presa una decisione importante? → 10_Memoria/decisioni/
- Hai identificato un pattern ripetitivo? → 10_Memoria/pattern/
- Hai appreso un fatto aziendale stabile? → 10_Memoria/contesto/
```

---

## Formato standard nota di memoria

```markdown
---
tipo: decisione | preferenza | pattern | contesto
data: YYYY-MM-DD
agente: nome-skill-che-ha-scritto
confidenza: alta | media | bassa
---

## Fatto

[cosa è stato appreso, max 3 righe]

## Contesto

[perché è rilevante, da dove emerge]

## Applicazione

[come deve influenzare i comportamenti futuri degli agenti]
```

---

## Manutenzione

Lo skill `memory-updater` consolida queste note ogni 2 settimane.
Mateo può correggere o eliminare manualmente note errate.
