---
title: Server MCP
description: Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise utilizzando i server Model Context Protocol.
last-substantial-update: 2026-09-16
source-git-commit: a70eede6e0efe0d1dbdc00c5d9de5aeb3b5d75de
workflow-type: tm+mt
source-wordcount: '2400'
ht-degree: 6%
---

# Server MCP

<!-- last-modified: 2026-09-16 -->

I server MCP di Adobe forniscono a qualsiasi client di intelligenza artificiale compatibile un accesso diretto e gestito ai dati e ai flussi di lavoro di Adobe. Connettiti una volta e puoi eseguire query sulle prestazioni della campagna, attivare tipi di pubblico, esaminare percorsi, gestire contenuti e altro ancora, il tutto in un linguaggio semplice, senza uscire dall’ambiente AI. Poiché i server MCP si trovano tra il client di intelligenza artificiale e i sistemi sottostanti di Adobe, si ottiene flessibilità in linguaggio naturale mantenendo attivi i controlli di accesso e la governance dei dati della propria organizzazione.

I server Adobe MCP seguono lo standard [Model Context Protocol](https://modelcontextprotocol.io/docs/getting-started/intro) aperto. Qualsiasi client AI compatibile con MCP si connette a qualsiasi server MCP di Adobe.

## Server CX Enterprise MCP {#cx-enterprise-mcp-servers}

>[!CONTEXTUALHELP]
>id="cx-enterprise-agentic-tools_mcp_servers_cx-enterprise"
>title="CX Enterprise Coworker"
>abstract="Chiedere, analizzare e intervenire sulle applicazioni CX Enterprise in linguaggio semplice, senza alcuna configurazione del server. Per le singole applicazioni con il proprio server MCP, è sufficiente connettersi direttamente."
>additional-url="https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home" text="Documentazione di CX Enterprise Coworker"

![CX Enterprise Coworker che connette un client di IA alle applicazioni CX Enterprise](../assets/mcp-sub-hero.gif)

**Il modo più veloce per lavorare nelle applicazioni CX Enterprise è CX Enterprise Coworker.** Si connette alle applicazioni CX Enterprise senza configurazione del server, endpoint da registrare e configurazione client di IA. [Prova CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home)

Se preferisci collegare il tuo client AI direttamente a una specifica applicazione Adobe, diverse applicazioni hanno anche il proprio server MCP.

| Server MCP | Endpoint | Che cosa puoi fare | Anche tramite CX Enterprise Coworker |
| --- | --- | --- | --- |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/ajo-mcp) | `https://ajo-mcp.adobe.io/mcp` | Rivedi percorsi, campagne e configurazioni di canale | Sì |
| [Customer Journey Analytics](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/cja-mcp) | `https://cja-mcp.adobe.io/mcp` | Eseguire query sui rapporti, individuare le visualizzazioni dati e creare aree di lavoro | Sì |
| [Adobe Analytics](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/mcp/mcp-product-tools/analytics-mcp) | `https://aa-mcp.adobe.io/mcp` | Individuazione suite di rapporti, authoring dei segmenti e creazione di aree di lavoro | Sì |
| [Adobe Target](https://experienceleague.adobe.com/it/docs/target/using/mcp/target-mcp) | `https://targetmcp.adobe.io/mcp` | Rivedi attività, offerte, tipi di pubblico, mbox, rapporti sulle prestazioni e URL di anteprima (versione beta pubblica: gli strumenti sono di sola lettura, gli strumenti di scrittura sono pianificati per la disponibilità generale) | Sì |
| [Real-Time CDP](https://experienceleague.adobe.com/it/docs/experience-platform/rtcdp/intro/rtcdp-mcp) | `https://rtcdp-mcp.adobe.io/mcp` | Cerca tipi di pubblico, destinazioni, origini e flussi in esecuzione; controlla gli spazi dei nomi delle identità e i criteri di unione (versione beta pubblica: inserisce nell&#39;elenco Consentiti richiesta, tutti gli strumenti sono di sola lettura). | Sì |
| [Server MCP AEM](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/overview) | `https://mcp.adobeaemcloud.com/adobe/mcp/aem` | Gestisci pagine, frammenti di contenuto, risorse e lanci; valuta contenuti e immagini in base alle linee guida del brand e alle regole di conformità | Sì |
| [AEM Cloud Manager](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | Gestire programmi, ambienti, pipeline e archivi | No |
| Adobe Marketing Agent | `https://aep-ai-ama.adobe.io/mcp` | Organizzazione dell’analisi del pubblico, della diagnostica AEP e della creazione di percorsi B2B AJO nelle applicazioni AEP | No |
| [Adobe Workfront](https://experienceleague.adobe.com/it/docs/workfront/using/basics/workfront-mcp-server/workfront-mcp-server-overview) | `https://mcp.prod.us-west-2.aws.wfk8s.com/mcp/v1/workfront` | Gestisci lavoro, progetti, record di pianificazione, approfondimenti e approvazioni di contenuti | No |
| [Marketo Engage](https://experienceleague.adobe.com/it/docs/marketo-developer/marketo/mcp-server) | `https://marketo-mcp.adobe.io/mcp` | Gestisci moduli, campagne intelligenti, lead, elenchi, programmi, e-mail e operazioni in blocco | Sì |
| Adobe Experience Platform | Tramite [CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home) | Individuazione dei set di dati, esplorazione degli schemi e gestione delle sandbox | N/D |
| Campaign Classic | Tramite [CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home) | Individuazione dell’istanza della campagna, esplorazione dello schema, esecuzione di query, controllo del flusso di lavoro ed esecuzione di SOAP/JS | N/D |
| Sperimentazione | Tramite [CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home) | Rapporti di esperimenti A/B, MVT e MAB, metriche, approfondimenti, opportunità e pianificazione delle dimensioni del campione | N/D |
| GenStudio for Performance Marketing | Tramite [CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home) | Accedere ai dati sulle prestazioni degli annunci e alle informazioni creative | N/D |
| Adobe Journey Optimizer B2B edition | Tramite [CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home) | Gestire percorsi B2B, programmi per account, gruppi di acquisto e personalizzazione | N/D |

>[!NOTE]
>
>L&#39;accesso a ciascun server MCP dipende dai diritti dell&#39;organizzazione per l&#39;applicazione e dalle autorizzazioni dell&#39;utente al suo interno. Le ultime cinque righe non dispongono ancora di un proprio server MCP disponibile per la connessione diretta. Usa CX Enterprise Coworker per raggiungerli oggi stesso.

## Connetti al client di intelligenza artificiale

La maggior parte dei server MCP di Adobe utilizza OAuth con Adobe Identity Management Service (IMS). Quando richiesto, seleziona l’organizzazione IMS corretta. La scelta di quella sbagliata è la fonte più comune di errori di autenticazione.

![Un agente di IA che si connette a un server Adobe MCP](../assets/hero-connect-mcp-servers.gif)

Se utilizzi CX Enterprise Coworker, queste connessioni si verificano automaticamente. Nessun elemento di seguito è applicabile a te. I passaggi seguenti consentono di connettere il client di intelligenza artificiale direttamente a un server MCP di Adobe e utilizzare come esempio l’endpoint del server MCP di AEM. Lo stesso processo si applica a qualsiasi server MCP di Adobe: scambia nell’URL dell’endpoint il server che desideri connettere.

>[!BEGINTABS]

>[!TAB CX Enterprise Coworker]

CX Enterprise Coworker include già molte di queste funzionalità MCP. Nessun server da aggiungere, nessun endpoint da registrare e nessun client di intelligenza artificiale da configurare. L’accesso a CX Enterprise Coworker è pronto per l’uso.

Documentazione completa: [documentazione CX Enterprise Coworker](https://experienceleague.adobe.com/it/docs/cx-enterprise-coworker/content/home)

>[!TAB Claude.ai]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Consigliato"> Utilizzare un connettore gestito

Vai a [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e cerca la tua applicazione Adobe. Se è elencato un connettore Claude (ad esempio, il [connettore Adobe Experience Manager](https://developer.adobe.com/ai-registry/#/connectors/adobe-experience-manager-connector)), seguire le istruzioni di installazione anziché i passaggi seguenti.

### Connetti utilizzando un connettore personalizzato

Claude.ai supporta i server MCP remoti tramite i connettori personalizzati nelle impostazioni dell’account.

1. Vai a **Impostazioni > Integrazioni**.
2. Fare clic su **Aggiungi connettore personalizzato**.
3. Immettere l&#39;endpoint del server come URL (ad esempio, `https://mcp.adobeaemcloud.com/adobe/mcp/aem` per il server MCP di AEM) e un nome visualizzato desiderato.
4. Fai clic su **Connetti** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione dei connettori personalizzati Claude.ai](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp)

>[!TAB Codice Claude]

### Utilizzo di CLI

Eseguire `claude mcp add` per registrare un server Adobe MCP. Sostituire il nome e l&#39;URL del server con i valori del server che si desidera connettere. In questo esempio viene utilizzato il server MCP di AEM:

```bash
claude mcp add --transport http adobe-aem https://mcp.adobeaemcloud.com/adobe/mcp/aem
```

### Modifica il file delle impostazioni

Aggiungi il server a `~/.claude.json` (globale) o `.mcp.json` nella directory principale del progetto (a livello di progetto). Sostituisci la chiave e l’URL con i valori per il server che desideri connettere:

```json
{
  "mcpServers": {
    "adobe-aem": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
    }
  }
}
```

I server MCP di Adobe utilizzano OAuth. Claude Code ti chiede di eseguire l’autenticazione con il tuo Adobe ID la prima volta che chiami uno strumento. Quando richiesto, seleziona l’organizzazione IMS corretta.

Configurazione completa: [documentazione MCP codice Claude](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursore]

Aggiungi un server Adobe MCP al file di configurazione Cursor `mcp.json`, quindi connettiti tramite **Impostazioni > MCP**. Sostituisci la chiave e l’URL con i valori per il server che desideri connettere. In questo esempio viene utilizzato il server MCP di AEM:

- **Globale (tutti i progetti):** `~/.cursor/mcp.json`
- **Livello progetto:** `.cursor/mcp.json` nella directory principale del progetto

```json
{
  "mcpServers": {
    "adobe-aem": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
    }
  }
}
```

Una volta aggiunti, i server MCP vengono visualizzati in **Server MCP installati** in Impostazioni cursore. Seleziona **Connetti** accanto a qualsiasi server che mostra **Necessita dell&#39;autenticazione** e accedi con il tuo Adobe ID. Seleziona l’organizzazione IMS che ha accesso all’applicazione.

![Configurazione del server MCP del cursore che mostra i server MCP di Adobe installati e mcp.json](../assets/screenshots/cursor-mcp-server-configuration.jpg)

Configurazione completa: [Documentazione MCP cursore](https://cursor.com/docs/mcp)

>[!TAB ChatGPT]

### <img src="../assets/icons/star.svg" width="24" height="24" alt="Consigliato"> Utilizzare un connettore gestito

Vai a [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=connector) e cerca la tua applicazione Adobe. Se è elencato un connettore ChatGPT, segui le relative istruzioni di configurazione invece dei passaggi seguenti.

### Connettersi utilizzando un server MCP remoto

Chiedi all’amministratore di ChatGPT di aggiungere il server MCP per la tua organizzazione. Questo consente a ogni utente di connettersi senza la configurazione seguente.

Se un amministratore non può aggiungerlo o se desideri la connessione solo per il tuo account, segui la procedura riportata di seguito.

**Configurazione unica:** attivare la modalità Sviluppatore prima di registrare un URL MCP personalizzato.

1. Vai a **Impostazioni > Protezione e accesso**.
2. Attiva **Modalità sviluppatore**.

**Aggiungi un server:**

1. Vai a **Impostazioni > Plug-in > Sfoglia plug-in**.
2. Selezionare **+** per aggiungere un nuovo plug-in.
3. Immettere un nome, ad esempio `AEM Content AI` o `Adobe Journey Optimizer`.
4. Immetti una descrizione.
5. Selezionare **URL server**.
6. In **Connessione**, immetti l&#39;URL MCP completo di Adobe. Ad esempio, `https://mcp.adobeaemcloud.com/adobe/mcp/aem` per AEM o `https://ajo-mcp.adobe.io/mcp` per Adobe Journey Optimizer.
7. Imposta **Autenticazione** su **OAuth**.
8. Leggi e accetta i termini del servizio.
9. Seleziona **Crea**.
10. Accedere con l&#39;account Adobe che ha accesso all&#39;applicazione CX Enterprise a cui il server MCP si connette.

Configurazione completa: [Documentazione MCP di ChatGPT](https://developers.openai.com/api/docs/guides/tools-connectors-mcp)

>[!TAB CLI codex OpenAI]

OpenAI Codex CLI supporta i server MCP remoti tramite la configurazione TOML.

**Percorsi file di configurazione:**

- **Livello utente (tutti i progetti):** `~/.codex/config.toml`
- **Ambito progetto:** `.codex/config.toml` nella directory principale del progetto

Sostituisci il nome della sezione e l’URL con i valori per il server che desideri connettere. In questo esempio viene utilizzato il server MCP di AEM:

```toml
[mcp_servers.adobe-aem]
url = "https://mcp.adobeaemcloud.com/adobe/mcp/aem"
enabled = true
```

I server MCP di Adobe utilizzano OAuth. Codex CLI gestisce automaticamente il flusso OAuth al primo utilizzo. Quando richiesto, seleziona l’organizzazione IMS corretta.

Configurazione completa: [Documentazione MCP CLI Codex OpenAI](https://developers.openai.com/codex/mcp)

>[!TAB Copilot Studio]

Microsoft Copilot Studio si connette ai server MCP remoti utilizzando l’Onboarding guidato MCP, che crea automaticamente un connettore personalizzato Power Platform.

1. Apri il tuo agente in Copilot Studio.
2. Vai alla pagina **Strumenti**.
3. Selezionare **Aggiungi uno strumento > Nuovo strumento > Protocollo contesto modello**.
4. Nella procedura guidata di onboarding MCP, immetti i dettagli del server. Ad esempio, per il server MCP di AEM:
   - **Nome server:** `AEM`
   - **URL server:** `https://mcp.adobeaemcloud.com/adobe/mcp/aem`
5. Imposta l&#39;autenticazione su **OAuth 2.0** e configura con l&#39;autorizzazione Adobe IMS e gli URL del token.
6. Seleziona **Crea**, quindi **Aggiungi all&#39;agente**.

>[!NOTE]
>
>Le connessioni server MCP in Copilot Studio passano attraverso Power Platform. Si applicano i criteri di prevenzione della perdita di dati (DLP) della tua organizzazione.

Configurazione completa: [Documentazione MCP di Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/mcp-add-existing-server-to-agent)

>[!ENDTABS]

## Server MCP in azione

Consulta Server Adobe MCP utilizzati per risolvere problemi di business reali. Ogni procedura dettagliata inizia da una vera e propria sfida operativa e mostra come un client di intelligenza artificiale la risolve in un linguaggio semplice, senza passare da uno strumento all’altro o scrivere codice.

<!--
CARDS

* ../use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* ../use-cases/manage-ajo-journeys.md
  {title = Catch journey issues early}
  {description = Monitor active journeys and surface operational issues before they reach your audience.}
  {cta = Monitor your journeys}

* ../use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Close content performance gaps}
  {description = Surface conversion gaps in CJA, trace them to underperforming content in AEM, and apply the fix in a single AI session.}
  {cta = Close performance gaps}
-->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/analyze-campaign-performance.md" title="Informazioni sulla campagna senza rapporti">
                        <img class="is-bordered-r-small" src="../assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Informazioni sulla campagna senza rapporti"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/analyze-campaign-performance.md" title="Informazioni sulla campagna senza rapporti">Informazioni sulla campagna senza rapporti</a>
                    </p>
                    <p class="is-size-6">Poni le domande sulle prestazioni in un linguaggio semplice e ottieni risposte da Customer Journey Analytics, senza creare un singolo rapporto.</p>
                </div>
                <a href="../use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Informazioni sulla campagna Surface</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Audience activation at a glance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/query-audiences.md" title="Panoramica dell’attivazione del pubblico">
                        <img class="is-bordered-r-small" src="../assets/use-cases/query-audiences/query-audiences-step4-02-summary.png" alt="Panoramica dell’attivazione del pubblico"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/query-audiences.md" title="Panoramica dell’attivazione del pubblico">Audience Activation at a glance</a>
                    </p>
                    <p class="is-size-6">Scopri quali tipi di pubblico sono live, dove fluiscono e se le destinazioni sono sane, senza navigare in Real-Time CDP.</p>
                </div>
                <a href="../use-cases/query-audiences.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Verifica attivazione pubblico</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Catch journey issues early">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-ajo-journeys.md" title="Recupera problemi percorso in anticipo">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-ajo-journeys/manage-ajo-journeys-step5-02-exe-summary.png" alt="Recupera problemi percorso in anticipo"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-ajo-journeys.md" title="Recupera problemi percorso in anticipo">Rileva problemi di percorso in anticipo</a>
                    </p>
                    <p class="is-size-6">Monitora i percorsi attivi e i problemi operativi superficiali prima che raggiungano il pubblico.</p>
                </div>
                <a href="../use-cases/manage-ajo-journeys.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Monitora i percorsi</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/manage-aem-content.md" title="Spedisci aggiornamenti contenuti più rapidamente">
                        <img class="is-bordered-r-small" src="../assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Spedisci aggiornamenti contenuti più rapidamente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/manage-aem-content.md" title="Spedisci aggiornamenti contenuti più rapidamente">Spedisci aggiornamenti contenuti più rapidamente</a>
                    </p>
                    <p class="is-size-6">Trova, aggiorna e pubblica più rapidamente le pagine AEM e i frammenti di contenuto, senza passare all’interfaccia di AEM.</p>
                </div>
                <a href="../use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Spedire i contenuti più velocemente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Close content performance gaps">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="../use-cases/optimize-content-with-performance-data.md" title="Colmare le lacune nelle prestazioni dei contenuti">
                        <img class="is-bordered-r-small" src="../assets/use-cases/optimize-content-with-performance-data/optimize-content-with-performance-data-step5-03-page-compare.png" alt="Colmare le lacune nelle prestazioni dei contenuti"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="../use-cases/optimize-content-with-performance-data.md" title="Colmare le lacune nelle prestazioni dei contenuti">Colmare le lacune nelle prestazioni dei contenuti</a>
                    </p>
                    <p class="is-size-6">Supera i gap di conversione in CJA, tracciali sui contenuti con prestazioni inferiori in AEM e applica la correzione in una singola sessione di intelligenza artificiale.</p>
                </div>
                <a href="../use-cases/optimize-content-with-performance-data.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Colmare le lacune nelle prestazioni</span>
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

Un server MCP di Adobe può essere autenticato solo per un’organizzazione IMS alla volta, anche se il tuo account utente ha accesso a più di un’organizzazione.

+++

+++Specifica di una sandbox, una suite di rapporti, un ambiente o un’altra risorsa sessione

Alcuni server MCP di Adobe richiedono di specificare una risorsa prima di poter restituire i risultati. A seconda dell’applicazione, può trattarsi di una sandbox, un programma, un ambiente, una suite di rapporti o una visualizzazione dati.

Se non sei sicuro delle risorse a cui hai accesso, chiedi al client di intelligenza artificiale. Ad esempio: &quot;Elencare le sandbox disponibili&quot; o &quot;A quali suite di rapporti ho accesso?&quot; Spesso i server Adobe MCP restituiscono un elenco completo delle risorse disponibili per l’utente.

Una volta impostata una risorsa sessione, puoi cambiarla in qualsiasi momento indicando al client di intelligenza artificiale quale utilizzare.

+++

+++Autorizzazioni ed errori di accesso

I clienti IA agiscono per conto del tuo account utente di Adobe utilizzando OAuth. Le stesse autorizzazioni e gli stessi controlli di accesso che si applicano quando si accede a un&#39;applicazione Adobe si applicano quando si utilizza un server MCP.

Se un&#39;azione non riesce o non restituisce alcun risultato, verificare che l&#39;utente disponga delle autorizzazioni necessarie in Adobe Admin Console e nell&#39;applicazione CX Enterprise pertinente. Se hai bisogno di regolare l’accesso, contatta l’amministratore di sistema di Adobe.

+++

+++Nuova autenticazione dopo una sessione persa

I server MCP di Adobe utilizzano OAuth per autenticare il tuo account utente Adobe. Se lo stato di autenticazione viene perso, non verranno eseguite ulteriori chiamate allo strumento finché non si esegue di nuovo l&#39;autenticazione.

Per autenticare di nuovo: apri la configurazione del server MCP del client di intelligenza artificiale, seleziona la voce del server MCP di Adobe e riconnettiti. Ti verrà chiesto di accedere nuovamente con il tuo Adobe ID.

+++
