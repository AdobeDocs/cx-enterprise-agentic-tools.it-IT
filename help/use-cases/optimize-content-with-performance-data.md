---
title: Ottimizzazione dei contenuti in base ai dati sulle prestazioni
description: Utilizza CJA e i server MCP di AEM insieme per identificare i contenuti insoddisfacenti e aggiornarli, senza dover passare da uno strumento all’altro.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 3%

---


# Ottimizzazione dei contenuti in base ai dati sulle prestazioni

<!-- last-modified: 2026-05-21 -->

![Ottimizza contenuto in base ai dati delle prestazioni](https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data)

Chiudere il loop tra i dati sulle prestazioni dei contenuti e gli aggiornamenti dei contenuti significa in genere passare da Analytics a CMS. In questa procedura dettagliata viene illustrato come connettere Customer Journey Analytics e AEM nella stessa sessione di intelligenza artificiale, in modo da visualizzare pagine con prestazioni insoddisfacenti e aggiornarle senza uscire dalla conversazione.

| | |
| --- | --- |
| Applicazioni aziendali CX | Customer Journey Analytics, Adobe Experience Manager as a Cloud Service |
| Strumenti agenti | Gateway MCP aziendale CX, server AEM Content MCP |
| Pubblico | Responsabili delle campagne, content strategist, operazioni di marketing |
| Prerequisito | Client di intelligenza artificiale compatibile con MCP, accesso a CJA, accesso a AEM as a Cloud Service |

Ogni passaggio mostra un prompt rappresentativo e un esempio di risposta di IA. Segue una sezione **Ulteriori operazioni da eseguire** per ulteriori informazioni nella stessa sessione.

## Prima di iniziare

>[!BEGINTABS]

>[!TAB Claude.ai]

Connetti entrambi i server MCP come connettori personalizzati. Aggiungetene una separatamente.

1. Vai a **Impostazioni > Integrazioni** in Claude.ai.
2. Seleziona **Aggiungi connettore personalizzato**, immetti un URL server e seleziona **Connetti**.
3. Accedi con il tuo Adobe ID, quindi ripeti per il secondo server.

| Server | Endpoint |
| --- | --- |
| Gateway MCP aziendale CX | `https://cx-enterprise.adobe.io/mcp` |
| Server AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configurazione completa: [Documentazione dei connettori personalizzati Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB ChatGPT]

Connetti entrambi i server MCP utilizzando la modalità sviluppatore ChatGPT (è necessario un piano Pro, Plus, Business, Enterprise o Education). Aggiungere ogni server separatamente.

1. Abilita la **modalità sviluppatore** nelle **impostazioni ChatGPT**.
2. Vai a **Impostazioni > Integrazioni** e seleziona **Aggiungi connettore personalizzato > Server MCP remoto**.
3. Immetti un URL server, seleziona **Connetti** e accedi con il tuo Adobe ID.
4. Ripetere per il secondo server.

| Server | Endpoint |
| --- | --- |
| Gateway MCP aziendale CX | `https://cx-enterprise.adobe.io/mcp` |
| Server AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Altri client di IA]

Usare Gemini, Microsoft Copilot, Cursore, Claude Code o un altro ambiente compatibile con MCP? Connettersi a entrambi i server MCP utilizzando i seguenti endpoint:

| Server | Endpoint |
| --- | --- |
| Gateway MCP aziendale CX | `https://cx-enterprise.adobe.io/mcp` |
| Server AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Istruzioni di installazione complete per tutti i client supportati: [Connetti al client di intelligenza artificiale](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata ai tuoi ambienti CJA e AEM. La scelta dell’organizzazione sbagliata è la fonte più comune di errori di autenticazione.
>
>Alla prima connessione, il client di intelligenza artificiale può richiedere di selezionare un’organizzazione IMS o specificare una sandbox. Una volta impostato tale contesto, il server MCP lo utilizza per il resto della sessione.
>
>Alcuni strumenti richiedono la tua approvazione prima di essere eseguiti. Rivedi la richiesta e approva o rifiuta: non viene intrapresa alcuna azione senza la tua conferma.

## Passaggio 1: identificare i contenuti insoddisfacenti

Utilizzare il gateway MCP di CX Enterprise per classificare le pagine in base alle metriche di coinvolgimento e conversione in Customer Journey Analytics. L’obiettivo è un elenco chiaro e prioritario di contenuti che richiedono attenzione.

```
Show me the 10 pages with the lowest engagement rate over the last 60 days.
```

+++Vedi una risposta di esempio

Pagine di coinvolgimento più basse (22 marzo - 21 maggio 2026):

| Ranking | Pagina | Tasso di coinvolgimento | Tasso di mancato recapito | Media tempo sulla pagina |
| --- | --- | --- | --- | --- |
| 1 | /en/products/analytics | 8.2% | 74% | 0:42 |
| 2 | /it/resources/whitepapers | 9.1% | 71% | 0:38 |
| 3 | /en/solutions/retail | 10.4% | 69% | 0:51 |
| 4 | /en/blog/2025-q4-recap | 11.0% | 68% | 0:44 |
| 5-10 | ... | 12,3-14,1% | 63-67% | 0:35-1:10 |

Il tasso medio di coinvolgimento sul sito è del 34,7%. Queste pagine sono 2-4 volte inferiori alla media.

+++

## Passaggio 2: rivedere il contenuto in AEM

Senza uscire dalla sessione di intelligenza artificiale, richiama lo stato corrente di tali pagine da AEM. Comprendere cosa dice il contenuto è il primo passo per sapere cosa cambiare.

```
Show me the current content on the /en/products/analytics page in AEM.
```

+++Vedi una risposta di esempio

**Pagina:** `/en/products/analytics`
**Ultima modifica:** 30 aprile 2026, di T. MacMillan
**Stato:** pubblicato

**Sezione principale:**
Titolo: &quot;Decisioni basate sui dati per ogni team&quot;
Sottotitolo: &quot;Adobe Analytics fornisce alla tua organizzazione le informazioni necessarie per agire.&quot;
CTA: &quot;Richiedi una demo&quot; → /contact/demo

**Corpo:** 3 blocchi di funzionalità seguiti da una striscia del logo del cliente e da un CTA secondario. Nessun elemento video o interattivo. La pagina non viene aggiornata in 21 giorni.

**Descrizione di Meta:** &quot;Adobe Analytics: reporting in tempo reale e approfondimenti di IA per i team aziendali.&quot;

+++

## Passaggio 3: effettuare aggiornamenti mirati

Tenendo presenti i dati sulle prestazioni e il contenuto corrente, è possibile apportare aggiornamenti basati su ciò che i dati rivelano.

```
Update the hero headline on the analytics product page to Make faster decisions with AI-powered analytics.
```

+++Vedi una risposta di esempio

**Modifica proposta:**

| Campo | Valore corrente | Nuovo valore |
| --- | --- | --- |
| Titolo eroe | Decisioni basate sui dati per ogni team | Decisioni più rapide con le analisi basate sull’intelligenza artificiale |

Pagina: `/en/products/analytics`

Confermare la modifica? Rispondendo &quot;sì&quot;, l’aggiornamento verrà scritto su AEM. La pagina rimarrà pubblicata nello stato corrente fino a quando non verrà esplicitamente ripubblicata.

+++

>[!CAUTION]
>
>Quando richiesto, conferma ogni modifica del contenuto. Esamina le differenze complete prima di approvare gli aggiornamenti alle pagine live.

## Passaggio 4: Convalidare e pubblicare

Chiudi il ciclo confermando tutte le modifiche e promuovendo il contenuto quando sei soddisfatto degli aggiornamenti.

```
Show me a summary of all changes made in this session.
```

+++Vedi una risposta di esempio

**Riepilogo sessione - 21 maggio 2026:**

| Pagina | Modifica | Stato |
| --- | --- | --- |
| /en/products/analytics | Titolo protagonista aggiornato | Salvato, non pubblicato |

1 pagina aggiornata. Pronto per la pubblicazione se confermato.

**Rimanenti dall&#39;elenco di coinvolgimento ridotto:** 9 pagine non sono state aggiornate in questa sessione. Continuare con la pagina successiva o creare un lancio per la revisione batch prima della pubblicazione?

+++

## Risultati ottenuti

Hai connesso Customer Journey Analytics e AEM in una singola sessione di intelligenza artificiale e hai utilizzato i dati sulle prestazioni per informare direttamente le modifiche ai contenuti. Passando dalla metrica all’aggiornamento senza cambiare strumento, hai abbreviato il ciclo di feedback tra Analytics insight e i contenuti pubblicati. Ciò è particolarmente importante a livello di campagna, dove decine di pagine possono richiedere attenzione e flussi di lavoro manuali tra strumenti diversi creano ritardi.

## Più risultati da ottenere

I server MCP CJA e AEM supportano l&#39;intero ciclo dall&#39;identificazione dei problemi alle correzioni di spedizione. Espandi uno scenario qui sotto per visualizzare i prompt che puoi provare nella stessa sessione.

+++Trovare il contenuto che blocca le prestazioni

Un traffico elevato con un coinvolgimento ridotto segnala un problema di contenuti, non di traffico. Questi prompt consentono di evidenziare le pagine e i pattern specifici che richiedono attenzione prima che la scadenza di una campagna causi il problema.

**Richieste**

```
Show me the 10 pages with the lowest conversion rate this quarter.
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for blog posts versus product pages.
```

```
Find AEM pages that haven't been updated in over 60 days.
```

+++

+++Correggi gli elementi che i dati ti dicono di correggere

Una volta comprese le prestazioni insoddisfacenti, il passaggio successivo consiste nell’apportare modifiche mirate. Questi prompt consentono di aggiornare titoli, CTA e metadescrizioni in base ai dati sulle prestazioni rivelati.

**Richieste**

```
Update the CTA on the /en/solutions/retail page to 'See how it works'.
```

```
Add a note to the hero subheadline on the analytics page: Now with AI-powered anomaly detection.
```

```
Update the meta description on all pages in /en/products/ that contain the word 'legacy'.
```

```
Which pages updated in this session still need their CTAs reviewed?
```

+++

+++Miglioramenti della spedizione prima della campagna successiva

Le modifiche apportate a metà sessione possono accumularsi rapidamente. Questi prompt consentono di esaminare cosa è pronto, raggruppare gli aggiornamenti in un lancio rivedibile e promuovere in modo pulito prima che una campagna venga pubblicata.

**Richieste**

```
Show me all pages updated in this session that are still unpublished.
```

```
Create a launch with all changes from this session for review before publishing.
```

```
Give me a summary of all changes made in this session.
```

```
Promote everything in the current launch to production.
```

+++

## Ulteriori informazioni

| Risorsa | Cosa troverai |
| --- | --- |
| [Documentazione MCP di Analytics](https://developer.adobe.com/analytics-mcp/docs/) | Configurazione di CJA MCP e riferimento dello strumento |
| [Documentazione su AEM as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service) | Documentazione completa di AEM |
| [Server MCP CJA nel Registro di sistema AI](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) | Strumenti e disponibilità del server CJA MCP |
| [Server AEM Content MCP nel Registro AI](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) | Strumenti e disponibilità di AEM Content MCP Server |
| [Server MCP](../tools/mcp-servers.md) | Collegare un client di intelligenza artificiale ai server Adobe MCP |
