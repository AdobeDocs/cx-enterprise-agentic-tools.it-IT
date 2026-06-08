---
title: Server MCP
description: Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise utilizzando i server Model Context Protocol.
index: false
source-git-commit: bb341fa02a8e1e8b3efbf832359846c94441df88
workflow-type: tm+mt
source-wordcount: '2364'
ht-degree: 4%

---


# Server MCP

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491330/?captions=ita&learn=on&enablevpops)

I server Adobe CX Enterprise MCP offrono a qualsiasi client di intelligenza artificiale compatibile un accesso diretto e controllato ai dati e ai flussi di lavoro di Adobe. Connettiti una volta e puoi eseguire query sulle prestazioni della campagna, attivare tipi di pubblico, esaminare percorsi, gestire contenuti e altro ancora, il tutto in un linguaggio semplice, senza uscire dall’ambiente AI. Poiché i server MCP si trovano tra il client di intelligenza artificiale e i sistemi sottostanti di Adobe, si ottiene flessibilità in linguaggio naturale mantenendo attivi i controlli di accesso e la governance dei dati della propria organizzazione.

I server Adobe MCP seguono lo standard [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) aperto. Qualsiasi client AI compatibile con MCP si connette a qualsiasi server MCP di Adobe.

## MCP aziendale CX

![CX Enterprise MCP collega il client AI agli strumenti di tutta la suite Adobe CX Enterprise](../assets/mcp-gateway-hero.gif)

**Un endpoint. Più applicazioni aziendali CX.**

Effettuare la connessione una volta e il client AI può accedere alle applicazioni CX Enterprise in base alle licenze dell&#39;organizzazione. Gli strumenti disponibili vengono determinati automaticamente dalle adesioni Adobe, ovvero non è necessaria alcuna connessione separata per ogni applicazione.

>[!BEGINTABS]

>[!TAB applicazioni aziendali CX]

Gli strumenti di ciascuna applicazione sono disponibili in base alle licenze Adobe della tua organizzazione.

| Applicazione | Che cosa puoi fare |
| --- | --- |
| Adobe Journey Optimizer | [Rivedi percorsi, campagne e configurazioni dei canali](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [Eseguire query sui report, individuare le visualizzazioni dati, creare aree di lavoro](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [Verifica destinazioni, stato attivazione e integrità flusso di dati](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) (versione beta chiusa) |

Se la tua applicazione non è elencata qui, consulta l&#39;[elenco completo dei server MCP](#adobe-cx-enterprise-mcp-servers) di seguito.

>[!TAB Connetti]

Utilizzare l&#39;endpoint MCP aziendale CX ovunque si utilizzi un endpoint MCP specifico per l&#39;applicazione.

```
https://cx-enterprise.adobe.io/mcp
```

Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata alle tue applicazioni Adobe. La scelta dell’organizzazione sbagliata è la causa più comune di strumenti mancanti o errori di autenticazione.

Per istruzioni di installazione complete, consulta [Connetti al client di intelligenza artificiale](#connect-to-your-ai-client) di seguito.

>[!ENDTABS]

## Server MCP Adobe CX Enterprise

I server elencati di seguito si connettono direttamente. Per AJO, Customer Journey Analytics e Real-Time CDP, utilizzare [CX Enterprise MCP](#cx-enterprise-mcp) sopra.

<!--
CARDS

* #cx-enterprise-mcp
  {title = CX Enterprise MCP}
  {description = One connection to AJO, CJA, and Real-Time CDP. Your AI client gets access to the applications your organization is licensed for — automatically.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View in AI Registry}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/analytics-mcp/docs/aa/" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/analytics-mcp/docs/aa/" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Strumenti per l’individuazione delle suite di rapporti, l’analisi di dimensioni e metriche, l’authoring dei segmenti e la creazione di workspace in Adobe Analytics.</p>
                </div>
                <a href="https://developer.adobe.com/analytics-mcp/docs/aa/" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza la documentazione</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" title="Contenuto AEM" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="Contenuto AEM"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" target="_blank" rel="referrer" title="Contenuto AEM">Contenuto AEM</a>
                    </p>
                    <p class="is-size-6">Strumenti per la gestione di pagine, frammenti di contenuto, risorse e avvii in Adobe Experience Manager as a Cloud Service utilizzando il linguaggio naturale.</p>
                </div>
                <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza la documentazione</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content (Read-Only)">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" title="Contenuto AEM (sola lettura)" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="Contenuto AEM (sola lettura)"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" target="_blank" rel="referrer" title="Contenuto AEM (sola lettura)">Contenuto AEM (Sola Lettura)</a>
                    </p>
                    <p class="is-size-6">Strumenti per l’individuazione e l’esecuzione di query su pagine, frammenti di contenuto e avvii in AEM as a Cloud Service. Nessun accesso in scrittura.</p>
                </div>
                <a href="https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza la documentazione</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Cloud Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager" title="AEM Cloud Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="AEM Cloud Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager" target="_blank" rel="referrer" title="AEM Cloud Manager">AEM Cloud Manager</a>
                    </p>
                    <p class="is-size-6">Strumenti per la gestione di programmi, ambienti, pipeline e archivi Cloud Manager dall’IDE utilizzando il linguaggio naturale.</p>
                </div>
                <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza la documentazione</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="CX Enterprise MCP">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="#cx-enterprise-mcp" title="MCP aziendale CX" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-cxenterprise-card.png" alt="MCP aziendale CX"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="#cx-enterprise-mcp" target="_blank" rel="referrer" title="MCP aziendale CX">MCP aziendale CX</a>
                    </p>
                    <p class="is-size-6">Una connessione ad AJO, CJA e Real-Time CDP. Il client di intelligenza artificiale ottiene automaticamente l’accesso alle applicazioni per le quali l’organizzazione dispone della licenza.</p>
                </div>
                <a href="#cx-enterprise-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Connetti</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Strumenti per l’individuazione delle suite di rapporti, l’analisi di dimensioni e metriche, l’authoring dei segmenti e la creazione di workspace in Adobe Analytics.</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza nel Registro di sistema di IA</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" title="Contenuto AEM" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="Contenuto AEM"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" target="_blank" rel="referrer" title="Contenuto AEM">Contenuto AEM</a>
                    </p>
                    <p class="is-size-6">Strumenti per la gestione di pagine, frammenti di contenuto, risorse e avvii in Adobe Experience Manager as a Cloud Service utilizzando il linguaggio naturale.</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza nel Registro di sistema di IA</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Content (Read-Only)">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" title="Contenuto AEM (sola lettura)" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="Contenuto AEM (sola lettura)"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" target="_blank" rel="referrer" title="Contenuto AEM (sola lettura)">Contenuto AEM (Sola Lettura)</a>
                    </p>
                    <p class="is-size-6">Strumenti per l’individuazione e l’esecuzione di query su pagine, frammenti di contenuto e avvii in AEM as a Cloud Service. Nessun accesso in scrittura.</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza nel Registro di sistema di IA</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="AEM Cloud Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" title="AEM Cloud Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/mcp-aem-card.png" alt="AEM Cloud Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" target="_blank" rel="referrer" title="AEM Cloud Manager">AEM Cloud Manager</a>
                    </p>
                    <p class="is-size-6">Strumenti per la gestione di programmi, ambienti, pipeline e archivi Cloud Manager dall’IDE utilizzando il linguaggio naturale.</p>
                </div>
                <a href="https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza nel Registro di sistema di IA</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

### Endpoint del server MCP

Tutti gli endpoint sono elencati nel [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector). Questa tabella è un riferimento rapido se sai già cosa ti serve: acquisisci l’URL dell’endpoint e analizza gli strumenti disponibili prima di connetterti.

| Server | Endpoint | Strumenti |
| --- | --- | --- |
| [MCP aziendale CX](#cx-enterprise-mcp) | `https://cx-enterprise.adobe.io/mcp` | · [Strumenti di Adobe Journey Optimizer](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Strumenti di Customer Journey Analytics](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Strumenti di Real-Time CDP](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [Contenuto AEM](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [Contenuto AEM (Sola Lettura)](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

## Connetti al client di intelligenza artificiale

Tutti i server MCP di Adobe utilizzano OAuth con Adobe Identity Management Service (IMS). Quando richiesto, seleziona l’organizzazione IMS corretta. La scelta di quella sbagliata è la fonte più comune di errori di autenticazione.

Prima di configurare manualmente, controlla il [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) per trovare un connettore gestito per il client di intelligenza artificiale e l&#39;applicazione Adobe. I connettori gestiti gestiscono automaticamente l’autenticazione. Se è disponibile un connettore per il client e l’applicazione, utilizzalo al posto dei passaggi manuali indicati di seguito.

![Un agente di IA che si connette a un server Adobe MCP](../assets/hero-connect-mcp-servers.gif)

>[!BEGINTABS]

>[!TAB Claude.ai]

### ![Consigliato](../assets/badge-recommended.svg) Utilizza un connettore gestito

Vai a [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e cerca la tua applicazione Adobe. Se è elencato un connettore Claude (ad esempio, il [connettore Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), seguire le istruzioni di installazione anziché i passaggi seguenti.

### Connetti utilizzando un connettore personalizzato

Claude.ai supporta i server MCP remoti tramite i connettori personalizzati nelle impostazioni dell’account.

1. Vai a **Impostazioni > Integrazioni**.
2. Fare clic su **Aggiungi connettore personalizzato**.
3. Immettere `https://cx-enterprise.adobe.io/mcp` come URL e un nome visualizzato come `Adobe CX Enterprise`.
4. Fai clic su **Connetti** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione dei connettori personalizzati Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Codice Claude]

### Utilizzo di CLI

Eseguire `claude mcp add` per registrare CX Enterprise MCP. Una connessione consente di accedere ad AJO, CJA e Real-Time CDP in base alle licenze della tua organizzazione.

```bash
claude mcp add --transport http adobe-cx-enterprise https://cx-enterprise.adobe.io/mcp
```

### Modifica il file delle impostazioni

Aggiungi il server a `~/.claude.json` (globale) o `.mcp.json` nella directory principale del progetto (a livello di progetto):

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

Aggiungere CX Enterprise MCP al file di configurazione del cursore `mcp.json`, quindi connettersi tramite **Impostazioni > MCP**.

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

Una connessione consente di accedere ad AJO, CJA e Real-Time CDP in base alle licenze della tua organizzazione.

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
4. Immetti `https://cx-enterprise.adobe.io/mcp` come URL e `Adobe CX Enterprise` come nome.
5. Imposta autenticazione su **OAuth**.
6. Fai clic su **Connetti** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI codex OpenAI]

OpenAI Codex CLI supporta i server MCP remoti tramite la configurazione TOML.

**Percorsi file di configurazione:**

- **Livello utente (tutti i progetti):** `~/.codex/config.toml`
- **Ambito progetto:** `.codex/config.toml` nella directory principale del progetto

Aggiungere CX Enterprise MCP:

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
4. Nella procedura guidata di onboarding MCP, immetti:
   - **Nome server:** `Adobe CX Enterprise`
   - **URL server:** `https://cx-enterprise.adobe.io/mcp`
5. Imposta l&#39;autenticazione su **OAuth 2.0** e configura con l&#39;autorizzazione Adobe IMS e gli URL del token.
6. Seleziona **Crea**, quindi **Aggiungi all&#39;agente**.

>[!NOTE]
>
>Le connessioni server MCP in Copilot Studio passano attraverso Power Platform. Si applicano i criteri di prevenzione della perdita di dati (DLP) della tua organizzazione.

Configurazione completa: [Documentazione MCP di Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Risoluzione dei problemi

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

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use CX Enterprise MCP for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Analizzare le prestazioni della campagna" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="Analizzare le prestazioni della campagna"
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
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="Eseguire query sui tipi di pubblico"
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
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="Rivedi percorsi AJO"
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
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="Gestire i contenuti AEM con IA"
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
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="Ottimizzazione dei contenuti in base ai dati sulle prestazioni"
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
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/cross-channel-campaign-review.md" title="Eseguire una revisione di una campagna cross-channel" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Eseguire una revisione di una campagna cross-channel"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Eseguire una revisione di una campagna cross-channel">Eseguire una revisione della campagna cross-channel</a>
                    </p>
                    <p class="is-size-6">Utilizza CX Enterprise MCP per una visualizzazione unificata dello stato delle campagne AJO, CJA e Real-Time CDP in una sola sessione AI.</p>
                </div>
                <a href="../use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

