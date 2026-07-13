---
title: Colmare le lacune nelle prestazioni dei contenuti con aggiornamenti basati sui dati
description: Utilizza CJA e AEM insieme in una sessione di intelligenza artificiale per trovare campagne con gap di conversione, diagnosticare la causa e aggiornare il contenuto senza cambiare strumenti.
last-substantial-update: 2026-06-10T00:00:00Z
source-git-commit: 937a3189965f3a3551c730bb27ee0592ae6fca92
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 2%

---


# Colmare le lacune nelle prestazioni dei contenuti con aggiornamenti basati sui dati
<!-- last-modified: 2026-06-10 -->

![Client AI che confronta il contenuto originale della pagina con quello aggiornato](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png){zoomable="yes"}

*Selezionare per ingrandire.*

I gap nelle prestazioni dei contenuti costano i risultati delle campagne e, in genere, chiuderli significa passare dallo strumento di analisi al CMS. In questa procedura dettagliata viene illustrato come eseguire questa operazione in una singola sessione di intelligenza artificiale: emergere campagne con interruzioni di conversione in Customer Journey Analytics, diagnosticare la causa, esaminare i contenuti insoddisfacenti in AEM e applicare gli aggiornamenti senza uscire dalla conversazione.

| Dettagli scenario | |
| --- | --- |
| Applicazioni aziendali CX | [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview), [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/overview/introduction) |
| Strumenti agenti | [CX Enterprise MCP](../tools/mcp-servers.md#cx-enterprise-mcp-servers), [AEM Content MCP Server](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) |
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
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
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
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| Server AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB Altri client di IA]

Usare Gemini, Microsoft Copilot, Cursore, Claude Code o un altro ambiente compatibile con MCP? Connettersi a entrambi i server MCP utilizzando i seguenti endpoint:

| Server | Endpoint |
| --- | --- |
| CX Enterprise MCP | `https://cx-enterprise.adobe.io/mcp` |
| Server AEM Content MCP | `https://mcp.adobeaemcloud.com/adobe/mcp/content` |

Istruzioni di installazione complete per tutti i client supportati: [Connetti al client di intelligenza artificiale](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata ai tuoi ambienti CJA e AEM. La scelta dell’organizzazione sbagliata è la fonte più comune di errori di autenticazione.
>
>Alla prima connessione, il client di intelligenza artificiale può richiedere di selezionare un’organizzazione IMS o specificare una sandbox. Una volta impostato tale contesto, il server MCP lo utilizza per il resto della sessione.
>
>Alcuni strumenti richiedono la tua approvazione prima di essere eseguiti. Rivedi la richiesta e approva o rifiuta. Non viene intrapresa alcuna azione senza la tua conferma.


## Passaggio 1: Trovare campagne con un gap di conversione

Utilizza CJA per far emergere le campagne in cui il click-through è forte ma il tasso di conversione è basso. Questo modello (intento elevato, completamento basso) in genere indica un problema di contenuto o esperienza sulla pagina di destinazione.

```
Which campaigns have strong click-through but low conversion in the last 30 days?
```

+++Vedi una risposta di esempio

![Campagne di visualizzazione client di IA con elevato click-through ma bassa conversione da CJA](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step1-campaigns.png){zoomable="yes"}

*Selezionare per ingrandire.*

+++



## Passaggio 2: diagnosticare la causa principale

Segui questo esempio per capire cosa sta causando il gap. Chiedi se il calo è concentrato su un tipo di dispositivo, un segmento di pubblico o un’interazione di contenuto specifici.

```
What's causing the conversion drop-off, is it device, segment, or content?
```

+++Vedi una risposta di esempio

![Client AI che diagnostica il calo di conversione per dispositivo, segmento e fattori di contenuto](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step2-diagnosis.png){zoomable="yes"}

*Selezionare per ingrandire.*

+++



## Passaggio 3: rivedere il contenuto in AEM

Una volta identificata la campagna insoddisfacente, richiama la pagina di destinazione da AEM nella stessa sessione. La visualizzazione di ciò che viene riportato nella pagina è il punto di partenza per capire cosa cambiare.

```
Show me the Bali Surf Camp page.
```

+++Vedi una risposta di esempio

![Client AI che mostra il contenuto corrente della pagina di destinazione da AEM](../assets/use-cases/optimize-content-with-performance-data/optimize-content-step3-page-content.png){zoomable="yes"}

*Selezionare per ingrandire.*

+++



## Passaggio 4: ottenere consigli mirati

Chiedi al tuo client di intelligenza artificiale di collegare i dati mostrati con quelli presenti sulla pagina. I motivi di IA in entrambe le origini per identificare quali sezioni di contenuto sono probabilmente responsabili del drop-off e cosa modificare.

```
Which content sections are underperforming, and what changes would you recommend?
```

+++Vedi una risposta di esempio

![Il client di IA identifica le sezioni di contenuto insoddisfacenti e consiglia modifiche specifiche](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step4.gif){zoomable="yes"}

*Selezionare per ingrandire.*

+++



## Passaggio 5: applicare e rivedere le modifiche

Chiedi al tuo client di intelligenza artificiale di creare una versione ottimizzata della pagina in base ai consigli e di riepilogare cosa è cambiato e perché.

```
Create an optimized version of the Bali Surf Camp page and summarize the proposed changes.
```

+++Vedi una risposta di esempio

![Client AI che crea una versione ottimizzata della pagina e riepiloga le modifiche](../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5.gif){zoomable="yes"}

*Selezionare per ingrandire.*

+++


>[!CAUTION]
>
>Rivedi il riepilogo completo delle modifiche proposte prima di confermare. Il server AEM Content MCP scriverà le modifiche nell’ambiente AEM. Le pagine rimangono nel loro stato di pubblicazione fino a quando non vengono esplicitamente ripubblicate.


## Risultati ottenuti

Hai connesso Customer Journey Analytics e AEM in una singola sessione di intelligenza artificiale e ti sei spostato dai dati della campagna alle modifiche al contenuto implementato senza passare da uno strumento all’altro. Hai identificato le campagne con divari di conversione, diagnosticato la causa principale, ispezionato la pagina di destinazione, ricevuto raccomandazioni mirate basate su dati e contenuto e applicato le modifiche nella stessa conversazione. In questo modo si riduce il ciclo di feedback tra Analytics insight e i contenuti pubblicati e si passa a un numero qualsiasi di pagine con prestazioni insoddisfacenti nella stessa sessione.


## Più risultati da ottenere

Con CJA e AEM connessi nella stessa sessione, puoi coprire l’intero ciclo dall’identificazione dei problemi alle correzioni delle spedizioni. Espandi uno scenario qui sotto per visualizzare i prompt che puoi provare.

+++Trovare il contenuto che blocca le prestazioni

Un traffico elevato con un coinvolgimento ridotto segnala un problema di contenuti, non di traffico. Questi prompt consentono di creare pagine e modelli specifici che richiedono attenzione prima che il problema venga risolto dalla scadenza di una campagna.

**Richieste**

```
Which campaigns have the highest traffic but lowest conversion rate this quarter?
```

```
Which pages have a high bounce rate but also high traffic?
```

```
Compare engagement rates for landing pages across email and paid social campaigns.
```

```
Find AEM pages linked from active campaigns that haven't been updated in over 60 days.
```

+++

+++Correggi gli elementi che i dati ti dicono di correggere

Una volta individuate le prestazioni insoddisfacenti, apportare modifiche mirate in base a ciò che i dati delle prestazioni hanno rivelato. Questi prompt consentono di aggiornare sezioni specifiche in base alla diagnosi.

**Richieste**

```
Update the CTA on the [page name] page to better match the campaign audience.
```

```
Rewrite the hero headline on the [page name] page to address the mobile drop-off.
```

```
Add a trust signal to the [page name] page above the conversion form.
```

```
Which pages updated in this session still need to be published?
```

+++

+++Miglioramenti della spedizione prima della campagna successiva

Le modifiche apportate a metà sessione possono accumularsi rapidamente. Queste richieste ti aiutano a rivedere ciò che è pronto, a raggruppare gli aggiornamenti per la revisione e a promuovere in modo pulito prima che una campagna venga pubblicata.

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
Publish all confirmed changes and share the updated URLs.
```

+++



## Ulteriori informazioni

| Risorsa | Cosa troverai |
| --- | --- |
| [Server MCP CJA nel Registro di sistema AI](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp){target="_blank"} | Strumenti e disponibilità del server CJA MCP |
| [Server AEM Content MCP nel Registro AI](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp){target="_blank"} | Strumenti e disponibilità di AEM Content MCP Server |
