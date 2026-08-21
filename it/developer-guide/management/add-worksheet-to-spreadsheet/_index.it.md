---
title: "Aspose.Cells Cloud Excel Add Worksheet Web API - Inserisci nuovi fogli con controllo di tipo e posizione"
second_title: "Documento"
ArticleTitle: "Come aggiungere fogli di lavoro a Excel – Inserire nuovi fogli in posizioni specifiche"
linktitle: "Aggiungi foglio di lavoro al foglio di calcolo"
type: docs
url: /add-worksheet-to-spreadsheet/
keywords: "excel, aggiungi foglio di lavoro, aspose cells api, foglio di calcolo, cloud api, tipo di foglio, posizione del foglio"
description: "Scopri come aggiungere programmaticamente un nuovo foglio di lavoro, un foglio grafico o un foglio macro a un libro Excel utilizzando l'API Aspose.Cells Cloud. Controlla il tipo di foglio, il nome e la posizione di inserimento con una singola chiamata REST."
weight: 100
---

Aggiungi programmaticamente fogli di lavoro ai file Excel con pieno controllo sul tipo e sulla posizione del foglio. Inserisci fogli di lavoro standard, fogli grafici o fogli macro in qualsiasi posizione all'interno del libro. Questa operazione RESTful consente la gestione e l'organizzazione automatizzate dei libri Excel.

**Prerequisiti**

- Un account Aspose.Cells Cloud attivo con un token di accesso JWT valido.
- Un nome di archiviazione cloud configurato (ad esempio `CompanyOneDrive`) in cui verrà salvato il libro.
- Il libro di destinazione deve essere accessibile nell'archiviazione specificata e, se protetto, deve essere fornita la password corretta.

| **Tipo di foglio**       | Descrizione                                          |
| :----------------------- | :--------------------------------------------------- |
| **VB**                   | Modulo Visual Basic                                  |
| **Worksheet**            | Foglio di lavoro normale                             |
| **Chart**                | Foglio grafico                                       |
| **BIFF4Macro**           | Foglio macro BIFF4                                   |
| **InternationalMacro**   | Foglio macro internazionale                          |
| **Other**                | Tipo di foglio personalizzato o meno comune non elencato sopra |
| **Dialog**               | Foglio di dialogo                                    |

## **Add Worksheet to Spreadsheet API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

### Parametri della richiesta

| Nome parametro     | Tipo    | Posizione | Descrizione                                                                                                                                                                                          |
| :----------------- | :------ | :-------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File    | FormData  | **Obbligatorio.** Il libro Excel (.xlsx, .xls, ecc.) a cui verrà aggiunto un nuovo foglio di lavoro.                                                                                                         |
| **sheetType**      | String  | Query     | **Opzionale.** Il tipo di foglio da creare. I valori accettabili sono `worksheet` (valore predefinito), `chartsheet`, `macrosheet`, `vbmodule` e `dialog`.                                                        |
| **position**       | Integer | Query     | **Opzionale.** Indice in base zero in corrispondenza del quale inserire il nuovo foglio. `0` inserisce prima del primo foglio; `2` inserisce come terzo foglio. Tralasciare per aggiungere il foglio alla fine.                                       |
| **sheetName**      | String  | Query     | **Opzionale.** Nome del nuovo foglio di lavoro. Deve essere univoco all'interno del libro. Se omesso, viene generato un nome predefinito come "SheetX".                                                              |
| **outPath**        | String  | Query     | **Opzionale.** Directory di destinazione nell'archiviazione cloud in cui verrà salvato il libro modificato. Se `null` o omesso, il libro viene salvato nella stessa posizione del file di origine o in un percorso predefinito. |
| **outStorageName** | String  | Query     | **Obbligatorio.** Identificatore dell'archiviazione cloud configurata (ad esempio `CompanyOneDrive`) in cui deve essere scritto il file di output.                                                                          |
| **region**         | String  | Query     | **Opzionale.** Impostazione locale (ad esempio `it-IT`) che può influenzare la formattazione e le regole regionali nel nuovo foglio di lavoro.                                                                                     |
| **password**       | String  | Query     | **Opzionale.** Password per decrittografare e modificare un libro protetto da password. Omettere se il file non è crittografato.                                                                                       |

### Risposta

In caso di esito positivo, l'API restituisce **HTTP 200 OK** (o **201 Created** quando viene generato un nuovo file) insieme al libro aggiornato.

```json
{
  "Name": "ResponseFile",
  "DataType": {
    "Identifier": "File",
    "Reference": "Stream"
  }
}
```

**Codici di stato HTTP**

| Codice | Significato           | Descrizione                                                       |
| ------ | --------------------- | ----------------------------------------------------------------- |
| 200    | OK                    | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida  | Parametri mancanti o non validi (ad esempio, tipo di file non supportato).      |
| 401    | Non autorizzato       | Token JWT non valido o mancante.                                     |
| 413    | Payload troppo grande | Il file caricato supera il limite di dimensione.                                 |
| 500    | Errore interno del server | Errore imprevisto del server.                                          |

## Dove dovremmo utilizzare l'API Add Worksheet to Spreadsheet?

- **Generazione automatizzata di report** – Creare e inserire dinamicamente fogli mensili (ad esempio `2024-05`) durante la generazione di prospetti finanziari.
- **Inizializzazione batch di modelli** – Aggiungere un foglio di analisi dedicato per ogni nuovo cliente o progetto durante la generazione in blocco di preventivi o proposte commerciali.
- **Espansione dinamica di dashboard** – Inserire nuovi fogli grafici in tempo reale man mano che diventano disponibili nuove dimensioni dei dati.
- **Conformità e archiviazione per audit** – Aggiungere automaticamente fogli di raccolta prove durante gli audit annuali, mantenendo isolati ciascun punto di ispezione.
- Per rimuovere un foglio, vedere l'operazione **[Elimina foglio di lavoro](/delete-worksheet/)**.
- Per spostare un foglio, vedere l'operazione **[Sposta foglio di lavoro](/move-worksheet/)**.

## Perché dovresti utilizzare l'API Add Worksheet to Spreadsheet?

- **Facile da usare per sviluppatori** – Aspose.Cells Cloud fornisce SDK per diversi linguaggi, riducendo lo sforzo di sviluppo e offrendo una documentazione approfondita.
- **Riduzione dei costi di manodopera** – Elimina la necessità di creare manualmente fogli di lavoro e svolgere compiti ripetitivi di copia-incolla.
- **Pay-per-use** – Si paga solo per le chiamate API effettivamente effettuate.
- **Nessuna manutenzione** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l'API Add Worksheet to Spreadsheet con gli SDK

### Specifica dell'API Add Worksheet to Spreadsheet

La [Specifiche dell'API Add Worksheet to Spreadsheet](https://reference.aspose.cloud/cells/#/ManagementController/AddWorksheetToSpreadsheet) definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/add/worksheet?worksheetName=Sheet1" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json" \
     -F "Spreadsheet=@/path/to/Book1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (codificato in Base64)",
  "contentType": "tipo MIME",
  "fileDownloadName": "nome file opzionale"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizzare gli SDK Aspose.Cells Cloud

L'utilizzo di un SDK astrae i dettagli di basso livello, consentendo di aggiungere un foglio di lavoro con un codice minimo. Consulta l'elenco completo degli SDK nel [repository GitHub](https://github.com/aspose-cells-cloud).

Gli esempi di codice seguenti mostrano come chiamare il servizio con vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_AddWorksheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_AddWorksheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_AddWorksheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_AddWorksheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_AddWorksheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_AddWorksheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_AddWorksheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_AddWorksheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}