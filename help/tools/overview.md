---
title: Strumenti agenti
description: Confrontate i server MCP, le competenze dell'agente e le API per i generatori e scegliete lo strumento agentico adatto per i flussi di lavoro Adobe CX Enterprise.
index: false
source-git-commit: 63f5958eaa227ea21fa5b193a2ac76a69fd349cb
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 1%

---


# Strumenti agenti

<!-- last-modified: 2026-05-08 -->

Non tutti gli strumenti agentici rispondono alle stesse esigenze. I server MCP consentono l’accesso immediato e in linguaggio naturale ai dati di Adobe da qualsiasi client di intelligenza artificiale compatibile, senza richiedere codifica. Le abilità dell’agente codificano l’esperienza del dominio Adobe in flussi di lavoro dell’agente ripetibili, in modo che le attività vengano eseguite in modo coerente ogni volta. Le API forniscono agli sviluppatori il controllo programmatico completo per la creazione di applicazioni e integrazioni personalizzate. In questa pagina vengono illustrati i compromessi che consentono di scegliere il punto di partenza più adatto alla propria situazione.

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

## Confrontare gli strumenti di gestione degli agenti

| | Server MCP | Abilità agente | API per builder |
| --- | --- | --- | --- |
| Ideale per | Utenti client AI | Tutti gli utenti | Sviluppatori |
| Richiede la codifica | No | No | Sì |
| Tempo di configurazione | Minutes | Minutes | Da ore a giorni |
| I risultati ottenuti | Accesso ad Adobe dal tuo strumento AI | Workflow guidati e ripetibili | Controllo programmatico completo |
| Client di intelligenza artificiale necessario | Sì | Sì | Facoltativo |

## Non sei sicuro di dove iniziare?

- Per utilizzare l&#39;intelligenza artificiale per interagire con le applicazioni Adobe CX Enterprise (eseguendo azioni, eseguendo query sui dati e consentendo all&#39;intelligenza artificiale di scoprire cosa fare dopo attraverso una conversazione naturale), i [server MCP](mcp-servers.md) sono il punto di partenza più flessibile.
- Per fare in modo che gli agenti seguano in modo coerente i flussi di lavoro nativi di Adobe senza eseguire improvvisazioni, [Le abilità dell&#39;agente](agent-skills.md) codificano tale esperienza del dominio in istruzioni riutilizzabili.
- Per creare un&#39;applicazione mirata che semplifichi o automatizzi un flusso di lavoro Adobe specifico per gli utenti, le [API per i generatori](apis.md) ti offrono un controllo diretto e programmabile su ciò che accade.

>[!BEGINTABS]

>[!TAB Server MCP]

Considera i server MCP come un collegamento in tempo reale tra lo strumento di intelligenza artificiale e Adobe. Connettiti una volta e la tua intelligenza artificiale può eseguire query sulle campagne, richiamare tipi di pubblico, controllare lo stato del percorso e altro ancora. Il tutto in un linguaggio semplice, senza bisogno di codice.

**Utilizzare i server MCP quando:**

- Desideri che i dati di Adobe all’interno dello strumento di intelligenza artificiale già utilizzato
- Stai effettuando analisi esplorative o recupero di dati ad hoc
- Desideri risultati veloci, senza far ruotare un progetto

**Prova:** Chiedi a Claude di riepilogare i tuoi percorsi attivi. Richiama le dimensioni del pubblico di Real-Time CDP da ChatGPT. Rivedi le metriche della campagna CJA senza aprire una dashboard.

[Esplora server MCP](mcp-servers.md)

>[!TAB Abilità agente]

Le abilità dell’agente sono competenze sul dominio di Adobe, codificate come istruzioni che l’agente può seguire. Invece di sperare che il tuo agente trovi i passaggi giusti, un&#39;abilità gli dice esattamente cosa fare. Affidabile, ripetibile e già ottimizzato per i flussi di lavoro Adobe.

**Utilizza le abilità dell&#39;agente quando:**

- Si desidera eseguire sempre la stessa operazione nello stesso modo
- Esecuzione di flussi di lavoro di produzione di contenuti o supporti ripetibili
- Vuoi un agente che conosca Adobe senza dover fornire spiegazioni

**Prova:** modifica in batch un set di foto per renderle coerenti. Genera varianti social compatibili con la piattaforma da una risorsa di origine. Progetta da un modello Adobe Express in pochi prompt.

[Esplora abilità agente](agent-skills.md)

>[!TAB API per i generatori]

Le API sono gli elementi costitutivi. Offrono agli sviluppatori un accesso diretto e programmatico ai dati e alle operazioni di Adobe, utilizzando le stesse API che alimentano i prodotti di Adobe. Utilizzali per creare qualcosa che funzioni secondo la tua pianificazione, le tue condizioni, il tuo stack.

**Utilizza le API quando:**

- Creazione di un&#39;applicazione o di un dashboard personalizzato
- È necessario integrare i dati di Adobe in un altro sistema
- Stai usando Claude Code o Cursor per generare un&#39;applicazione completa
- È necessario un controllo completo di creazione, aggiornamento o eliminazione

**Prova:** crea un dashboard campagna personalizzato. Automatizzare una pipeline di dati. Genera un&#39;applicazione con Claude Code che legge e scrive in Adobe Experience Platform.

[Esplora le API per i generatori](apis.md)

>[!ENDTABS]

## Utilizzarli insieme

I server MCP, le competenze dell’agente e le API sono complementari. Molti flussi di lavoro combinano tutti e tre:

- Un&#39;abilità agente definisce il flusso di lavoro e guida l&#39;agente
- I server MCP concedono all’agente l’accesso in lettura ai dati di Adobe mid-workflow
- Le API gestiscono azioni che richiedono scritture dirette del sistema o logica di applicazione personalizzata
