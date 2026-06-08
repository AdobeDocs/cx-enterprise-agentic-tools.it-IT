---
title: Server MCP
description: Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise utilizzando i server Model Context Protocol.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '1601'
ht-degree: 2%

---


# Server MCP

<!-- last-modified: 2026-05-19 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491320/?learn=on&enablevpops)

I server Adobe CX Enterprise MCP offrono a qualsiasi client di intelligenza artificiale compatibile un accesso diretto e controllato ai dati e ai flussi di lavoro di Adobe. Connettiti una volta e puoi eseguire query sulle prestazioni della campagna, attivare tipi di pubblico, esaminare percorsi, gestire contenuti e altro ancora, il tutto in un linguaggio semplice, senza uscire dall’ambiente AI. Poiché i server MCP si trovano tra il client di intelligenza artificiale e i sistemi sottostanti di Adobe, si ottiene flessibilità in linguaggio naturale mantenendo attivi i controlli di accesso e la governance dei dati della propria organizzazione.

I server MCP di Adobe seguono lo standard open Model Context Protocol. Qualsiasi client AI compatibile con MCP si connette a qualsiasi server MCP di Adobe.

## Gateway MCP aziendale CX

![Il gateway MCP di CX Enterprise collega il client AI agli strumenti MCP in tutta la suite Adobe CX Enterprise](../assets/mcp-gateway-hero.gif)

**Un endpoint. Tutti i server MCP di Adobe CX Enterprise.**

Il gateway aziendale CX indirizza il client AI a strumenti di Analytics, Campagne, Contenuti e Dati, senza una connessione separata per ciascuna applicazione. Connettiti una volta e il gateway fa emergere solo gli strumenti per i quali l’organizzazione ha la licenza, in base ai diritti Adobe.

>[!BEGINTABS]

>[!TAB applicazioni aziendali CX]

Gli strumenti di ciascuna applicazione sono disponibili in base alle licenze Adobe della tua organizzazione.

| Applicazione | Che cosa puoi fare |
| --- | --- |
| Adobe Journey Optimizer | [Rivedi percorsi, campagne e configurazioni dei canali](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server) |
| Customer Journey Analytics | [Eseguire query sui report, individuare le visualizzazioni dati, creare aree di lavoro](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp) |
| Real-Time CDP | [Verifica destinazioni, stato attivazione e integrità flusso di dati](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) (versione beta chiusa) |

>[!TAB Connetti]

Utilizzare l&#39;endpoint di gateway aziendale CX ovunque si utilizzi un endpoint MCP specifico per l&#39;applicazione.

```
https://cx-enterprise.adobe.io/mcp
```

>[!NOTE]
>Per AEM, utilizzare l&#39;endpoint AEM diretto: AEM non viene instradato attraverso il gateway MCP aziendale CX.

Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata alle tue applicazioni Adobe. La scelta dell’organizzazione sbagliata è la causa più comune di strumenti mancanti o errori di autenticazione.

Per istruzioni di installazione complete, consulta [Connetti al client di intelligenza artificiale](#connect-to-your-ai-client) di seguito.

>[!ENDTABS]

## Server MCP Adobe CX Enterprise

I server elencati di seguito si connettono direttamente e non vengono instradati attraverso il gateway MCP aziendale CX. Per l&#39;accesso ad AJO, Customer Journey Analytics e Real-Time CDP, utilizzare il [gateway MCP aziendale CX](#cx-enterprise-mcp-gateway) sopra.

<!--
CARDS

* #cx-enterprise-mcp-gateway
  {title = CX Enterprise MCP Gateway}
  {description = One connection to AJO, CJA, and Real-Time CDP tools. The gateway surfaces only the tools your organization is licensed for.}
  {cta = Connect}
  {image = ../assets/mcp-cxenterprise-card.png}

* https://developer.adobe.com/analytics-mcp/docs/aa/
  {title = Adobe Analytics}
  {description = Tools for report suite discovery, dimension and metric analysis, segment authoring, and workspace creation in Adobe Analytics.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content}
  {description = Tools for managing pages, content fragments, assets, and launches in Adobe Experience Manager as a Cloud Service using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service
  {title = AEM Content (Read-Only)}
  {description = Tools for discovering and querying pages, content fragments, and launches in AEM as a Cloud Service. No write access.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager
  {title = AEM Cloud Manager}
  {description = Tools for managing Cloud Manager programs, environments, pipelines, and repositories from your IDE using natural language.}
  {cta = View documentation}
  {target = _blank}
  {image = ../assets/mcp-aem-card.png}

-->

### Endpoint del server MCP

| Server | Endpoint | Strumenti |
| --- | --- | --- |
| [Gateway MCP aziendale CX](#cx-enterprise-mcp-gateway) | `https://cx-enterprise.adobe.io/mcp` | · [Strumenti di Adobe Journey Optimizer](https://developer.adobe.com/ai-registry/#/mcp/ajo-mcp-server)<br>· [Strumenti di Customer Journey Analytics](https://developer.adobe.com/ai-registry/#/mcp/cja-mcp)<br>· [Strumenti di Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/mcp/rtcdp-mcp) |
| [Adobe Analytics](https://developer.adobe.com/analytics-mcp/docs/aa/) | `https://aa-mcp.adobe.io/mcp` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/adobe-analytics-mcp) |
| [AEM Cloud Manager](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) | `https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-cloud-manager-mcp) |
| [Contenuto AEM](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp) |
| [Contenuto AEM (Sola Lettura)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/using-mcp-with-aem-as-a-cloud-service) | `https://mcp.adobeaemcloud.com/adobe/mcp/content-readonly` | [Visualizza strumenti](https://developer.adobe.com/ai-registry/#/mcp/aem-content-mcp-readonly) |

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

Eseguire `claude mcp add` per registrare il gateway MCP di CX Enterprise. Una connessione consente di accedere agli strumenti di AJO, CJA e Real-Time CDP in base alle licenze dell’organizzazione.

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

Aggiungere il gateway MCP di CX Enterprise al file di configurazione del cursore `mcp.json`, quindi connettersi tramite **Impostazioni > MCP**.

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

Una voce gateway consente di accedere a AJO, CJA e Real-Time CDP in base alle licenze dell’organizzazione.

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

Aggiungere il gateway MCP aziendale CX:

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
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* ../use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* ../use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* ../use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* ../use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine the CX Enterprise MCP Gateway and AEM Content MCP Server to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* ../use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Use the CX Enterprise MCP Gateway for a unified view of AJO, CJA, and Real-Time CDP campaign health in one AI session.}
  {cta = Start walkthrough}
-->
