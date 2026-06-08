---
title: Strumenti di Adobe CX Enterprise Agent
description: Collegare gli agenti di intelligenza artificiale e gli strumenti di sviluppo alle funzionalità di Adobe CX Enterprise utilizzando i server MCP, le competenze degli agenti e le API.
index: false
source-git-commit: 5b9dc2c695ad0bd30a4776f838d25b5ed13e5b45
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 1%

---


# Strumenti di Adobe CX Enterprise Agent

<!-- last-modified: 2026-05-08 -->

>[!VIDEO](https://video.tv.adobe.com/v/3491252/?captions=ita&learn=on&enablevpops)

Assegna all&#39;intelligenza artificiale una linea diretta per **dati, flussi di lavoro e automazione di Adobe CX Enterprise**. Esegui query sulle campagne, attiva tipi di pubblico e gestisci percorsi in **linguaggio semplice** da qualsiasi client di IA o strumento di sviluppo compatibile.

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
                    <a href="tools/mcp-servers.md" title="Server MCP" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="Server MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="Server MCP">Server MCP</a>
                    </p>
                    <p class="is-size-6">Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise. Esegui query sui dati, analizza le campagne e accedi ai tipi di pubblico senza uscire dallo strumento di intelligenza artificiale.</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora server MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="Abilità agente" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="Abilità agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="Abilità agente">Abilità agente</a>
                    </p>
                    <p class="is-size-6">Workflow curati da Adobe che guidano gli agenti attraverso le attività di CX Enterprise. Esperienza del dominio codificata una volta, applicata in modo coerente.</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="API per builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="API per builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/apis.md" target="_blank" rel="referrer" title="API per builder">API per i generatori</a>
                    </p>
                    <p class="is-size-6">Crea applicazioni Adobe CX Enterprise personalizzate utilizzando strumenti di codifica agentici come Claude Code e Cursor.</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le API per i generatori</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/mcp-servers.md" title="Server MCP" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/mcp-servers-card.png" alt="Server MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/mcp-servers.md" target="_blank" rel="referrer" title="Server MCP">Server MCP</a>
                    </p>
                    <p class="is-size-6">Collegare qualsiasi client AI compatibile con MCP ai flussi di lavoro Adobe CX Enterprise. Esegui query sui dati, analizza le campagne e accedi ai tipi di pubblico senza uscire dallo strumento di intelligenza artificiale.</p>
                </div>
                <a href="tools/mcp-servers.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora server MCP</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/agent-skills.md" title="Abilità agente" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/agent-skills-card.png" alt="Abilità agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/agent-skills.md" target="_blank" rel="referrer" title="Abilità agente">Abilità agente</a>
                    </p>
                    <p class="is-size-6">Workflow curati da Adobe che guidano gli agenti attraverso le attività di CX Enterprise. Esperienza del dominio codificata una volta, applicata in modo coerente.</p>
                </div>
                <a href="tools/agent-skills.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="tools/apis.md" title="API per builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="assets/apis-card.png" alt="API per builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="tools/apis.md" target="_blank" rel="referrer" title="API per builder">API per i generatori</a>
                    </p>
                    <p class="is-size-6">Crea applicazioni Adobe CX Enterprise personalizzate utilizzando strumenti di codifica agentici come Claude Code e Cursor.</p>
                </div>
                <a href="tools/apis.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le API per i generatori</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Strumenti agenti per ogni team

>[!BEGINTABS]

>[!TAB Business Leader]

Comprendi il valore aziendale degli strumenti Adobe per gli agenti e come estendono il tuo investimento Adobe.

- Gli agenti accelerano i flussi di lavoro operativi e di marketing senza sostituire il team
- I controlli di accesso, gli audit trail e i flussi di lavoro human-in-the-loop sono incorporati fin dall’inizio
- Gli strumenti agenti funzionano su qualsiasi client di intelligenza artificiale compatibile, non solo sulle superfici di Adobe
- I dati rimangono nell&#39;ambiente, governato dalle autorizzazioni

Consulta [procedure dettagliate reali](agentic-tools-in-action.md) per capire cosa fanno oggi i team con questi strumenti di gestione.

>[!TAB Utenti aziendali]

Scopri in che modo gli strumenti di gestione accelerano i flussi di lavoro quotidiani di Adobe.

- Connetti il client di intelligenza artificiale ai dati di Adobe in pochi minuti utilizzando [Server MCP](tools/mcp-servers.md)
- Segui le procedure dettagliate dettagliate per le attività comuni di [campaign](use-cases/analyze-campaign-performance.md), [audience](use-cases/query-audiences.md) e [percorso](use-cases/manage-ajo-journeys.md)
- Utilizzare l’ambiente di intelligenza artificiale già in uso

>[!TAB Generatori e sviluppatori]

Integrazione delle funzionalità di Adobe CX Enterprise in applicazioni e agenti personalizzati.

- Sfoglia le [API per i generatori](tools/apis.md) in base all&#39;area delle funzionalità e connettiti ai [server MCP](tools/mcp-servers.md) nell&#39;ambiente di sviluppo
- Utilizza strumenti di codifica basati sull&#39;intelligenza artificiale come [Claude Code](https://docs.anthropic.com/en/docs/claude-code/mcp) e [Cursor](https://cursor.com/docs/mcp) insieme alle API di Adobe
- Configura autenticazione e credenziali in [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)
- Consulta [Server MCP](tools/mcp-servers.md) per un elenco completo dei client di intelligenza artificiale supportati e istruzioni di configurazione

>[!TAB Amministratori]

Gestisci l’accesso, gestisci gli strumenti di gestione approvati e mantieni la supervisione all’interno dell’organizzazione.

- Configura l&#39;autenticazione per i server e le API MCP tramite [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/)
- Configurare le autorizzazioni a livello di organizzazione di Identity Management System (IMS) per controllare quali utenti e team possono accedere agli strumenti per gli agenti
- Definire e applicare quali client AI e server MCP sono approvati per l’utilizzo all’interno dell’organizzazione
- Monitora l’utilizzo, esamina gli audit trail e assicurati che l’attività degli agenti soddisfi i requisiti di conformità

Consulta [Server MCP](tools/mcp-servers.md) per la configurazione dell&#39;autenticazione e [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) per la gestione delle credenziali e dei progetti.

>[!ENDTABS]

## Strumenti agenti in azione

Scopri l’aspetto pratico degli strumenti per agenti Adobe CX Enterprise. Ogni procedura dettagliata descrive uno scenario di business reale, dalla configurazione al risultato, mostrando esattamente come collegare un client di intelligenza artificiale, cosa chiedere e cosa ottenere indietro.

<!--
CARDS

* use-cases/analyze-campaign-performance.md
  {title = Analyze campaign performance}
  {description = Use the CX Enterprise MCP Gateway to surface Customer Journey Analytics metrics and insights from any AI client.}
  {cta = Start walkthrough}

* use-cases/query-audiences.md
  {title = Query audiences}
  {description = Use the CX Enterprise MCP Gateway to query Real-Time CDP audience and destination data using plain language prompts.}
  {cta = Start walkthrough}

* use-cases/manage-ajo-journeys.md
  {title = Review AJO journeys}
  {description = Use the CX Enterprise MCP Gateway to access AJO journeys, campaign status, and journey conditions from your AI client.}
  {cta = Start walkthrough}

* use-cases/manage-aem-content.md
  {title = Manage AEM content with AI}
  {description = Discover, update, and publish pages and content fragments in AEM using natural language.}
  {cta = Start walkthrough}

* use-cases/optimize-content-with-performance-data.md
  {title = Optimize content based on performance data}
  {description = Combine CJA and AEM MCP Servers to find underperforming content and update it in one session.}
  {cta = Start walkthrough}

* use-cases/cross-channel-campaign-review.md
  {title = Run a cross-channel campaign review}
  {description = Connect AJO, CJA, and Real-Time CDP in one AI session for a unified view of campaign health.}
  {cta = Start walkthrough}
-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="Analizzare le prestazioni della campagna" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="Analizzare le prestazioni della campagna"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analizzare le prestazioni della campagna">Analizzare le prestazioni della campagna</a>
                    </p>
                    <p class="is-size-6">Utilizza il gateway MCP aziendale CX per ottenere metriche e informazioni Customer Journey Analytics da qualsiasi client AI.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/query-audiences.md" title="Eseguire query sui tipi di pubblico" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="Eseguire query sui tipi di pubblico"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" title="Eseguire query sui tipi di pubblico">Interroga tipi di pubblico</a>
                    </p>
                    <p class="is-size-6">Utilizzare il gateway MCP di CX Enterprise per eseguire query sui dati relativi al pubblico e alla destinazione di Real-Time CDP utilizzando prompt in linguaggio semplice.</p>
                </div>
                <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-ajo-journeys.md" title="Rivedi percorsi AJO" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="Rivedi percorsi AJO"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Rivedi percorsi AJO">Rivedi percorsi AJO</a>
                    </p>
                    <p class="is-size-6">Utilizzare il gateway MCP di CX Enterprise per accedere ai percorsi AJO, allo stato della campagna e alle condizioni di percorso dal client AI.</p>
                </div>
                <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="Gestire i contenuti AEM con IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="Gestire i contenuti AEM con IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Gestire i contenuti AEM con IA">Gestire i contenuti AEM con IA</a>
                    </p>
                    <p class="is-size-6">Scopri, aggiorna e pubblica pagine e frammenti di contenuto in AEM utilizzando il linguaggio naturale.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/optimize-content-with-performance-data.md" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="Ottimizzazione dei contenuti in base ai dati sulle prestazioni"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni">Ottimizza il contenuto in base ai dati sulle prestazioni</a>
                    </p>
                    <p class="is-size-6">Combina i server CJA e AEM MCP per trovare i contenuti insoddisfacenti e aggiornarli in una sessione.</p>
                </div>
                <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/cross-channel-campaign-review.md" title="Eseguire una revisione di una campagna cross-channel" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Eseguire una revisione di una campagna cross-channel"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Eseguire una revisione di una campagna cross-channel">Eseguire una revisione della campagna cross-channel</a>
                    </p>
                    <p class="is-size-6">Connetti AJO, CJA e Real-Time CDP in una sessione di intelligenza artificiale per una visualizzazione unificata dell’integrità della campagna.</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Analyze campaign performance">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/analyze-campaign-performance.md" title="Analizzare le prestazioni della campagna" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Analyze+Campaign+Performance" alt="Analizzare le prestazioni della campagna"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" title="Analizzare le prestazioni della campagna">Analizzare le prestazioni della campagna</a>
                    </p>
                    <p class="is-size-6">Utilizza il gateway MCP aziendale CX per ottenere metriche e informazioni Customer Journey Analytics da qualsiasi client AI.</p>
                </div>
                <a href="use-cases/analyze-campaign-performance.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Query audiences">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/query-audiences.md" title="Eseguire query sui tipi di pubblico" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Query+Audiences" alt="Eseguire query sui tipi di pubblico"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" title="Eseguire query sui tipi di pubblico">Interroga tipi di pubblico</a>
                    </p>
                    <p class="is-size-6">Utilizzare il gateway MCP di CX Enterprise per eseguire query sui dati relativi al pubblico e alla destinazione di Real-Time CDP utilizzando prompt in linguaggio semplice.</p>
                </div>
                <a href="use-cases/query-audiences.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Review AJO journeys">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-ajo-journeys.md" title="Rivedi percorsi AJO" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Review+AJO+Journeys" alt="Rivedi percorsi AJO"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" title="Rivedi percorsi AJO">Rivedi percorsi AJO</a>
                    </p>
                    <p class="is-size-6">Utilizzare il gateway MCP di CX Enterprise per accedere ai percorsi AJO, allo stato della campagna e alle condizioni di percorso dal client AI.</p>
                </div>
                <a href="use-cases/manage-ajo-journeys.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Manage AEM content with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/manage-aem-content.md" title="Gestire i contenuti AEM con IA" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Manage+AEM+Content+with+AI" alt="Gestire i contenuti AEM con IA"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" title="Gestire i contenuti AEM con IA">Gestire i contenuti AEM con IA</a>
                    </p>
                    <p class="is-size-6">Scopri, aggiorna e pubblica pagine e frammenti di contenuto in AEM utilizzando il linguaggio naturale.</p>
                </div>
                <a href="use-cases/manage-aem-content.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Optimize content based on performance data">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/optimize-content-with-performance-data.md" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Optimize+Content+Based+on+Performance+Data" alt="Ottimizzazione dei contenuti in base ai dati sulle prestazioni"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" title="Ottimizzazione dei contenuti in base ai dati sulle prestazioni">Ottimizza il contenuto in base ai dati sulle prestazioni</a>
                    </p>
                    <p class="is-size-6">Combina i server CJA e AEM MCP per trovare i contenuti insoddisfacenti e aggiornarli in una sessione.</p>
                </div>
                <a href="use-cases/optimize-content-with-performance-data.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Run a cross-channel campaign review">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="use-cases/cross-channel-campaign-review.md" title="Eseguire una revisione di una campagna cross-channel" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="https://placehold.co/1600x900?text=Cross-Channel+Campaign+Review" alt="Eseguire una revisione di una campagna cross-channel"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" title="Eseguire una revisione di una campagna cross-channel">Eseguire una revisione della campagna cross-channel</a>
                    </p>
                    <p class="is-size-6">Connetti AJO, CJA e Real-Time CDP in una sessione di intelligenza artificiale per una visualizzazione unificata dell’integrità della campagna.</p>
                </div>
                <a href="use-cases/cross-channel-campaign-review.md" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Inizia procedura dettagliata</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->

## Risorse di Adobe

| Risorsa | Cosa troverai |
| --- | --- |
| [Registro di sistema di Adobe AI](https://developer.adobe.com/ai-registry/?type=mcp) | Catalogo completo dei server MCP disponibili e delle competenze dell&#39;agente |
| [Catalogo API Adobe](https://developer.adobe.com/apis) | Riferimento API completo di Adobe CX Enterprise |
| [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/) | Configurazione e autenticazione del progetto API |
| [Experience League](https://experienceleague.adobe.com/it/docs/experience-cloud-ai/experience-cloud-ai/home) | Documentazione e tutorial completi sulle applicazioni Adobe |
