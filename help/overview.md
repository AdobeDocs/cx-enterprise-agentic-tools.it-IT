---
title: Strumenti di Adobe CX Enterprise Agent
description: Collegare gli agenti di intelligenza artificiale e gli strumenti di sviluppo alle funzionalità di Adobe CX Enterprise utilizzando i server MCP, le competenze degli agenti e le API.
last-substantial-update: 2026-06-08T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '803'
ht-degree: 2%

---


# Strumenti di Adobe CX Enterprise Agent

<!-- last-modified: 2026-06-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491235/?learn=on&enablevpops)

Con AI puoi diventare il tuo collaboratore per Adobe CX Enterprise. Connetti il tuo client di intelligenza artificiale a campagne, tipi di pubblico, percorsi e contenuti. Interagisci con loro in linguaggio semplice da qualsiasi strumento già utilizzato. Nessuna nuova interfaccia, nessun cambio di contesto, nessuna codifica necessaria per iniziare.

>[!TIP]
>**Inizia con CX Enterprise MCP.** Una connessione consente al client di intelligenza artificiale di accedere a Adobe Journey Optimizer, Customer Journey Analytics e Real-Time CDP in base alle licenze della tua organizzazione. [Connetti ora](tools/mcp-servers.md#cx-enterprise-mcp-servers)

<!--
CARDS

* tools/mcp-servers.md
  {title = MCP Servers}
  {description = Connect any MCP-compatible AI client to Adobe CX Enterprise workflows. Query data, analyze campaigns, and access audiences without leaving your AI tool.}
  {cta = Explore MCP Servers}
  {image = assets/mcp-servers-card.png}

* tools/agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflows that guide agents through CX Enterprise tasks. Domain expertise encoded once, applied consistently.}
  {cta = Explore Agent Skills}
  {image = assets/agent-skills-card.png}

* tools/apis.md
  {title = APIs for Builders}
  {description = Build custom Adobe CX Enterprise applications using agentic coding tools like Claude Code and Cursor.}
  {cta = Explore APIs for Builders}
  {image = assets/apis-card.png}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="Server MCP">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="Server MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" title="Server MCP">Server MCP</a>
                    </p>
                    <p class="is-size-6">Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise. Esegui query sui dati, analizza le campagne e accedi ai tipi di pubblico senza uscire dallo strumento di intelligenza artificiale.</p>
                </div>
                <a href="tools/mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora server MCP</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="Abilità agente">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="Abilità agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" title="Abilità agente">Abilità agente</a>
                    </p>
                    <p class="is-size-6">Workflow curati da Adobe che guidano gli agenti attraverso le attività di CX Enterprise. Esperienza del dominio codificata una volta, applicata in modo coerente.</p>
                </div>
                <a href="tools/agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le abilità dell'agente</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="API per builder">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="API per builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/apis.md" title="API per builder">API per i generatori</a>
                    </p>
                    <p class="is-size-6">Crea applicazioni Adobe CX Enterprise personalizzate utilizzando strumenti di codifica agentici come Claude Code e Cursor.</p>
                </div>
                <a href="tools/apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le API per i generatori</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Strumenti agenti per ogni team

>[!BEGINTABS]

>[!TAB Server MCP]

Utilizzare qualsiasi client AI compatibile per accedere alle applicazioni CX Enterprise in linguaggio semplice. Non è richiesta alcuna codifica. Inizia con CX Enterprise MCP per una singola connessione ad AJO, CJA e Real-Time CDP, oppure per collegarti direttamente ad AEM e ad altre applicazioni.

- Connessione in pochi minuti da Claude, Cursor, ChatGPT e altri client compatibili con MCP
- Eseguire query su campagne, tipi di pubblico e dati di percorso utilizzando il linguaggio naturale
- Nessuna nuova interfaccia o formazione richiesta

[Introduzione ai server MCP](tools/mcp-servers.md)

>[!TAB Abilità agente]

Le abilità dell’agente codificano l’esperienza nel dominio Adobe come istruzioni che il client di intelligenza artificiale può seguire. Invece di improvvisare, l’agente sa esattamente cosa fare, in modo affidabile, ripetibile e allineato alle best practice di Adobe.

- Risultati coerenti per flussi di lavoro aziendali CX ripetibili
- Non è necessario spiegare Adobe all’agente: l’abilità la gestisce
- Funziona tra client AI che supportano le competenze degli agenti

[Esplora abilità agente](tools/agent-skills.md)

>[!TAB API per i generatori]

Accesso diretto e programmatico alle stesse API che alimentano i prodotti Adobe. Creazione di applicazioni e integrazioni personalizzate che offrono al team un accesso mirato e gestito a specifici flussi di lavoro aziendali CX.

- Genera una volta e implementa in tutta l’organizzazione
- Aggiungi guardrail, approvazioni e logica personalizzata di cui il tuo team ha bisogno
- Utilizza Claude Code, Cursor e altri strumenti di codifica per creare più rapidamente

[Esplora le API per i generatori](tools/apis.md)

>[!ENDTABS]

## Strumenti agenti in azione

Scopri l’aspetto pratico degli strumenti per agenti Adobe CX Enterprise. Ogni procedura dettagliata descrive uno scenario di business reale, dalla configurazione al risultato, mostrando esattamente come collegare un client di intelligenza artificiale, cosa chiedere e cosa ottenere indietro.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Campaign insights without reports}
  {description = Ask performance questions in plain language and get answers from Customer Journey Analytics, without building a single report.}
  {cta = Surface campaign insights}

* use-cases/manage-aem-content.md
  {title = Ship content updates faster}
  {description = Find, update, and publish AEM pages and content fragments faster, without switching to the AEM interface.}
  {cta = Ship content faster}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Campaign insights without reports">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="Informazioni sulla campagna senza rapporti">
                        <img class="is-bordered-r-small" src="assets/use-cases/analyze-campaign-performance/analyze-campaign-performance-step5-02-actions.png" alt="Informazioni sulla campagna senza rapporti"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" title="Informazioni sulla campagna senza rapporti">Informazioni sulla campagna senza rapporti</a>
                    </p>
                    <p class="is-size-6">Poni le domande sulle prestazioni in un linguaggio semplice e ottieni risposte da Customer Journey Analytics, senza creare un singolo rapporto.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Informazioni sulla campagna Surface</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Ship content updates faster">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="Spedisci aggiornamenti contenuti più rapidamente">
                        <img class="is-bordered-r-small" src="assets/use-cases/manage-aem-content/manage-aem-content-step4-02-product.png" alt="Spedisci aggiornamenti contenuti più rapidamente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" title="Spedisci aggiornamenti contenuti più rapidamente">Spedisci aggiornamenti contenuti più rapidamente</a>
                    </p>
                    <p class="is-size-6">Trova, aggiorna e pubblica più rapidamente le pagine AEM e i frammenti di contenuto, senza passare all’interfaccia di AEM.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Spedire i contenuti più velocemente</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

**[Visualizza tutte le procedure dettagliate](use-cases/overview.md)**

## Risorse di Adobe

| Risorsa | Cosa troverai |
| --- | --- |
| [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=mcp) | Connettori gestiti e dettagli del server per determinati server Adobe MCP |
| [Abilità agente Adobe](https://github.com/adobe/skills) | Competenze degli agenti curate da Adobe per i flussi di lavoro aziendali CX |
| [Catalogo API Adobe](https://developer.adobe.com/apis) | Riferimento API completo di Adobe CX Enterprise |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | Configurazione e autenticazione del progetto API |
| [Adobe Admin Console](https://adminconsole.adobe.com) | Gestione dell’accesso a utenti e prodotti |
| [Experience League](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home) | Documentazione e tutorial completi sulle applicazioni Adobe |
