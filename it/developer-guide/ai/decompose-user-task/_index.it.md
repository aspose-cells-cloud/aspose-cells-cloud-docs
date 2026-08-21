---
---
title: "Aspose.Cells Cloud AI – API di decomposizione dei compiti utente (v4.0) | Pianificazione dei compiti SMART"
second_title: "Documento"
ArticleTitle: "Come convertire obiettivi utente in piani di azione sequenziali con l'API di decomposizione dei compiti di Aspose.Cells Cloud AI"
linktitle: "Decomponi compito utente"
type: docs
url: /decompose-user-task/
keywords: "Aspose.Cells AI, API di decomposizione dei compiti, pianificazione dei compiti SMART, importazione Redmine, automazione di progetto"
description: "Trasforma obiettivi liberi in liste di compiti SMART, con stime temporali in ore, grazie ad Aspose.Cells Cloud AI. Ottieni output CSV/XLSX pronti per Redmine, Jira o Azure DevOps con una singola richiesta PUT."
weight: 100
---

L'endpoint **DecomposeUserTask** fornisce un endpoint REST per trasformare una descrizione di un compito in formato libero in un piano d’azione dettagliato e sequenziale conforme ai criteri SMART. Assegna automaticamente stime temporali in ore, formatta l’output per l’importazione compatibile con Redmine e crea nodi di traguardo di progetto. Fornendo soltanto l’elenco grezzo dei compiti e, opzionalmente, le stime temporali, l’API restituisce un file pronto all’uso (CSV, XLSX, ecc.) che può essere importato direttamente in strumenti di project management, automatizzando la scomposizione dei compiti e riducendo lo sforzo manuale.

## **API di decomposizione dei compiti utente**

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### **Parametri della richiesta:**

| Nome del parametro | Tipo   | Posizione | Obbligatorio/Opzionale | Descrizione                                                                                                                                                                                                                              |
| :----------------- | :----- | :-------- | :--------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription    | string | Corpo     | Obbligatorio           | Una descrizione in testo semplice dell’obiettivo complessivo dell’utente. Il servizio analizza la descrizione e genera singoli compiti. Esempio: “Lanciare una campagna di marketing per il terzo trimestre, inclusa la creazione di contenuti, invio di email e inserzioni sui social media.” |

### **Risposta**

Risposta riuscita (200 OK)  
Content‑Type: `application/octet-stream` (flusso binario di file)

Intestazioni:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <dimensione in byte>`

La stessa struttura viene utilizzata per i formati XLSX/ODS, con le colonne posizionate nel primo foglio di lavoro.

**Codici di stato HTTP**

| Codice | Significato             | Descrizione                                                        |
| ------ | ----------------------- | ------------------------------------------------------------------ |
| 200    | OK                      | Filtro applicato correttamente; la risposta contiene i dettagli dell’operazione. |
| 400    | Richiesta non valida    | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non autorizzato         | Token JWT non valido o mancante.                                   |
| 413    | Payload troppo grande   | Il file caricato supera il limite di dimensione.                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                     |

**Esempio di risposta di errore (400 Bad Request)**

```json
{
  "code": "InvalidParameter",
  "message": "Il campo 'TaskDescription' è obbligatorio e non può essere vuoto."
}
```

**Esempio di corpo della richiesta (JSON)**

```json
{
  "TaskDescription": "Sviluppare un'API web per una funzionalità di suddivisione dei compiti nel sistema esistente."
}
```

**Esempio di risposta**  
L’API restituisce un flusso binario contenente il file generato. Per visualizzare le prime righe di una risposta in formato CSV, decodificare il flusso e visualizzare la riga di intestazione, ad esempio:

```
ID,Oggetto,Responsabile,Durata stimata,Descrizione
1	Rilevamento dei requisiti per l'API di suddivisione dei compiti	Analista aziendale	8	Raccogliere i requisiti funzionali e non funzionali, le user story e i criteri di accettazione per il nuovo endpoint di suddivisione dei compiti.
2	Specifica dell'API (OpenAPI)	Analista aziendale	6	Definire il contratto OpenAPI per POST /tasks/split, inclusi schema di richiesta, formati di risposta, codici di errore e requisiti di sicurezza.
3	Algoritmo di suddivisione e progettazione del modello dati	Architetto di soluzione	5	Progettare l’algoritmo principale che divide un compito padre in sotto-compiti e estendere il modello dati (tabelle DB / entità) per memorizzare la gerarchia e i metadati.
4	Revisione dell'integrazione architettonica	Architetto di soluzione	4	Analizzare l’impatto sui servizi esistenti, sui flussi di eventi e sulle migrazioni del database; produrre il piano di integrazione.
...
```

## Dove utilizzare l’API di decomposizione dei compiti utente?

- **Avvio di progetto**: Convertire un breve cenno generale del progetto in un elenco di compiti compatibile con Redmine, con stime temporali, abilitando la pianificazione immediata degli sprint.
- **Automazione marketing**: Suddividere gli obiettivi della campagna in passi eseguibili, esportare in CSV e importare negli strumenti di gestione dei compiti per la coordinazione tra team diversi.
- **Assegnazione delle risorse**: Generare stime in ore per ogni sotto-compito, consentendo ai manager di bilanciare il carico di lavoro tra i membri del team prima dell’inizio del progetto.
- **Monitoraggio dei traguardi**: Creare automaticamente nodi di traguardo che possono essere sincronizzati con strumenti di diagramma di Gantt, garantendo che ogni fase abbia un risultato tangibile.

## Perché utilizzare l’API di decomposizione dei compiti utente?

- **Output conforme a SMART** garantisce che ogni compito generato soddisfi i criteri Specifico, Misurabile, Realizzabile, Rilevante e Temporizzato.
- **Stima temporale in ore integrata** elimina la necessità di calcoli manuali e migliora la precisione delle previsioni.
- **Formati di file pronti all’importazione** (CSV, XLSX, ecc.) facilitano l’integrazione con Redmine, Jira, Azure DevOps e altre piattaforme di project management.
- **Automazione in una singola richiesta** consente la scomposizione dei compiti tramite una singola richiesta, accelerando l’avvio del progetto e riducendo lo sforzo manuale.

## Come utilizzare l’API di decomposizione dei compiti utente con gli SDK

### Specifica dell’API di decomposizione dei compiti utente

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">Specifica dell’API di decomposizione dei compiti utente</a> fornisce un'interfaccia di programmazione pubblicamente accessibile per eseguire interazioni REST direttamente da un browser web.

## SDK per l’API Excel

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell’SDK è il modo più rapido per sviluppare, poiché astrae i dettagli a basso livello e consente di chiamare l’endpoint DecomposeUserTask con codice conciso.  
Consultare il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per un elenco completo degli SDK di Aspose.Cells Cloud.  
I seguenti esempi di codice mostrano come interagire con i servizi web di Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---