---
name: os1-docs
description: Usa questa skill per domande su OS1, il gestionale ERP di OSItalia: funzionalità, moduli, tabelle del database, procedure e schede operative, messaggi di errore, configurazioni, OS1Box (Fatture, Intra, Ordini, Fiscale, Open Banking), OS1 CRM, integrazione Arxivar. Cerca nella documentazione ufficiale tramite il server MCP Virgilio.
---

# Documentazione OS1

OS1 è il gestionale ERP di Open Source Italia (OSItalia), in versione OS1 e OS1 Enterprise. Questo plugin è fornito da SCAO Informatica (https://www.scao.it) tramite Virgilio, il suo server MCP.

Rispondi alle domande su OS1 usando solo la documentazione ufficiale esposta dal server MCP `os1-virgilio`, non la memoria.

## Procedura

1. **`search`**: formula la query in **italiano**, con parole chiave brevi (modulo, funzione, messaggio di errore, nome tabella). Se i risultati non sono pertinenti, riformula o fai più ricerche per modulo.
2. **`fetch`**: leggi con l'`id` restituito i documenti più rilevanti prima di rispondere.
3. **`view_images`**: usala solo se la domanda riguarda cosa si vede a schermo (campi, pulsanti, colonne, layout). Usa gli URL di `metadata.images` di `fetch`, al massimo 2 per chiamata e solo quelli pertinenti.
4. **Rispondi** in italiano e **cita sempre la fonte** con l'`url` del documento.

## Accesso negato

L'accesso a Virgilio richiede che l'email dell'utente sia autorizzata. Se il server rifiuta la connessione o risponde con un errore di autorizzazione, spiega all'utente che deve contattare il proprio referente commerciale SCAO Informatica per farsi abilitare l'email. Non tentare di aggirare il blocco e non rispondere a memoria al posto della documentazione.

## Regole

- Se la documentazione non contiene la risposta, dillo chiaramente: non inventare procedure, campi o nomi di tabella.
- Se più documenti si contraddicono, riportali entrambi con le rispettive fonti.
- Non riportare documenti interi: sintetizza i passaggi utili e rimanda all'`url`.
