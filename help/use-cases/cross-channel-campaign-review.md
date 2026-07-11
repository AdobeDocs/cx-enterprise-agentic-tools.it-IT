---
title: Eseguire una revisione di una campagna cross-channel
description: Utilizza CX Enterprise MCP in una singola sessione di intelligenza artificiale per ottenere una visione unificata dello stato delle campagne AJO, CJA e Real-Time CDP tra percorsi, pubblico e prestazioni.
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '1412'
ht-degree: 5%

---


# Eseguire una revisione di una campagna cross-channel

<!-- last-modified: 2026-05-21 -->

![Esegui una revisione campagna cross-channel](https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review)

Un quadro completo dello stato della campagna richiede dati provenienti da più sistemi: percorsi attivi da AJO, stato di attivazione del pubblico da Real-Time CDP e metriche delle prestazioni da CJA. In questa procedura dettagliata viene illustrato come connettere tutti e tre in una singola sessione di intelligenza artificiale, in modo da poter passare dallo stato del percorso all’integrità del pubblico ai trend di prestazioni in una conversazione anziché in tre strumenti separati.

| Dettagli scenario | |
| --- | --- |
| Applicazioni aziendali CX | [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home), [Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/analytics-platform/using/cja-overview/cja-overview), [Real-Time CDP](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/home) |
| Strumenti agenti | [MCP aziendale CX](../tools/mcp-servers.md#cx-enterprise-mcp-servers) |
| Pubblico | Manager campagne, operazioni di marketing |
| Prerequisito | Client di intelligenza artificiale compatibile con MCP, accesso ad AJO, CJA e Real-Time CDP |

Ogni passaggio mostra un prompt rappresentativo e un esempio di risposta di IA. Segue una sezione **Ulteriori operazioni da eseguire** per ulteriori informazioni nella stessa sessione.

## Prima di iniziare

>[!BEGINTABS]

>[!TAB Claude.ai]

Collegare CX Enterprise MCP come connettore personalizzato. Una connessione consente di accedere agli strumenti di AJO, CJA e Real-Time CDP.

1. Vai a **Impostazioni > Integrazioni** in Claude.ai.
2. Seleziona **Aggiungi connettore personalizzato** e immetti l&#39;URL del server: `https://cx-enterprise.adobe.io/mcp`
3. Seleziona **Connetti** e accedi con il tuo Adobe ID.

Configurazione completa: [Documentazione dei connettori personalizzati Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Collegare CX Enterprise MCP utilizzando la modalità di sviluppo ChatGPT (è necessario un piano Pro, Plus, Business, Enterprise o Education).

1. Abilita la **modalità sviluppatore** nelle **impostazioni ChatGPT**.
2. Vai a **Impostazioni > Integrazioni** e seleziona **Aggiungi connettore personalizzato > Server MCP remoto**.
3. Immettere l&#39;URL del server: `https://cx-enterprise.adobe.io/mcp`
4. Seleziona **Connetti** e accedi con il tuo Adobe ID.

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Altri client di IA]

Usare Gemini, Microsoft Copilot, Cursore, Claude Code o un altro ambiente compatibile con MCP? Connettersi a CX Enterprise MCP utilizzando questo endpoint:

```
https://cx-enterprise.adobe.io/mcp
```

Istruzioni di installazione complete per tutti i client supportati: [Connetti al client di intelligenza artificiale](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata ai tuoi ambienti AJO, CJA e Real-Time CDP. La scelta dell’organizzazione sbagliata è la fonte più comune di errori di autenticazione.
>
>Alla prima connessione, il client di intelligenza artificiale può richiedere di selezionare un’organizzazione IMS o specificare una sandbox. Una volta impostato tale contesto, il server MCP lo utilizza per il resto della sessione.
>
>Alcuni strumenti richiedono la tua approvazione prima di essere eseguiti. Rivedi la richiesta e approva o rifiuta. Non viene intrapresa alcuna azione senza la tua conferma.

## Passaggio 1: rivedere percorsi e campagne attivi

Inizia con AJO per stabilire cosa è attualmente in esecuzione. Sapere quali percorsi sono live e modificati di recente fornisce le basi per il resto della recensione.

```
What journeys are currently active in AJO?
```

+++Vedi una risposta di esempio

Trovati 8 percorsi attivi nella tua organizzazione AJO:

| Percorso | Canale/i | Ultima modifica |
| --- | --- | --- |
| Serie introduttiva: nuovi membri | E-mail, push | 18 maggio 2026 |
| Follow-up post-acquisto | E-mail, SMS | 14 maggio 2026 |
| Nuovo coinvolgimento fedeltà | E-mail | 20 maggio 2026 |
| Carrello abbandonato: 24 ore | E-mail, SMS | 10 maggio 2026 |
| Promozione di primavera | E-mail, push | 19 maggio 2026 |
| Win-Back: 90 giorni inattivi | E-mail | 28 aprile 2026 |
| Premio Compleanno | E-mail | 15 aprile 2026 |
| Nuovo coinvolgimento: rinuncia push | SMS | 12 maggio 2026 |

3 percorsi sono stati modificati negli ultimi 7 giorni. Vuoi dettagli su uno di questi?

+++


## Passaggio 2: verificare lo stato di attivazione del pubblico

Con i percorsi in vista, verifica che i tipi di pubblico che alimentano tali campagne fluiscano correttamente nelle loro destinazioni.

```
Show me the activation status for the high-value loyalty segment.
```

+++Vedi una risposta di esempio

**Segmento fedeltà di valore elevato**: stato di attivazione tra le destinazioni:

| Destinazione | Stato | Ultima esecuzione riuscita | Dimensione del pubblico |
| --- | --- | --- | --- |
| Google Ads | Attivo | 21 maggio 2026 02:14 AM | 48,320 |
| Meta Ads | Attivo | 21 maggio 2026 01:58 AM | 48,295 |
| Salesforce Marketing Cloud | Attivo | 20 maggio 2026 11:30 PM | 47,940 |
| Adobe Target | Attivo | 21 maggio 2026 12:00 AM | 48,320 |

Non sono stati rilevati errori di flusso di dati. Tutte le attivazioni completate nelle ultime 3 ore.

+++


## Passaggio 3: estrarre le metriche delle prestazioni da CJA

Una volta stabilito il contesto di percorso e pubblico, utilizza CJA per valutare in che modo tali campagne si stanno convertendo e dove il coinvolgimento si interrompe.

```
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
Show me click-through and conversion rates for the [campaign name] campaign over the last 30 days.
```

+++Vedi una risposta di esempio

**Campagna di ricoinvolgimento fedeltà**: dal 21 aprile al 21 maggio 2026:

| Canale | Invia | CTR | Conversioni | Conv. Tasso |
| --- | --- | --- | --- | --- |
| E-mail | 48,320 | 8.4% | 1,973 | 4.1% |
| Push | 31,200 | 12.1% | 987 | 3.2% |

Tasso di conversione combinato: 3,8%. Il CTR dell’e-mail è aumentato dell’1,2% rispetto al periodo di 30 giorni precedente. Le conversioni push sono piatte.

+++


## Passaggio 4: sintetizzare un riepilogo dello stato di una campagna

Chiedi al tuo client AI di unire l’immagine tra tutte e tre le sorgenti e di far emergere tutto ciò che richiede attenzione.

```
Give me a summary of our campaign health: what is running, which audiences are activated, and how performance looks against last month.
```

+++Vedi una risposta di esempio

Ecco il riepilogo attuale sullo stato della campagna in AJO, Real-Time CDP e CJA:

**percorsi attivi:** 8 in diretta, 3 modificati questa settimana. Il percorso di ricoinvolgimento fedeltà è l’ultimo aggiornamento.

**Attivazione pubblico:** tutti i segmenti scorrono correttamente su 4 destinazioni. Non sono stati rilevati errori di flusso di dati.

**Prestazioni:** il CTR dell&#39;e-mail è attivo nelle campagne fedeltà. La conversione push è piatta. Nessun canale è in declino significativo.

**Contrassegni per l&#39;attenzione:**

- Il percorso di Win-Back (90 giorni inattivi) è stato modificato l’ultima volta 23 giorni fa e non è stato rivisto di recente.
- Il tasso di conversione push è rimasto invariato per 3 periodi consecutivi, vale la pena rivedere i messaggi o i tempi.

Nessun problema critico rilevato. Due elementi sopra giustificano una revisione prima del prossimo lancio della campagna.

+++


È qui che l’approccio multiserver ripaga: i motivi dei client di intelligenza artificiale in configurazione di percorso, stato del pubblico e dati sulle prestazioni in un’unica conversazione.

## Passaggio 5: intervenire su ciò che è stato trovato

La recensione ha fatto emergere due elementi. Chiedi al tuo client di intelligenza artificiale di aiutarti a definire la priorità e a indirizzare ciascuno di essi.

```
For each flag you identified, what should I do and where should I go to do it?
```

+++Vedi una risposta di esempio

Ecco un piano di azione prioritario per i due flag:

**1. Percorso Win-Back: rivedere le condizioni di reinserimento (AJO MCP, quindi applicazione AJO se sono necessarie modifiche)**

Il percorso Win-Back non viene modificato dopo 23 giorni. Chiedimi di esaminare le condizioni di rientro e la logica di uscita attuali. Se le condizioni sembrano obsolete o errate, le modifiche strutturali al flusso di percorso richiedono l’apertura di AJO. Il limite di frequenza e gli aggiornamenti del pubblico possono essere effettuati qui.

**2. Effettua un push flat per 3 periodi: aggiorna i messaggi o verifica una variante**

La conversione Flat in genere segnala un senso di affaticamento del messaggio o una mancata corrispondenza tra l’offerta e il pubblico. Due percorsi:

- **Aggiorna contenuto push ora (AEM MCP):** Se le notifiche push sono collegate a una pagina di destinazione, aggiungi il server AEM Content MCP e aggiorna la copia della pagina o CTA senza passare da uno strumento all&#39;altro.
- **Esegui un test A/B push (applicazione AJO):** Crea una variante a livello di campagna con messaggi diversi per isolare se si tratta di contenuto o targeting. Questo richiede di andare direttamente ad AJO.

Con quale vuoi iniziare?

+++


## Risultati ottenuti

Hai eseguito una revisione dello stato di salute di una campagna cross-channel collegando AJO, Real-Time CDP e CJA a una singola sessione di intelligenza artificiale. Anziché aprire tre applicazioni e assemblare manualmente un&#39;immagine, in una conversazione è stato possibile spostarsi tra lo stato del percorso, l&#39;attivazione del pubblico e i dati sulle prestazioni. Il riepilogo sintetico offre ai manager delle campagne un percorso più rapido per identificare ciò che funziona, ciò che richiede un aggiustamento e dove concentrarsi successivamente.

## Più risultati da ottenere

Con AJO, CJA e Real-Time CDP connessi nella stessa sessione, puoi andare ben oltre la procedura dettagliata. Espandi uno scenario qui sotto per visualizzare i prompt che puoi provare.

+++Scopri esattamente cosa è in esecuzione prima di lanciare qualcosa di nuovo

La sovrapposizione di percorsi, campagne modificate di recente e canali non esaminati può influire su un nuovo lancio. Questi prompt forniscono un&#39;immagine chiara dello stato corrente prima di aggiungere qualsiasi elemento.

**Richieste**

```
Which journey has the most active profiles right now?
```

```
Show me all journeys modified in the last 7 days.
```

```
Which campaigns are scheduled to end this week?
```

```
Are any journeys targeting the same segment as the campaign I'm about to launch?
```

+++

+++Assicurati che il pubblico raggiunga le destinazioni giuste

I problemi di attivazione non sono visibili: un segmento smette di scorrere e la campagna viene inviata a un elenco più piccolo senza alcun avviso. In questo modo vengono visualizzati gli spazi vuoti e gli errori prima che influiscano sui risultati.

**Richieste**

```
Which audiences have grown the most in the last 30 days?
```

```
Are there any dataflow errors across my active destinations?
```

```
How many records were exported to each destination in the last 7 days?
```

```
Are there any audiences with no active destinations?
```

+++

+++Comprendere cosa funziona e dove concentrarsi

Le tendenze delle prestazioni nei vari canali indicano dove investire e cosa recuperare. Queste richieste ti aiutano a identificare quali sono i risultati più significativi e dove l&#39;attenzione del trimestre successivo dovrebbe andare.

**Richieste**

```
Show me email performance trends for the last 90 days.
```

```
Which campaigns are underperforming against their conversion targets?
```

```
What is the average revenue per conversion this month compared to last month?
```

```
Which channel has the highest conversion rate across all active campaigns?
```

+++


## Ulteriori informazioni

| Risorsa | Cosa troverai |
| --- | --- |
| [Documentazione di AJO](https://experienceleague.adobe.com/it/docs/journey-optimizer/using/ajo-home){target="_blank"} | Documentazione completa dell’applicazione AJO |
| [Server AJO MCP nel Registro di sistema AI](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server){target="_blank"} | Strumenti e disponibilità del server AJO MCP |
| [Server MCP CJA nel Registro di sistema AI](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | Strumenti e disponibilità del server CJA MCP |
