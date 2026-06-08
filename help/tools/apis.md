---
title: API per builder
description: Creare applicazioni e integrazioni personalizzate utilizzando le API Adobe CX Enterprise.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 3%

---


# API per builder

<!-- last-modified: 2026-06-02 -->

![API Adobe CX Enterprise](../assets/hero-apis.png)

Le API Enterprise di Adobe CX consentono agli sviluppatori e agli strumenti di codifica basati sull’intelligenza artificiale di accedere direttamente ai dati e ai flussi di lavoro di Adobe. Utilizzale per creare applicazioni personalizzate, automatizzare le integrazioni e incorporare le funzionalità di Adobe nei tuoi sistemi. Le API sono la scelta giusta quando hai bisogno di un controllo programmatico completo sull’integrazione di un sistema o quando crei un’applicazione sopra i dati di Adobe. Per l&#39;accesso conversazionale basato su agenti ai flussi di lavoro di Adobe, vedere [Server MCP](mcp-servers.md).

## API di Adobe CX Enterprise

Le API Adobe CX Enterprise espongono i dati e le operazioni principali che alimentano prodotti come Adobe Experience Platform, Journey Optimizer e Customer Journey Analytics. Ogni API segue una progettazione API-first, che fornisce agli sviluppatori e agli strumenti di codifica assistiti da AI un accesso diretto e programmabile alle stesse funzionalità utilizzate internamente da Adobe. Utilizzale per creare applicazioni personalizzate, automatizzare i flussi di lavoro e integrare i dati di Adobe nei tuoi sistemi.

<!--
CARDS

* https://developer.adobe.com/audience-manager/
  {title = Audience Manager}
  {description = Audience management and activation workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aam-card.png}

* https://developer.adobe.com/client-sdks/home/
  {title = Client SDKs}
  {description = Mobile SDKs, edge SDKs, and in-app messaging.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/cja-apis/docs/
  {title = Customer Journey Analytics}
  {description = Analytics data access, reporting, and CJA insights workflows.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cja-card.png}

* https://developer.adobe.com/data-collection-apis/docs/
  {title = Data Collection}
  {description = Edge Network data ingestion, real-time event collection, and streaming data delivery.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/developer-console/docs/guides/
  {title = Developer Console}
  {description = API project setup, authentication, and credential management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://developer.adobe.com/events/docs/
  {title = Events}
  {description = Event-driven integrations, webhooks, and automation triggers.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}

* https://experienceleague.adobe.com/it/docs/experience-platform/privacy/home
  {title = Privacy}
  {description = Privacy workflows, data governance, and data subject requests.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/experience-platform-apis/
  {title = Adobe Experience Platform}
  {description = CRUD operations for datasets, schemas, profiles, identities, queries, and segmentation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aep-card.png}

* https://developer.adobe.com/journey-optimizer-apis/
  {title = Adobe Journey Optimizer}
  {description = Journey orchestration, campaign management, content templates, and offer decisioning.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-ajo-card.png}

* https://developer.adobe.com/analytics-apis/docs/2.0/
  {title = Adobe Analytics}
  {description = Reporting, data feeds, calculated metrics, and segment management.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-analytics-card.png}

* https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/developing/apis-and-extensions
  {title = AEM as a Cloud Service}
  {description = Content, asset, and workflow management APIs for Adobe Experience Manager.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-aem-card.png}

* https://developer.adobe.com/commerce/webapi/
  {title = Adobe Commerce}
  {description = REST and GraphQL APIs for catalog, cart, orders, customers, and promotions.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-commerce-card.png}

* https://developer.adobe.com/umapi/
  {title = User Management}
  {description = User management, identity administration, and enterprise account automation.}
  {cta = Explore API}
  {target = _blank}
  {image = ../assets/apis-cxenterprise-card.png}
-->

## API per Builder e server MCP

Utilizza le API quando hai bisogno di un controllo completo sull’integrazione del sistema o quando stai creando un’applicazione personalizzata. Utilizza i server MCP quando desideri che un agente di intelligenza artificiale funzioni direttamente con i flussi di lavoro di Adobe.

| | API | Server MCP |
| --- | --- | --- |
| Integrazione diretta del sistema | Sì | A volte |
| Orchestrazione intuitiva | Limitato | Sì |
| Accesso ai dati non elaborati | Sì | Di solito astratto |
| Sviluppo di applicazioni personalizzate | Caso d’uso principale | Secondario |
| Flussi di lavoro basati sull’intelligenza artificiale | Supportato | Caso d’uso principale |

## Guida introduttiva alle API per i generatori

![Connessione IDE alle API Adobe CX Enterprise](../assets/hero-connect-apis.gif)

Prima di poter generare le API di Adobe CX Enterprise è necessario disporre di due elementi: credenziali autenticate provenienti da Adobe Developer Console e documentazione API aggiunta al progetto, in modo che l’agente di codifica possa funzionare con le API di Adobe in modo affidabile.

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
