# virgilio-os1

Plugin per Claude che dà accesso alla documentazione ufficiale di **OS1** tramite **Virgilio**, il server MCP di **SCAO Informatica**.

Sviluppato e mantenuto da SCAO Informatica (https://www.scao.it).

## Cos'è OS1

**OS1** è un gestionale ERP prodotto da **Open Source Italia** (OSItalia) e distribuito tramite software house partner e rivenditori. Esiste in due versioni, **OS1** e **OS1 Enterprise**. Il manuale in linea descrive tutte le funzioni di OS1 Enterprise, e chi usa OS1 trova solo le finestre e le voci di menù previste dalla propria versione.

Attorno al gestionale ci sono moduli e software collegati, che la documentazione tratta in schede operative dedicate:

- **OS1Box**: Fatture, Intra, Ordini, Fiscale, Open Banking
- **OS1 CRM**
- integrazione con **Arxivar**

## Cos'è Virgilio

**Virgilio** è il server MCP di SCAO Informatica che espone la documentazione di OS1 (manuale in linea e schede operative) con ricerca testuale. L'assistente la consulta, legge i documenti pertinenti e risponde citando la fonte. La documentazione è in italiano.

## Cosa fa il plugin

- Collega Claude al server MCP Virgilio (`https://os1.ai.scao.it/mcp/`).
- Include la skill `os1-docs`, che guida l'assistente: ricerca in italiano, lettura dei documenti, risposta con citazione dell'URL, nessuna risposta a memoria.

## Come ottenere l'accesso

L'accesso a Virgilio non è libero: l'indirizzo email dell'utente deve essere **autorizzato**.

1. Contatta il tuo **referente commerciale** SCAO Informatica e chiedi l'abilitazione della tua email.
2. Una volta autorizzata, installa il plugin e accedi con quella stessa email quando il server lo richiede.

Se la connessione viene rifiutata o non compaiono risultati, la causa più probabile è che l'email non sia ancora stata abilitata.

## Esempi di domande

- "Come si configura OS1BoxFatture?"
- "Cosa significa questo messaggio di errore in OS1?"
- "In quale tabella del database sono salvati i clienti?"
- "Come si importano i codici articolo in OS1?"

## Contenuto del repository

| File | Scopo |
|---|---|
| `.claude-plugin/plugin.json` | Manifest del plugin |
| `.mcp.json` | Collega il server MCP `os1-virgilio` |
| `skills/os1-docs/SKILL.md` | Guida all'uso della documentazione |

## Tool esposti dal server

- `search(query)`: cerca nella documentazione (query in italiano)
- `fetch(id)`: testo integrale di un documento
- `view_images(urls)`: mostra fino a 2 screenshot come immagini

## Note

- L'endpoint richiede lo slash finale (`/mcp/`); senza risponde con un redirect 307.
- Il plugin non è ancora stato provato in un'installazione reale.

## Chi siamo

**SCAO Informatica** sviluppa e mantiene Virgilio e questo plugin. Sito aziendale: https://www.scao.it

## Contatti

SCAO Informatica: https://www.scao.it
Repository del plugin: https://github.com/scao-ita/VirgilioClaudePlugin
Per segnalazioni e suggerimenti sulla documentazione di OS1 ci si rivolge al proprio rivenditore di fiducia.
