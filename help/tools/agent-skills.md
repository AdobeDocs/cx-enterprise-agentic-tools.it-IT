---
title: Abilità agente
description: Flussi di lavoro curati da Adobe e istruzioni che guidano gli agenti di intelligenza artificiale attraverso le attività aziendali di CX in modo coerente.
last-substantial-update: 2026-05-19T00:00:00Z
index: false
source-git-commit: 1681b6de9d0459ed9d5420f77048778712cd0004
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 6%

---


# Abilità agente

<!-- last-modified: 2026-05-19 -->

![Abilità agente per Adobe CX Enterprise](../assets/hero-agent-skills.png)

Le abilità degli agenti sono flussi di lavoro curati da Adobe che forniscono agli agenti di intelligenza artificiale istruzioni dettagliate per il completamento affidabile delle attività aziendali di Adobe CX. Ogni abilità dell’agente codifica l’esperienza nel dominio e le best practice in modo che gli agenti producano risultati coerenti e convalidati senza dover improvvisare. Le abilità dell’agente hanno senso quando desideri un comportamento ripetibile e guidato nelle conversazioni, in particolare per attività che altrimenti richiederebbero ogni volta una richiesta di conferma dettagliata. Integrano i server e le API MCP: le abilità dell’agente definiscono il funzionamento di un agente; i server e le API MCP forniscono l’accesso sottostante.

Tutte le abilità dell&#39;agente vengono mantenute nell&#39;archivio [Adobe Skills GitHub](https://github.com/adobe/skills), che è l&#39;origine principale per la documentazione, l&#39;installazione e i dettagli di implementazione dell&#39;abilità dell&#39;agente.

## Competenze di Adobe CX Enterprise Agent

Tutte le abilità dell&#39;agente vengono mantenute nell&#39;archivio [Adobe Skills GitHub](https://github.com/adobe/skills). Seleziona un’area di funzionalità in basso per esplorare le abilità per quel flusso di lavoro.

<!--
CARDS

* https://github.com/adobe/skills/tree/main/plugins/aem
  {title = Adobe Experience Manager}
  {description = Agent Skills for Experience Manager development, content, design, and project management across AEM as a Cloud Service, Edge Delivery Services, and AEM 6.5 LTS.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-aem-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-analytics
  {title = Adobe Analytics}
  {description = Agent Skills for KPI monitoring, funnel analysis, and executive reporting workflows in Adobe Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-analytics-card.png}

* https://github.com/adobe/skills/tree/main/plugins/adobe-cja
  {title = Customer Journey Analytics}
  {description = Agent Skills for performance comparison, dimension analysis, and workspace authoring in Customer Journey Analytics.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cja-card.png}

* https://github.com/adobe/skills/tree/main/plugins/app-builder
  {title = Adobe App Builder}
  {description = Agent Skills for scaffolding, testing, and deploying custom applications with Adobe App Builder.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-cxenterprise-card.png}

* https://github.com/adobe/skills/tree/main/plugins/creative-cloud
  {title = Creative Cloud}
  {description = Agent Skills for batch photo editing, design from templates, video editing, and social media variants with Creative Cloud.}
  {cta = View Agent Skills}
  {target = _blank}
  {image = ../assets/agent-skills-creative-cloud.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Experience Manager">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/aem" title="Adobe Experience Manager" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-aem-card.png" alt="Adobe Experience Manager"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" title="Adobe Experience Manager">Adobe Experience Manager</a>
                    </p>
                    <p class="is-size-6">Competenze degli agenti per lo sviluppo, il contenuto, la progettazione e la gestione dei progetti Experience Manager in AEM as a Cloud Service, Edge Delivery Services e AEM 6.5 LTS.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/aem" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" title="Adobe Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-analytics-card.png" alt="Adobe Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" title="Adobe Analytics">Adobe Analytics</a>
                    </p>
                    <p class="is-size-6">Abilità dell’agente per i flussi di lavoro di monitoraggio dei KPI, analisi funnel e reporting manageriale in Adobe Analytics.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-analytics" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Customer Journey Analytics">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" title="Customer Journey Analytics" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cja-card.png" alt="Customer Journey Analytics"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" title="Customer Journey Analytics">Customer Journey Analytics</a>
                    </p>
                    <p class="is-size-6">Abilità dell’agente per il confronto delle prestazioni, l’analisi delle dimensioni e la creazione di aree di lavoro in Customer Journey Analytics.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/adobe-cja" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Adobe App Builder">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" title="Adobe App Builder" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-cxenterprise-card.png" alt="Adobe App Builder"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" title="Adobe App Builder">Adobe App Builder</a>
                    </p>
                    <p class="is-size-6">Abilità dell’agente per lo scaffolding, il test e la distribuzione di applicazioni personalizzate con Adobe App Builder.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/app-builder" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Creative Cloud">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" title="Creative Cloud" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/agent-skills-creative-cloud.png" alt="Creative Cloud"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" title="Creative Cloud">Creative Cloud</a>
                    </p>
                    <p class="is-size-6">Competenze dell’agente per la modifica di foto in batch, la progettazione da modelli, la modifica di video e varianti di social media con Creative Cloud.</p>
                </div>
                <a href="https://github.com/adobe/skills/tree/main/plugins/creative-cloud" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Visualizza le abilità dell'agente</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->


Per informazioni dettagliate sulle competenze, i metodi di installazione e il codice sorgente, consulta l&#39;[archivio GitHub Adobe Skills](https://github.com/adobe/skills).

## Funzionamento delle abilità dell’agente

![Funzionamento delle abilità dell&#39;agente](../assets/hero-connect-agent-skills.gif)

Un’abilità agente è un insieme di istruzioni che indica a un agente di intelligenza artificiale come completare un’attività utilizzando gli strumenti di Adobe per gli agenti. Quando un agente carica un’abilità, segue quel flusso di lavoro anziché improvvisare.

- Gli agenti completano le attività sempre nello stesso modo
- L’esperienza del dominio viene codificata una volta e riutilizzata nelle conversazioni
- Le abilità possono concatenare più strumenti e azioni agenti in un unico flusso di lavoro

## Introduzione

Le abilità dell’agente vengono installate in base al client di intelligenza artificiale in uso. Alcuni client supportano l&#39;installazione diretta dalla riga di comando:

- **Codice Claude**: `/plugin install adobe/skills`
- **Ambienti nodo**: `npx skills add adobe/skills`
- **CLI GitHub**: `gh upskill adobe/skills`

Altri client richiedono di scaricare e aggiungere i file delle competenze direttamente al client di intelligenza artificiale. Per istruzioni complete sull&#39;installazione da parte del client, consulta il file README delle [abilità di Adobe su GitHub](https://github.com/adobe/skills#installation).

### Ricerca delle abilità dell’agente

Sfoglia l&#39;elenco completo delle abilità disponibili nell&#39;archivio [Adobe Skills GitHub](https://github.com/adobe/skills). Ogni abilità agente include un file `SKILL.md` con istruzioni dettagliate, riferimenti ed esempi.

Dopo aver installato o aggiunto il pacchetto `adobe/skills`, alcuni client di IA ti consentono di elencare direttamente tutte le abilità disponibili:

- **Codice Claude**: `claude /plugin list`
- **Ambienti nodo**: `npx skills list`
- **CLI GitHub**: `gh upskill list`

## Competenze agente e server MCP e API per i generatori

| | Abilità agente | Server MCP | API per builder |
| --- | --- | --- | --- |
| Scopo | Flussi di lavoro guidati e best practice | Accesso ai dati e ai flussi di lavoro di Adobe | Integrazione diretta del sistema |
| Codifica competenze di dominio | Sì | No | No |
| Richiede la codifica | No | No | Sì |
| Ideale per | Attività ripetibili e guidate | Query di dati e azioni del flusso di lavoro | Sviluppo di applicazioni personalizzate |
