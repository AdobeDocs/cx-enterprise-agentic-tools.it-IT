---
title: Implementare in AEM as a Cloud Service con sicurezza
description: Controlla lo stato dell’ambiente, controlla la cronologia delle pipeline e attiva o gestisci le distribuzioni senza uscire dal client di intelligenza artificiale.
last-substantial-update: 2026-06-10T00:00:00Z
index: false
source-git-commit: 8735d40a6bee547608a3c0efea7f942b813f2d41
workflow-type: tm+mt
source-wordcount: '938'
ht-degree: 2%

---


# Implementare in AEM as a Cloud Service con sicurezza

<!-- last-modified: 2026-05-21 -->

>[!VIDEO](https://video.tv.adobe.com/v/3480340/?learn=on&enablevpops)

L’affidabilità dell’implementazione deriva dalla consapevolezza che l’ambiente è sano prima di inviare messaggi push. In questa procedura dettagliata viene illustrato come verificare lo stato dell’ambiente AEM, esaminare la cronologia delle pipeline e attivare le distribuzioni da un client di intelligenza artificiale utilizzando il server MCP di AEM Cloud Manager, in modo che i team possano spostarsi rapidamente senza perdere visibilità.

| Dettagli scenario | |
| --- | --- |
| Applicazioni aziendali CX | [Adobe Experience Manager Cloud Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/implementing/using-cloud-manager/introduction-to-cloud-manager) |
| Strumenti agenti | [Server MCP AEM Cloud Manager](https://experienceleague.adobe.com/it/docs/experience-manager-learn/cloud-service/ai/mcp-servers/cloud-manager) |
| Pubblico | Sviluppatori, DevOps, team operativi |
| Prerequisito | Client di intelligenza artificiale compatibile con MCP, accesso AEM Cloud Manager |

Ogni passaggio mostra un prompt rappresentativo e un esempio di risposta di IA. Segue una sezione **Ulteriori richieste per provare** per ulteriori informazioni nella stessa sessione.

## Prima di iniziare

>[!BEGINTABS]

>[!TAB Codice Claude]

Passa prima alla directory del progetto, quindi aggiungi il server Cloud Manager MCP utilizzando CLI:

```bash
claude mcp add --transport http adobe-cloud-manager https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Oppure aggiungerlo manualmente a `.mcp.json` nella directory principale del progetto:

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Riavvia Claude Code. Gli strumenti di Cloud Manager sono disponibili nella sessione successiva.

Configurazione completa: [documentazione MCP codice Claude](https://docs.anthropic.com/en/docs/claude-code/mcp)

>[!TAB Cursore]

Aggiungi il server Cloud Manager MCP a `~/.cursor/mcp.json` (globale) o `.cursor/mcp.json` nella directory principale del progetto:

```json
{
  "mcpServers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Apri **Impostazioni > MCP**, seleziona **Connetti** accanto al server e accedi con il tuo Adobe ID.

Configurazione completa: [Documentazione MCP cursore](https://cursor.com/docs/mcp)

>[!TAB Copilota GitHub]

Aggiungere il server Cloud Manager MCP a `.vscode/mcp.json` nella directory principale del progetto:

```json
{
  "servers": {
    "adobe-cloud-manager": {
      "type": "http",
      "url": "https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager"
    }
  }
}
```

Nota: il codice VS utilizza `"servers"` come chiave di livello principale, non `"mcpServers"`.

Apri il pannello **GitHub Copilot Chat**, passa alla **modalità agente** e seleziona **Connetti** accanto al server. Gli strumenti MCP sono disponibili solo in modalità agente.

Configurazione completa: [documentazione dei server MCP di codice VS](https://code.visualstudio.com/docs/copilot/customization/mcp-servers)

>[!TAB Altri client di IA]

Utilizzare un altro ambiente compatibile con MCP? Connettersi al server Cloud Manager MCP utilizzando questo endpoint:

```
https://mcp.adobeaemcloud.com/adobe/mcp/cloudmanager
```

Istruzioni di installazione complete per tutti i client supportati: [Connetti al client di intelligenza artificiale](../tools/mcp-servers.md)

>[!ENDTABS]

>[!NOTE]
>
>Quando richiesto, accedi con il tuo Adobe ID e seleziona l’organizzazione IMS collegata al tuo programma AEM as a Cloud Service. Le autorizzazioni vengono applicate a livello di Cloud Manager. Il client di intelligenza artificiale può eseguire solo operazioni per le quali il tuo account è autorizzato.
>
>Alla prima connessione, il client di intelligenza artificiale potrebbe chiederti di confermare l’organizzazione o il programma AEM. Una volta impostato tale contesto, il server MCP lo utilizza per il resto della sessione.
>
>Alcuni strumenti richiedono la tua approvazione prima di essere eseguiti. Esamina l’azione proposta e approva o rifiuta. Non viene intrapresa alcuna azione senza la tua conferma.

## Passaggio 1: verificare lo stato dell’ambiente

Prima di avviare una versione, verifica che gli ambienti siano integri e che non sia in esecuzione nulla.

```
What is the status of the production environment?
```

+++Vedi una risposta di esempio

![Client IA che mostra lo stato dell&#39;ambiente di produzione da Cloud Manager](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step1-01-ai.png)

+++


## Passaggio 2: rivedere le esecuzioni della pipeline

Rivedi la cronologia della pipeline recente per comprendere i pattern di distribuzione e gli errori di catch prima che blocchino la versione successiva.

```
Show me the last five pipeline runs for the production pipeline.
```

+++Vedi una risposta di esempio

![Il client di IA visualizza le ultime cinque esecuzioni della pipeline per la pipeline di produzione](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step2-01-ai.png)

+++


## Passaggio 3: attivare una pipeline

Avvia l’esecuzione di una pipeline direttamente dal client di intelligenza artificiale. Il server conferma l&#39;ambiente di destinazione e richiede l&#39;approvazione prima di iniziare.

```
Run the Fullstack pipeline against dev environment of WKND sandbox program.
```

+++Vedi una risposta di esempio

![Il client AI mostra la conferma del trigger della pipeline e l&#39;interfaccia utente di Cloud Manager che riflette la pipeline in esecuzione](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step3.gif)

+++


>[!CAUTION]
>
>Il client di intelligenza artificiale ti chiederà di confermare il nome della pipeline prima di attivare un’esecuzione. Immetti il nome esatto della pipeline per continuare. Rivedi attentamente l’ambiente di destinazione prima della conferma, in particolare per le pipeline che vengono distribuite in produzione.

## Passaggio 4: verificare lo stato della pipeline

Dopo aver attivato un’esecuzione, chiedi al client di intelligenza artificiale un aggiornamento dello stato senza passare all’interfaccia di Cloud Manager.

```
What is the status of the triggered pipeline?
```

+++Vedi una risposta di esempio

![Il client AI mostra lo stato dell&#39;esecuzione della pipeline attivata](../assets/use-cases/aem-cloud-manager-mcp/aem-cloud-manager-mcp-step4-01-ai.png)

+++


## Risultati ottenuti

Hai utilizzato il server MCP di AEM Cloud Manager per verificare lo stato dell’ambiente, esaminare la cronologia della pipeline, attivare una distribuzione e verificarne lo stato, senza aprire l’interfaccia di Cloud Manager. Combinando visibilità dell’ambiente e controllo dell’implementazione in un’unica sessione di intelligenza artificiale, i team di sviluppo e operativi possono rispondere più rapidamente ai problemi e mantenere il flusso di lavoro all’interno degli strumenti già utilizzati.

## Più risultati da ottenere

Il server MCP di Cloud Manager gestisce molto di più di quanto descritto nella procedura dettagliata precedente. Espandi uno scenario qui sotto per visualizzare i prompt che puoi provare nella stessa sessione.

+++Rilevare i problemi prima dell’uscita di una versione

Le distribuzioni spesso non riescono per motivi visibili prima dell’esecuzione della pipeline. Queste richieste consentono di confermare lo stato dell’ambiente, verificare la presenza di esecuzioni in conflitto e verificare l’allineamento della versione in tutti gli ambienti prima di eseguire il commit a una versione.

**Richieste**

```
We're about to kick off a production release. Give me a full status check on all environments first.
```

```
Is there anything currently running in the staging pipeline? I don't want to queue on top of an active run.
```

```
Before I promote main branch to production, confirm main was deployed to Dev and all environments are on the same AEM version.
```

```
What repositories are connected to the WKND program?
```

+++

+++Correggere un&#39;implementazione già in esecuzione

Un trigger accidentale o un gate di approvazione bloccato può verificarsi a catena in una pipeline bloccata o in una distribuzione indesiderata. Queste richieste consentono di annullare o far avanzare una pipeline in esecuzione senza passare all’interfaccia di Cloud Manager.

**Richieste**

```
The staging pipeline kicked off by mistake. Cancel it before it deploys.
```

```
The release pipeline is waiting at the approval gate. Advance it to continue the deployment.
```

+++

+++Comprendere i dati della registrazione della distribuzione

Sapere quando le cose sono andate a buon fine, quanto tempo vengono eseguite le pipeline e se i pattern stanno cambiando ti aiuta a pianificare i rilasci e a rallentare il degrado prima che diventi un incidente. Utilizza questi prompt per richiamare la cronologia su richiesta.

**Richieste**

```
What is the status of the last production pipeline execution? If it failed, explain why.
```

```
When was the last successful deployment to the staging environment?
```

```
Our pipeline times are creeping up. What's the longest run we've had in the last 30 days?
```

+++

+++Riportare in pista una build interrotta

Quando una pipeline non riesce, il percorso più veloce per la risoluzione consiste nel capire esattamente dove si è rotta e perché. Questi prompt evidenziano i dettagli degli errori, la cronologia delle modifiche e i problemi del gate di qualità, in modo che il team possa diagnosticare e risolvere i problemi senza dover scorrere manualmente i registri.

**Richieste**

```
We're seeing a regression on the live site. What changed in production over the last week?
```

```
Which pipelines have failed in the last 7 days, and at what stage did they fail?
```

```
The last pipeline failed at the code quality step. What specific issues need to be fixed before I can retry?
```

```
Pull the step logs for the last failed run. I need to see exactly what the quality gate flagged.
```

+++


## Ulteriori informazioni

| Risorsa | Cosa troverai |
| --- | --- |
| [Documentazione su AEM as a Cloud Service](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service){target="_blank"} | Documentazione completa dell’applicazione AEM |
