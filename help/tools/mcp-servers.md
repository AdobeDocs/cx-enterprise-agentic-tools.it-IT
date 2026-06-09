---
title: Server MCP
description: Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise utilizzando i server Model Context Protocol.
index: false
last-substantial-update: 2026-06-09T00:00:00Z
source-git-commit: 9c62818daecf3c20230457da5b9b8086d954260f
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 3%

---


# Server MCP

<!-- last-modified: 2026-06-09 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

I server Adobe CX Enterprise MCP offrono a qualsiasi client di intelligenza artificiale compatibile un accesso diretto e controllato ai dati e ai flussi di lavoro di Adobe. Connettiti una volta e puoi eseguire query sulle prestazioni della campagna, attivare tipi di pubblico, esaminare percorsi, gestire contenuti e altro ancora, il tutto in un linguaggio semplice, senza uscire dall’ambiente AI. Poiché i server MCP si trovano tra il client di intelligenza artificiale e i sistemi sottostanti di Adobe, si ottiene flessibilità in linguaggio naturale mantenendo attivi i controlli di accesso e la governance dei dati della propria organizzazione.

I server Adobe MCP seguono lo standard [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) aperto. Qualsiasi client AI compatibile con MCP si connette a qualsiasi server MCP di Adobe.

## Server MCP aziendali CX

![CX Enterprise MCP collega il client AI agli strumenti di tutta la suite Adobe CX Enterprise](../assets/mcp-gateway-hero.gif)

Seleziona un’applicazione per visualizzare l’endpoint e le funzionalità.

>[!BEGINTABS]

>[!TAB MCP aziendale CX]

**Un endpoint. Più applicazioni aziendali CX.**

Effettuare la connessione una volta e il client AI può accedere alle applicazioni CX Enterprise in base alle licenze dell&#39;organizzazione. Per abilitare la tua organizzazione, invia un&#39;e-mail a [cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com) per richiedere l&#39;accesso.

```
https://cx-enterprise.adobe.io/mcp
```

| Applicazione CX Enterprise | Che cosa puoi fare |
| --- | --- |
| Adobe Analytics | Individuazione suite di rapporti, authoring dei segmenti e creazione di aree di lavoro |
| Adobe Experience Platform | Individuazione dei set di dati, esplorazione degli schemi e gestione delle sandbox |
| Adobe Journey Optimizer | Rivedi percorsi, campagne e configurazioni di canale |
| Adobe Journey Optimizer B2B edition | Gestire percorsi B2B, programmi per account, gruppi di acquisto e personalizzazione |
| Customer Journey Analytics | Eseguire query sui rapporti, individuare le visualizzazioni dati e creare aree di lavoro |
| Real-Time CDP | Verificare lo stato di attivazione del pubblico, lo stato della destinazione e lo stato del flusso di dati |

>[!NOTE]
>
>L&#39;accesso a ogni applicazione CX Enterprise si basa sui diritti dell&#39;organizzazione e sulle autorizzazioni dell&#39;utente in Adobe Admin Console. Per abilitare CX Enterprise MCP per la tua organizzazione, invia un&#39;e-mail a [cxo-mcp-feedback@adobe.com](mailto:cxo-mcp-feedback@adobe.com).

>[!TAB Experience Manager]

Adobe Experience Manager dispone di più server MCP per flussi di lavoro diversi.

| Server MCP | Endpoint | Che cosa puoi fare |
| --- | --- | --- |
| [AEM (Modalità Codice)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Accesso diretto REST API ad AEM tramite ricerca in linguaggio naturale, lettura, scrittura ed eliminazione |
| [AEM Cloud Manager](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Gestire programmi, ambienti, pipeline e archivi |
| [Contenuto AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | Gestire pagine, frammenti di contenuto, risorse e avvii |
| [Contenuto AEM (Sola Lettura)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | Individuazione ed esecuzione di query su pagine, frammenti di contenuto e avvii senza accesso in scrittura |
| [Authoring di documenti AEM]&#x200B;(TODO: validate) | `https://mcp.adobeaemcloud.com/adobe/mcp/da` | Gestire file, cronologia delle versioni e riferimenti multimediali in Creazione di documenti |
| [Governance delle esperienze AEM](https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/experience-governance-mcp-server) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-governance` | Valutazione di contenuti e immagini in base alle linee guida del brand e alle regole di conformità |
| [Produzione AEM Experience](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/experience-production/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/experience-production` | Trasforma e crea pagine AEM su larga scala utilizzando le descrizioni dei contenuti basate sull’intelligenza artificiale |

>[!NOTE]
>
>L’accesso a ogni ambiente AEM dipende dalle autorizzazioni AEM Cloud Service della tua organizzazione e dalle autorizzazioni dell’utente in tale ambiente.

>[!TAB Experience Platform]

| Server MCP | Endpoint | Che cosa puoi fare |
| --- | --- | --- |
| [Adobe Marketing Agent] (TODO: validate) | `https://aep-ai-ama.adobe.io/mcp` | Organizzazione dell’analisi del pubblico, della diagnostica AEP e della creazione di percorsi B2B AJO nelle applicazioni AEP |

>[!NOTE]
>
>L’accesso dipende dai diritti Adobe Experience Platform della tua organizzazione e dalle autorizzazioni dell’utente.

>[!TAB Marketo Engage]

| Server MCP | Endpoint | Che cosa puoi fare |
| --- | --- | --- |
| [Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Gestisci programmi, campagne, lead, elenchi avanzati, e-mail e moduli |

>[!NOTE]
>
>Marketo Engage MCP utilizza credenziali del servizio native per Marketo, non Adobe IMS. Consulta la [documentazione del server Marketo Engage MCP](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/mcp-server) per la configurazione dell&#39;autenticazione. L’accesso dipende dalla sottoscrizione a Marketo Engage e dalle autorizzazioni dell’utente API.

>[!TAB Target]

Adobe Target MCP è in versione beta pubblica. Tutti gli strumenti attualmente disponibili sono di sola lettura. Gli strumenti di scrittura sono pianificati per la disponibilità generale.

| Server MCP | Endpoint | Che cosa puoi fare |
| --- | --- | --- |
| [Adobe Target](https://experienceleague.adobe.com/it/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Rivedi attività, offerte, tipi di pubblico, mbox e rapporti sulle prestazioni |

>[!NOTE]
>
>L’accesso dipende dai diritti di Adobe Target e dalle autorizzazioni dell’utente.

>[!TAB Workfront]

| Server MCP | Endpoint | Che cosa puoi fare |
| --- | --- | --- |
| [Adobe Workfront] (TODO: validate) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Gestisci lavoro, progetti, record di pianificazione, approfondimenti e approvazioni di contenuti |

>[!NOTE]
>
>L&#39;accesso dipende dalle licenze Adobe Workfront e dalle autorizzazioni dell&#39;utente.

>[!ENDTABS]

## Connetti al client di intelligenza artificiale

Tutti i server MCP di Adobe utilizzano OAuth con Adobe Identity Management Service (IMS). Quando richiesto, seleziona l’organizzazione IMS corretta. La scelta di quella sbagliata è la fonte più comune di errori di autenticazione.

Prima di configurare manualmente, controlla il [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) per trovare un connettore gestito per il client di intelligenza artificiale e l&#39;applicazione Adobe. I connettori gestiti gestiscono automaticamente l’autenticazione. Se è disponibile un connettore per il client e l’applicazione, utilizzalo al posto dei passaggi manuali indicati di seguito.

I passaggi seguenti utilizzano l&#39;endpoint MCP di CX Enterprise come esempio. Lo stesso processo si applica a qualsiasi server MCP di Adobe: scambiare nell’URL dell’endpoint il server che si desidera connettere.

![Un agente di IA che si connette a un server Adobe MCP](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### ![Consigliato](../assets/badge-recommended.svg) Utilizza un connettore gestito

Vai a [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e cerca la tua applicazione Adobe. Se è elencato un connettore Claude (ad esempio, il [connettore Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), seguire le istruzioni di installazione anziché i passaggi seguenti.

### Connetti utilizzando un connettore personalizzato

Claude.ai supporta i server MCP remoti tramite i connettori personalizzati nelle impostazioni dell’account.

1. Vai a **Impostazioni > Integrazioni**.
2. Fare clic su **Aggiungi connettore personalizzato**.
3. Immettere l&#39;endpoint del server come URL, ad esempio `https://cx-enterprise.adobe.io/mcp` per l&#39;MCP aziendale CX, e un nome visualizzato desiderato.
4. Fai clic su **Connetti** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione dei connettori personalizzati Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Codice Claude]

### Utilizzo di CLI

Eseguire `claude mcp add` per registrare un server Adobe MCP. Sostituire il nome e l&#39;URL del server con i valori del server che si desidera connettere. In questo esempio viene utilizzato CX Enterprise MCP:

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Modifica il file delle impostazioni

Aggiungi il server a `~/.claude.json` (globale) o `.mcp.json` nella directory principale del progetto (a livello di progetto). Sostituisci la chiave e l’URL con i valori per il server che desideri connettere:

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

I server MCP di Adobe utilizzano OAuth. Claude Code ti chiede di eseguire l’autenticazione con il tuo Adobe ID la prima volta che chiami uno strumento. Quando richiesto, seleziona l’organizzazione IMS corretta.

Configurazione completa: [documentazione MCP codice Claude](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursore]

Aggiungi un server Adobe MCP al file di configurazione Cursor `mcp.json`, quindi connettiti tramite **Impostazioni > MCP**. Sostituisci la chiave e l’URL con i valori per il server che desideri connettere. In questo esempio viene utilizzato CX Enterprise MCP:

- **Globale (tutti i progetti):** `~/.cursor/mcp.json`
- **Livello progetto:** `.cursor/mcp.json` nella directory principale del progetto

```json
{
  "mcpServers": {
    "adobe-cx-enterprise": {
      "type": "http",
      "url": "https://cx-enterprise.adobe.io/mcp"
    }
  }
}
```

Una volta aggiunti, i server MCP vengono visualizzati in **Server MCP installati** in Impostazioni cursore. Seleziona **Connetti** accanto a qualsiasi server che mostra **Necessita dell&#39;autenticazione** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS che ha accesso all’applicazione.

![Configurazione del server MCP del cursore che mostra i server MCP di Adobe installati e mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configurazione completa: [Documentazione MCP cursore](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### ![Consigliato](../assets/badge-recommended.svg) Utilizza un connettore gestito

Vai a [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e cerca la tua applicazione Adobe. Se è elencato un connettore ChatGPT, segui le relative istruzioni di configurazione invece dei passaggi seguenti.

### Connettersi utilizzando un server MCP remoto

ChatGPT supporta server MCP remoti tramite [Modalità sviluppatore](https://developers.openai.com/api/docs/guides/developer-mode), disponibile nei piani Pro, Plus, Business, Enterprise e Education.

1. Abilitare la modalità sviluppatore in **Impostazioni ChatGPT**.
2. Vai a **Impostazioni > Integrazioni**.
3. Fare clic su **Aggiungi connettore personalizzato** e scegliere **Server MCP remoto**.
4. Immettere l&#39;endpoint del server come URL, ad esempio `https://cx-enterprise.adobe.io/mcp` per l&#39;MCP aziendale CX, e un nome visualizzato desiderato.
5. Imposta autenticazione su **OAuth**.
6. Fai clic su **Connetti** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI codex OpenAI]

OpenAI Codex CLI supporta i server MCP remoti tramite la configurazione TOML.

**Percorsi file di configurazione:**

- **Livello utente (tutti i progetti):** `~/.codex/config.toml`
- **Ambito progetto:** `.codex/config.toml` nella directory principale del progetto

Sostituisci il nome della sezione e l’URL con i valori per il server che desideri connettere. In questo esempio viene utilizzato CX Enterprise MCP:

```toml
[mcp_servers.adobe-cx-enterprise]
url = "https://cx-enterprise.adobe.io/mcp"
enabled = true
```

I server MCP di Adobe utilizzano OAuth. Codex CLI gestisce automaticamente il flusso OAuth al primo utilizzo. Quando richiesto, seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione MCP CLI Codex OpenAI](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio si connette ai server MCP remoti utilizzando l’Onboarding guidato MCP, che crea automaticamente un connettore personalizzato Power Platform.

1. Apri il tuo agente in Copilot Studio.
2. Vai alla pagina **Strumenti**.
3. Selezionare **Aggiungi uno strumento > Nuovo strumento > Protocollo contesto modello**.
4. Nella procedura guidata di onboarding MCP, immettere i dettagli del server, ad esempio, per MCP aziendale CX:
   - **Nome server:** `Adobe CX Enterprise`
   - **URL server:** `https://cx-enterprise.adobe.io/mcp`
5. Imposta l&#39;autenticazione su **OAuth 2.0** e configura con l&#39;autorizzazione Adobe IMS e gli URL del token.
6. Seleziona **Crea**, quindi **Aggiungi all&#39;agente**.

>[!NOTE]
>
>Le connessioni server MCP in Copilot Studio passano attraverso Power Platform. Si applicano i criteri di prevenzione della perdita di dati (DLP) della tua organizzazione.

Configurazione completa: [Documentazione MCP di Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Strumenti agenti in azione

Consulta Server MCP Adobe CX Enterprise applicati a flussi di lavoro aziendali reali.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use CX Enterprise MCP to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use CX Enterprise MCP to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use CX Enterprise MCP to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CX Enterprise MCP and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analizzare le prestazioni della campagna" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Analizzare le prestazioni della campagna"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analizzare le prestazioni della campagna">Analizzare le prestazioni della campagna</a>
                    </p>
                    <p class="is-size-6">Utilizza CX Enterprise MCP per ottenere metriche e informazioni di Customer Journey Analytics da qualsiasi client AI.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Eseguire query sui tipi di pubblico" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Eseguire query sui tipi di pubblico"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" title="Eseguire query sui tipi di pubblico">Interroga tipi di pubblico</a>
                    </p>
                    <p class="is-size-6">Utilizza CX Enterprise MCP per eseguire query sui dati di destinazione e di pubblico di Real-Time CDP utilizzando prompt in linguaggio semplice.</p>
                </div>
                <a href="../use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Rivedi percorsi AJO" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Rivedi percorsi AJO"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Rivedi percorsi AJO">Rivedi percorsi AJO</a>
                    </p>
                    <p class="is-size-6">Utilizza CX Enterprise MCP per accedere ai percorsi AJO, allo stato della campagna e alle condizioni di percorso dal client AI.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Gestire i contenuti AEM con IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Gestire i contenuti AEM con IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Gestire i contenuti AEM con IA">Gestire i contenuti AEM con IA</a>
                    </p>
                    <p class="is-size-6">Scopri, aggiorna e pubblica pagine e frammenti di contenuto in AEM utilizzando il linguaggio naturale.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Ottimizzazione dei contenuti in base ai dati sulle prestazioni"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni">Ottimizza il contenuto in base ai dati sulle prestazioni</a>
                    </p>
                    <p class="is-size-6">Combinando CX Enterprise MCP e AEM Content MCP Server è possibile trovare i contenuti con prestazioni insoddisfacenti e aggiornarli in un'unica sessione.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Hai bisogno di ulteriore aiuto?

Le connessioni MCP richiedono l’autenticazione, la selezione dell’organizzazione e le autorizzazioni a livello di applicazione. Se qualcosa non funziona come previsto, questi passaggi descrivono le cause più comuni.

+++Passaggio da un’organizzazione Adobe a un’altra

Se il tuo utente Adobe appartiene a più organizzazioni IMS e vedi strumenti o dati per quello sbagliato, disconnetti il server MCP, esci dalla sessione Adobe nel browser, quindi riconnettiti. Verrà richiesto di scegliere un&#39;organizzazione durante l&#39;accesso.

Un server Adobe CX Enterprise MCP può essere autenticato solo per un’organizzazione IMS alla volta, anche se l’account utente dispone dell’accesso a più di un’organizzazione.

+++

+++Specifica di una sandbox, una suite di rapporti, un ambiente o un’altra risorsa sessione

Alcuni server Adobe CX Enterprise MCP richiedono di specificare una risorsa prima di poter restituire i risultati. A seconda dell’applicazione, può trattarsi di una sandbox, un programma, un ambiente, una suite di rapporti o una visualizzazione dati.

Se non sei sicuro delle risorse a cui hai accesso, chiedi al client di intelligenza artificiale. Ad esempio: &quot;Elencare le sandbox disponibili&quot; o &quot;A quali suite di rapporti ho accesso?&quot; I server MCP aziendali di Adobe CX spesso possono restituire un elenco completo delle risorse disponibili per l&#39;utente.

Una volta impostata una risorsa sessione, puoi cambiarla in qualsiasi momento indicando al client di intelligenza artificiale quale utilizzare.

+++

+++Autorizzazioni ed errori di accesso

I clienti IA agiscono per conto del tuo account utente di Adobe utilizzando OAuth. Le stesse autorizzazioni e gli stessi controlli di accesso che si applicano quando si accede a un&#39;applicazione Adobe si applicano quando si utilizza un server MCP.

Se un&#39;azione non riesce o non restituisce alcun risultato, verificare che l&#39;utente disponga delle autorizzazioni necessarie in Adobe Admin Console e nell&#39;applicazione CX Enterprise pertinente. Se hai bisogno di regolare l’accesso, contatta l’amministratore di sistema di Adobe.

+++

+++Nuova autenticazione dopo una sessione persa

I server Adobe CX Enterprise MCP utilizzano OAuth per autenticare l&#39;account utente Adobe. Se lo stato di autenticazione viene perso, non verranno eseguite ulteriori chiamate allo strumento finché non si esegue di nuovo l&#39;autenticazione.

Per autenticare di nuovo: apri la configurazione del server MCP del client di intelligenza artificiale, seleziona la voce del server MCP aziendale di Adobe CX e riconnettiti. Ti verrà chiesto di accedere nuovamente con il tuo Adobe ID.

+++
