---
title: "Aspose.Cells Cloud – Scambia colonne, righe e intervalli (v4.0)"
second_title: "Documento"
ArticleTitle: "Scambia/Interscambia dati tra colonne, righe e celle in Excel"
linktitle: "Scambia intervallo"
type: docs
url: /it/swap-range/
keywords: "Aspose Cells, API Excel, Scambia intervallo, foglio di calcolo cloud"
description: "Scambia colonne, righe o intervalli in file Excel tramite l'API Aspose.Cells Cloud. Preserva formattazione, formule e riferimenti alle celle in una singola richiesta."
weight: 100
---

Scambia automaticamente dati tra due qualsiasi colonne, righe, intervalli o celle nei file Excel utilizzando l'API Aspose.Cells Cloud. L'API Scambia intervallo consente di scambiare dati con precisione, preservando tutta la formattazione, le formule e i riferimenti alle celle. Supporta la riorganizzazione complessa dei dati, l'elaborazione in batch e l'integrazione fluida con il cloud per flussi di lavoro aziendali.

## **API Scambia intervallo**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parametri della richiesta**

| Nome parametro     | Tipo   | Posizione | Descrizione                                                                                                                                   |
| ------------------ | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | File   | FormData  | **Obbligatorio.** File del foglio di calcolo Excel di origine (`.xlsx`, `.xls`).                                                               |
| **worksheet1**     | String | Query     | **Obbligatorio.** Nome del foglio di calcolo contenente la prima area di dati.                                                                |
| **range1**         | String | Query     | **Obbligatorio.** Intervallo di celle (ad esempio, `A1:D10`) in `worksheet1` da scambiare.                                                     |
| **worksheet2**     | String | Query     | **Obbligatorio.** Nome del foglio di calcolo contenente la seconda area di dati (può essere lo stesso di `worksheet1`).                       |
| **range2**         | String | Query     | **Obbligatorio.** Intervallo di celle (ad esempio, `F1:I10`) in `worksheet2` da scambiare. **Importante:** `range1` e `range2` devono avere dimensioni identiche. |
| **outPath**        | String | Query     | **Facoltativo.** Cartella nello storage cloud in cui verrà salvato il foglio di calcolo modificato.                                           |
| **outStorageName** | String | Query     | **Obbligatorio.** Nome del servizio di storage cloud configurato (ad esempio, `MyCompanyStorage`).                                            |
| **region**         | String | Query     | **Facoltativo.** Impostazione delle impostazioni locali (ad esempio, `en-US`, `ja-JP`) che potrebbero influenzare la formattazione.            |
| **password**       | String | Query     | **Facoltativo.** Password per decrittografare un foglio di calcolo protetto. Omettere se non crittografato.                                   |

**Esempio di richiesta (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **Risposta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Note:**  
- L'API restituisce il foglio di calcolo modificato come flusso di file. Se `outPath` è specificato, il file viene salvato anche nella posizione specificata nello storage cloud.  
- Intervalli con dimensioni non corrispondenti genereranno un errore **400 Bad Request**.

### Codici di errore

| Codice               | Descrizione                                                        |
| -------------------- | ------------------------------------------------------------------ |
| **400 Bad Request**  | URI della richiesta non valido o dimensioni degli intervalli non corrispondenti. |
| **401 Unauthorized** | Token di accesso non valido o scaduto; client-id o secret errati. |
| **404 Not Found**    | Il file del foglio di calcolo specificato non può essere accessibile. |
| **500 Server Error** | Si è verificato un errore interno durante l'elaborazione del foglio di calcolo. |

## Dove dovremmo utilizzare l'API Scambia intervallo?

- **Ristrutturazione di modelli finanziari** – Riorganizza blocchi di dati (ad esempio, sposta la previsione del Q3 nel Q4) preservando formule e formattazione condizionale.
- **Pipeline dei dati e processi ETL** – Scambia intervalli di dati grezzi con intervalli puliti in un foglio di lavoro di staging prima della generazione finale.
- **Correzione errori e recupero dati** – Correggi rapidamente dati spostati in modo errato senza copiare e incollare manualmente.

## Perché utilizzare l'API Scambia intervallo?

- **Facile da usare per sviluppatori** – Sono disponibili SDK per diversi linguaggi, riducendo lo sforzo di sviluppo rispetto alla creazione di soluzioni personalizzate.
- **Riduce i costi di manodopera** – Automatizza il ridisposizionamento dei dati, riducendo la necessità di consolidamenti manuali.
- **Pagamento solo per l’uso** – Si paga solo per le chiamate API effettivamente effettuate.
- **Nessuna manutenzione** – Nessun server da gestire, nessun aggiornamento software e nessun problema di compatibilità.

## Come utilizzare l'API Scambia intervallo con gli SDK

### Specifica dell'API Scambia intervallo

La [Specifiche dell'API Scambia intervallo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) definisce un'interfaccia di programmazione pubblicamente accessibile e consente di effettuare interazioni REST direttamente da un browser web.

### Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo di un SDK è il modo più rapido per sviluppare, poiché nasconde i dettagli di basso livello, consentendo di scambiare intervalli con codice conciso. Consulta il [repository GitHub](https://github.com/aspose-cells-cloud) per un elenco completo degli SDK di Aspose.Cells Cloud.

Gli esempi di codice seguenti mostrano come effettuare chiamate ai servizi web Aspose.Cells utilizzando vari SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}
---