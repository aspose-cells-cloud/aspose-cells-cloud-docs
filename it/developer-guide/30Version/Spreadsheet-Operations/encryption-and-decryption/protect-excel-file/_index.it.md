---
title: "Proteggi un Workbook Excel con l'API Aspose.Cells Cloud"
second_title: "Documento"
linktitle: "Proteggi un File Excel"
type: docs
url: /it/protect-excel-file/
aliases: [/it/protect-excel-workbooks/, /it/workbook/protect/]
keywords: "Aspose.Cells, protezione Excel, API, REST, SDK"
description: "Scopri come proteggere un workbook Excel tramite l'API REST Aspose.Cells Cloud. Include i passaggi per l'autenticazione, i parametri di query e del corpo della richiesta, la richiesta cURL e campioni di codice SDK per C#, Java, PHP, Ruby, Node.js, Python, Perl e Go."
weight: 30
ArticleTitle: "Proteggi un Workbook Excel usando l'API Aspose.Cells Cloud"
---

Questa API REST **protegge** un workbook Excel, consentendoti di proteggere in modo sicuro un workbook Excel tramite password e opzioni di protezione utilizzando Aspose.Cells Cloud.

## API PostProtectDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">l'autenticazione basata su token JWT</a>.

### Parametri di Query

| Nome Parametro | Tipo   | Descrizione                                                     |
| -------------- | ------ | --------------------------------------------------------------- |
| folder         | string | Cartella contenente il workbook di origine. _(opzionale)_          |
| storageName    | string | Nome della posizione di archiviazione. _(opzionale; default = "Default")_ |

### Parametri del Corpo della Richiesta

| Nome Parametro | Tipo                      | Descrizione                                                   |
| -------------- | ------------------------- | ------------------------------------------------------------- |
| protection     | WorkbookProtectionRequest | Oggetto che definisce le impostazioni di protezione per il workbook. |

#### WorkbookProtectionRequest

| Nome Parametro | Tipo   | Descrizione                                                                                                                                              |
| -------------- | ------ | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ProtectionType | string | Tipo di protezione da applicare. Valori ammessi (indipendenti dalla maiuscola/minuscola): **ALL**, **CONTENTS**, **NONE**, **OBJECTS**, **SCENARIOS**, **STRUCTURE**, **WINDOWS**. |
| Password       | string | Password opzionale da impostare per la protezione.                                                                                                             |

### Risposta

```json
{
  "Status":"OK",
  "Code":200
}
```

**Codici di Stato HTTP**

| Codice | Significato                 | Descrizione                                      |
|--------|-----------------------------|--------------------------------------------------|
| 200    | OK                          | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta Non Validata      | Parametri mancanti o non validi (es. tipo di file non supportato). |
| 401    | Non Autorizzato             | Token JWT non valido o mancante. |
| 413    | Payload Troppo Grande       | Il file caricato supera il limite di dimensione. |
| 500    | Errore Interno del Server   | Errore imprevisto del server. |

## Come utilizzare l'API PostProtectDocument con gli SDK

### Prerequisiti

Prima di chiamare l'API, assicurati di aver completato i seguenti passaggi:

- **Ottenere un token di accesso JWT** seguendo il flusso di autenticazione descritto nella sezione sulla sicurezza.  
- **Caricare il workbook** nella tua archiviazione Aspose Cloud o verificare che esso esista già nella cartella di destinazione.  
- **Conoscere il nome dell'archiviazione** (il valore predefinito è `"Default"` se non specificato) e il nome esatto del file che desideri proteggere.

### Specifica dell'API PostProtectDocument

La <a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">Specifica OpenAPI</a> definisce un'interfaccia di programmazione accessibile pubblicamente e consente di effettuare interazioni REST direttamente da un browser web.

### Esempio: Proteggi un Workbook con cURL

1. Ottieni un token di accesso come descritto in **Prerequisiti / Autenticazione**.  
2. Esegui la richiesta:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   La risposta conterrà un oggetto di stato che conferma che la protezione è andata a buon fine.

### Utilizzo degli SDK Aspose.Cells Cloud

L'utilizzo di un SDK rappresenta il modo più rapido per sviluppare con Aspose.Cells Cloud. Un SDK nasconde i dettagli di basso livello, consentendoti di concentrarti sulla logica di business. Consulta il <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repository GitHub</a> per l'elenco completo degli SDK Aspose.Cells Cloud.

I seguenti esempi di codice mostrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Risposta Completa di Esempio

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```