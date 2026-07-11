---
title: Strumenti agenti
description: Confrontate i server MCP, le competenze dell'agente e le API per i generatori e scegliete lo strumento agentico adatto per i flussi di lavoro Adobe CX Enterprise.
last-substantial-update: 2026-06-08T00:00:00Z
source-git-commit: 40d93f878ba9f48c9daffd3beccb4bf829113a36
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 0%

---


# Strumenti agenti

<!-- last-modified: 2026-06-08 -->

Non tutti gli strumenti agentici rispondono alle stesse esigenze. Scopri cosa fanno le persone, quando usarle e come iniziare, in modo da poter scegliere il punto di partenza giusto per la tua situazione.

<!--
CARDS

* mcp-servers.md
  {title = MCP Servers}
  {description = Connect any compatible AI client to Adobe CX Enterprise data and workflows. No coding required.}
  {cta = Explore MCP Servers}
  {image = ../assets/mcp-servers-card.png}

* agent-skills.md
  {title = Agent Skills}
  {description = Adobe-curated workflow instructions that guide agents through CX Enterprise tasks consistently.}
  {cta = Explore Agent Skills}
  {image = ../assets/agent-skills-card.png}

* apis.md
  {title = APIs for Builders}
  {description = Build custom applications and integrations using the same APIs that power Adobe products.}
  {cta = Explore APIs for Builders}
  {image = ../assets/apis-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="MCP Servers">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="mcp-servers.md" title="Server MCP">
                        <img class="is-bordered-r-small" src="../assets/mcp-servers-card.png" alt="Server MCP"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="mcp-servers.md" title="Server MCP">Server MCP</a>
                    </p>
                    <p class="is-size-6">Collegare qualsiasi client AI compatibile ai dati e ai flussi di lavoro di Adobe CX Enterprise. Non è richiesta alcuna codifica.</p>
                </div>
                <a href="mcp-servers.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora server MCP</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Agent Skills">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="agent-skills.md" title="Abilità agente">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Abilità agente"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="agent-skills.md" title="Abilità agente">Abilità agente</a>
                    </p>
                    <p class="is-size-6">Istruzioni per i flussi di lavoro curate da Adobe che guidano gli agenti attraverso le attività aziendali di CX in modo coerente.</p>
                </div>
                <a href="agent-skills.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le abilità dell'agente</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="APIs for Builders">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="apis.md" title="API per builder">
                        <img class="is-bordered-r-small" src="../assets/apis-card.png" alt="API per builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="apis.md" title="API per builder">API per i generatori</a>
                    </p>
                    <p class="is-size-6">Crea applicazioni e integrazioni personalizzate utilizzando le stesse API che alimentano i prodotti Adobe.</p>
                </div>
                <a href="apis.md" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Esplora le API per i generatori</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


## Confrontare gli strumenti di gestione degli agenti

| | Server MCP | Abilità agente | API per builder |
| --- | --- | --- | --- |
| Ideale per | Utenti delle applicazioni aziendali CX | Utenti e sviluppatori di applicazioni aziendali CX | Sviluppatori |
| Richiede la codifica | No | No | Sì |
| Tempo di configurazione | Minutes | Minutes | Da ore a giorni |
| I risultati ottenuti | Accesso alle applicazioni CX Enterprise dai client AI | Workflow guidati e ripetibili | Controllo programmatico completo |

## Non sei sicuro di dove iniziare?

- Per utilizzare l&#39;intelligenza artificiale per interagire con le applicazioni CX Enterprise (eseguendo azioni, eseguendo query sui dati e consentendo all&#39;intelligenza artificiale di scoprire cosa fare dopo attraverso una conversazione naturale), i [server MCP](mcp-servers.md) sono il punto di partenza più flessibile.
- Per fare in modo che gli agenti seguano in modo coerente le best practice di Adobe per i flussi di lavoro aziendali CX senza eseguire improvvisazioni, [Le abilità dell&#39;agente](agent-skills.md) codificano tale esperienza del dominio in istruzioni riutilizzabili.
- Per creare un&#39;applicazione mirata che semplifichi o automatizzi un flusso di lavoro aziendale CX specifico per gli utenti, le [API per i generatori](apis.md) forniscono un controllo diretto e programmabile su ciò che accade.

>[!BEGINTABS]

>[!TAB Server MCP]

Considera i server MCP come un collegamento in tempo reale tra il client AI e le applicazioni CX Enterprise. Connettiti una volta e la tua intelligenza artificiale può eseguire query sulle campagne, richiamare tipi di pubblico, controllare lo stato del percorso e altro ancora, il tutto in un linguaggio semplice, senza bisogno di codice.

**Utilizzare i server MCP quando:**

- Desideri integrare l’intelligenza artificiale direttamente nei flussi di lavoro aziendali di CX
- Si desidera inserire i dati CX Enterprise nel client AI già utilizzato
- Stai effettuando analisi esplorative o recupero di dati ad hoc
- Desideri risultati veloci, senza far ruotare un progetto

[Esplora server MCP](mcp-servers.md)

>[!TAB Abilità agente]

Le abilità dell’agente sono competenze sul dominio di Adobe, codificate come istruzioni che l’agente può seguire. Invece di sperare che l&#39;agente definisca i passaggi corretti, un&#39;abilità gli indica esattamente cosa fare, in modo affidabile, ripetibile e già ottimizzato per i flussi di lavoro aziendali CX.

**Utilizza le abilità dell&#39;agente quando:**

- Desideri seguire le best practice di Adobe durante l’esecuzione di lavoro nelle app CX Enterprise tramite client AI
- Si desidera eseguire sempre la stessa operazione nello stesso modo
- Esecuzione di flussi di lavoro di produzione di contenuti o supporti ripetibili

[Esplora abilità agente](agent-skills.md)

>[!TAB API per i generatori]

Le API sono gli elementi costitutivi. Offrono agli sviluppatori un accesso diretto e programmatico ai dati e alle operazioni di Adobe, utilizzando le stesse API che alimentano i prodotti di Adobe. Utilizzale per creare esperienze personalizzate mirate che semplificano flussi di lavoro aziendali specifici con le protezioni di cui la tua organizzazione ha bisogno.

**Utilizza le API quando:**

- Creazione di un&#39;applicazione o integrazione personalizzata per un caso d&#39;uso aziendale specifico
- È necessario ottimizzare o automatizzare un flusso di lavoro con guardrail e controlli specifici
- Stai usando Claude Code o Cursor per generare un&#39;applicazione completa
- È necessario integrare i dati di CX Enterprise in un altro sistema

[Esplora le API per i generatori](apis.md)

>[!ENDTABS]

## Utilizzarli insieme

Questi strumenti sono progettati per funzionare insieme. La combinazione di questi elementi è il modo in cui si ottiene il massimo da Adobe AI. Le competenze degli agenti possono guidare l&#39;utilizzo dei server MCP da parte dei client di intelligenza artificiale, mantenendo gli agenti sulla strada giusta per i flussi di lavoro aziendali di CX. Le abilità possono anche informare su come e quando chiamare le API, aggiungendo guardrail di best practice di Adobe alle automazioni personalizzate. Non devi sceglierne solo uno.

## Strumenti agenti in azione

Questi strumenti vengono applicati ai flussi di lavoro aziendali reali di CX.

<!--
CARDS

* ../use-cases/query-audiences.md
  {title = Audience activation at a glance}
  {description = See which audiences are live, where they are flowing, and whether destinations are healthy, without navigating Real-Time CDP.}
  {cta = Check audience activation}

* https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development
  {title = Develop AEM components with AI}
  {description = Use Claude Code or Cursor with Agent Skills to scaffold, code, and refine AEM components guided by Adobe best practices.}
  {cta = Try with Agent Skills}
  {image = ../assets/agent-skills-card.png}

* https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
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
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Develop AEM components with AI">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" title="Sviluppare componenti AEM con AI" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-card.png" alt="Sviluppare componenti AEM con AI"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" title="Sviluppare componenti AEM con AI">Sviluppa componenti AEM con IA</a>
                    </p>
                    <p class="is-size-6">Utilizza Claude Code o Cursor con Abilità di agente per impalcare, codificare e perfezionare i componenti AEM guidati dalle best practice di Adobe.</p>
                </div>
                <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/ai-assisted-development/use-cases/component-development" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Prova con le abilità agente</span>
                
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Richiama le API di AEM da un’app web" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Richiama le API di AEM da un’app web"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Richiama le API di AEM da un’app web">Richiama API AEM da un'app Web</a>
                    </p>
                    <p class="is-size-6">Crea un’applicazione web che autentica gli utenti e chiama le API aperte di AEM utilizzando OAuth per fornire un accesso regolamentato e programmatico.</p>
                </div>
                <a href="https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Prova con le API</span>
                
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
