---
title: API per builder
description: Creare applicazioni e integrazioni personalizzate utilizzando le API Adobe CX Enterprise.
last-substantial-update: 2026-06-02T00:00:00Z
index: false
source-git-commit: f7ace53bd5988b5902659c89c6da16448398e0c0
workflow-type: tm+mt
source-wordcount: '886'
ht-degree: 9%

---


# API per generatori

<!-- last-modified: 2026-06-02 -->

![API Adobe CX Enterprise](../assets/hero-apis.png)

Le API Enterprise di Adobe CX consentono agli sviluppatori e agli strumenti di codifica basati sull’intelligenza artificiale di accedere direttamente ai dati e ai flussi di lavoro di Adobe. Utilizzale per creare applicazioni personalizzate, automatizzare le integrazioni e incorporare le funzionalità di Adobe nei tuoi sistemi. Le API sono la scelta giusta quando hai bisogno di un controllo programmatico completo sull’integrazione di un sistema o quando crei un’applicazione sopra i dati di Adobe. Per l&#39;accesso conversazionale basato su agenti ai flussi di lavoro di Adobe, vedere [Server MCP](mcp-servers.md).

## API di Adobe CX Enterprise

>[!BEGINTABS]

>[!TAB Adobe Analytics]

Reporting, feed di dati, metriche calcolate e gestione dei segmenti.

[Esplora API](https://developer.adobe.com/analytics-apis/docs/2.0/)

>[!TAB Adobe Commerce]

API REST e GraphQL per catalogo, carrello, ordini, clienti e promozioni.

[Esplora API](https://developer.adobe.com/commerce/webapi/)

>[!TAB Adobe Experience Platform]

Operazioni CRUD per set di dati, schemi, profili, identità, query e segmentazione.

[Esplora API](https://developer.adobe.com/experience-platform-apis/)

>[!TAB Adobe Journey Optimizer]

Orchestrazione del percorso, gestione delle campagne, modelli di contenuto e Offer Decisioning.

[Esplora API](https://developer.adobe.com/journey-optimizer-apis/)

>[!TAB AEM as a Cloud Service]

API per la gestione di contenuti, risorse e flussi di lavoro per Adobe Experience Manager.

[Esplora API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions)

>[!TAB Audience Manager]

Flussi di lavoro di attivazione e gestione dell’audience.

[Esplora API](https://developer.adobe.com/audience-manager/)

>[!TAB SDK client]

SDK per dispositivi mobili, SDK edge e messaggistica in-app.

[Esplora API](https://developer.adobe.com/client-sdks/home/)

>[!TAB Customer Journey Analytics]

Flussi di lavoro per l’accesso ai dati di Analytics, la generazione di rapporti e approfondimenti su CJA.

[Esplora API](https://developer.adobe.com/cja-apis/docs/)

>[!TAB Raccolta dati]

Acquisizione dei dati di Edge Network, raccolta di eventi in tempo reale e distribuzione di dati in streaming.

[Esplora API](https://developer.adobe.com/data-collection-apis/docs/)

>[!TAB Developer Console]

Configurazione del progetto API, autenticazione e gestione delle credenziali.

[Esplora API](https://developer.adobe.com/developer-console/docs/guides/)

>[!TAB Eventi]

Integrazioni guidate da eventi, webhook e trigger di automazione.

[Esplora API](https://developer.adobe.com/events/docs/)

>[!TAB Privacy]

Flussi di lavoro per la privacy, governance dei dati e richieste degli interessati.

[Esplora API](https://experienceleague.adobe.com/it/docs/experience-platform/privacy/home)

>[!TAB Gestione utente]

Gestione degli utenti, amministrazione delle identità e automazione degli account aziendali.

[Esplora API](https://developer.adobe.com/umapi/)

>[!ENDTABS]

## Creare con API

![Connessione IDE alle API Adobe CX Enterprise](../assets/hero-connect-apis.gif)

Gli agenti di codifica come Claude Code, Cursor e OpenAI Codex sono particolarmente adatti per la creazione di API aziendali di Adobe CX. Aggiungi una specifica OpenAPI al progetto affinché l’agente possa individuare endpoint, creare richieste e motivare il comportamento dell’API senza dover ricorrere a cablaggi manuali. Per iniziare, è necessario disporre di due elementi: credenziali autenticate provenienti da Adobe Developer Console e documentazione API aggiunta al progetto.

### Configurare le credenziali API in Adobe Developer Console

Tutti gli accessi alle API di Adobe CX Enterprise sono gestiti tramite [Adobe Developer Console](https://developer.adobe.com/developer-console/docs/guides/). Crea un progetto, aggiungi le API necessarie per l’applicazione e genera le credenziali.

1. Accedi e [crea un progetto](https://developer.adobe.com/developer-console/docs/guides/projects/) in Adobe Developer Console.
2. [Aggiungere l&#39;API](https://developer.adobe.com/developer-console/docs/guides/services/) per l&#39;applicazione Adobe CX Enterprise necessaria.
3. Scegli un tipo di autenticazione [&#128279;](https://developer.adobe.com/developer-console/docs/guides/authentication/). Utilizza **OAuth Server-to-Server** per flussi di lavoro automatizzati o **OAuth Web App** per applicazioni rivolte all&#39;utente.
4. Genera le credenziali. Prendi nota dell’ID client, del segreto client e dell’endpoint token da utilizzare nell’applicazione.

La maggior parte delle API Adobe CX Enterprise richiede licenze per le applicazioni. Se un’API non è disponibile nel progetto Developer Console, contatta il rappresentante Adobe.

### Aggiungere al progetto il contesto API di Adobe

Gli agenti di codifica IA possono individuare e utilizzare in modo affidabile le API di Adobe quando aggiungi al progetto il materiale di riferimento corretto. Questo funziona per qualsiasi API aziendale di Adobe CX che pubblica una specifica OpenAPI.

**1. Trova la specifica API**

Sfoglia le [API Adobe CX Enterprise](#adobe-cx-enterprise-apis) elencate sopra o passa direttamente al [catalogo API Adobe Developer](https://developer.adobe.com/apis).

**2. Scarica la specifica OpenAPI**

Crea una directory `/specs` nel progetto. Scarica il file YAML OpenAPI dalla pagina dei riferimenti API in [developer.adobe.com](https://developer.adobe.com/apis) e salvalo. Aggiungi un `README.md` per registrare l&#39;URL di origine e la data di download.

```
/specs/README.md
/specs/aem-assets.openapi.yaml
```

>[!TIP]
>Un’istantanea archiviata offre all’agente di codifica un comportamento stabile e riproducibile e rende visibili le modifiche API nella cronologia Git.

**3. Genera un indice API**

Incolla questo prompt nell&#39;agente di codifica, sostituendo `<API-SPEC-FILE>` con il tuo nome file:

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and generate /docs/<API-SPEC-FILE>.api.md.

Create a concise API index for AI coding agents. For each operation include: operationId, HTTP method, path, purpose, authentication requirements, required inputs, response shape, common error responses, pagination behavior, asynchronous behavior, and deprecation status.

Do not invent endpoints, parameters, request bodies, response fields, or behavior not present in the OpenAPI specification.
```

**4. Genera istruzioni agente**

```
Read /specs/<API-SPEC-FILE>.openapi.yaml and /docs/<API-SPEC-FILE>.api.md.

Generate AGENTS.md. Instructions should:
- Treat the OpenAPI specification as the source of truth.
- Use the API index as a navigation guide.
- Never invent endpoints, parameters, response fields, or status codes.
- Prefer documented operationIds.
- Avoid deprecated or experimental APIs unless explicitly requested.
- Follow authentication requirements defined in the specification.
- Use the local OpenAPI snapshot for implementation decisions.
```

**5. Verifica**

Chiedi all’agente di codifica di completare un’attività semplice utilizzando solo i file generati:

```
Write a function that takes an AEM asset ID and returns the asset title and description. Use only /specs/aem-assets.openapi.yaml and /docs/aem-assets.api.md.
```

Se l&#39;agente lo completa correttamente senza inventare il comportamento, l&#39;impostazione è completa.

**Struttura di progetto consigliata**

```
project/
├── specs/
│   ├── README.md
│   └── aem-assets.openapi.yaml
├── docs/
│   └── aem-assets.api.md
└── AGENTS.md
```

**Specifiche aggiornate**

Quando Adobe pubblica una nuova versione API: scarica una nuova istantanea in `/specs`, aggiorna la data in `README.md` e rigenera l&#39;indice e `AGENTS.md`.

## API in azione

Le API offrono ai team di sviluppo un controllo programmatico completo per la creazione di applicazioni mirate che automatizzano flussi di lavoro aziendali CX specifici. In queste procedure dettagliate vengono illustrate le integrazioni effettive create in modo completo, dalla configurazione delle credenziali al codice di lavoro che può essere fornito dall&#39;organizzazione.

<!--
CARDS

* https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app
  {title = Invoke AEM APIs from a web app}
  {description = Build a web application that authenticates users and calls AEM OpenAPIs using OAuth to deliver governed, programmatic access.}
  {cta = Try with APIs}
  {image = ../assets/using-api-card.png}

-->
<!-- START CARDS HTML - DO NOT MODIFY BY HAND -->
<div class="columns">
    <div class="column is-half-tablet is-half-desktop is-one-third-widescreen" aria-label="Invoke AEM APIs from a web app">
        <div class="card" style="height: 100%; display: flex; flex-direction: column; height: 100%;">
            <div class="card-image">
                <figure class="image x-is-16by9">
                    <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" title="Richiama le API di AEM da un’app web" target="_blank" rel="referrer">
                        <img class="is-bordered-r-small" src="../assets/using-api-card.png" alt="Richiama le API di AEM da un’app web"
                             style="width: 100%; aspect-ratio: 16 / 9; object-fit: cover; overflow: hidden; display: block; margin: auto;">
                    </a>
                </figure>
            </div>
            <div class="card-content is-padded-small" style="display: flex; flex-direction: column; flex-grow: 1; justify-content: space-between;">
                <div class="top-card-content">
                    <p class="headline is-size-6 has-text-weight-bold">
                        <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" title="Richiama le API di AEM da un’app web">Richiama API AEM da un'app Web</a>
                    </p>
                    <p class="is-size-6">Crea un’applicazione web che autentica gli utenti e chiama le API aperte di AEM utilizzando OAuth per fornire un accesso regolamentato e programmatico.</p>
                </div>
                <a href="https://experienceleague.adobe.com/en/docs/experience-manager-learn/cloud-service/aem-apis/openapis/invoke-api-using-oauth-web-app" target="_blank" rel="referrer" class="spectrum-Button spectrum-Button--outline spectrum-Button--primary spectrum-Button--sizeM" style="align-self: flex-start; margin-top: 1rem;">
                    <span class="spectrum-Button-label has-no-wrap has-text-weight-bold">Prova con le API</span>
                </a>
            </div>
        </div>
    </div>
</div>
<!-- END CARDS HTML - DO NOT MODIFY BY HAND -->
