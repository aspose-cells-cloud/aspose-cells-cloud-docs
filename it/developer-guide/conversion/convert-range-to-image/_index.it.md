---
title: "Converti intervallo Excel in immagine – Aspose.Cells Cloud API"
description: "Converti un intervallo specifico da un file Excel locale in PNG, JPEG, SVG, TIFF o BMP tramite l'API REST Aspose.Cells Cloud – non è necessario caricare l'intero libro."
keywords: "Aspose.Cells Cloud, converti intervallo in immagine, API Excel, formati immagine, PNG, JPEG, SVG, TIFF, BMP"
slug: convert-range-to-image
api_version: "v4.0"
date: 2026-07-30
---

La chiamata legge un file spreadsheet locale, converte l'intervallo specificato e restituisce l'immagine come flusso binario.

## Metodo di conversione intervallo in immagine

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/image
```

### **Sicurezza e autenticazione**

Le API Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Parametri della richiesta

| Nome               | Posizione                          | Tipo    | Obbligatorio | Descrizione                                                                     |
| ------------------ | --------------------------------- | ------- | ------------ | ------------------------------------------------------------------------------- |
| **Spreadsheet**    | Form‑Data (`multipart/form-data`) | File    | **Sì**       | Il file Excel da elaborare.                                                     |
| **worksheet**      | Query                             | Stringa | **Sì**       | Nome del foglio di lavoro contenente l'intervallo (es. `Sheet1`).              |
| **range**          | Query                             | Stringa | **Sì**       | Area di celle da convertire, ad esempio `A1:C10`.                              |
| **format**         | Query                             | Stringa | **Sì**       | Formato immagine in uscita (`png`, `jpeg`, `svg`, `tiff`, `bmp`).              |
| **printHeadings**  | Query                             | Booleano| No           | `true` per includere le intestazioni di riga/columni nell'immagine.            |
| **outPath**        | Query                             | Stringa | No           | Percorso della cartella per il file generato, se si desidera salvarlo nello storage cloud. |
| **outStorageName** | Query                             | Stringa | No           | Nome del servizio di archiviazione (es. `MyStorage`).                          |
| **fontsLocation**  | Query                             | Stringa | No           | URL o percorso dei caratteri personalizzati utilizzati durante la conversione. |
| **region**         | Query                             | Stringa | No           | Identificatore delle impostazioni locali (es. `en-US`, `fr-FR`). Influenza la formattazione di numeri e date. |
| **password**       | Query                             | Stringa | No           | Password per libri di lavoro crittografati.                                    |
| **AutoRowsFit**    | Query                             | Booleano| No           | Ridimensiona automaticamente le righe prima del rendering.                     |
| **AutoColumnsFit** | Query                             | Booleano| No           | Ridimensiona automaticamente le colonne prima del rendering.                   |

## Risposta

L'API restituisce il file HTML convertito come **flusso binario** (`application/octet-stream`).

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

### Esempio di risposta positiva (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423
```

Salva il corpo della risposta in un file (ad esempio `report.png`) per visualizzare l'immagine resa in un browser.

---

**Codici di stato HTTP**

| Codice | Significato            | Descrizione                                                       |
| ------ | ---------------------- | ----------------------------------------------------------------- |
| 200    | OK                     | Filtro applicato correttamente; la risposta contiene i dettagli dell'operazione. |
| 400    | Richiesta non valida   | Parametri mancanti o non validi (ad esempio, tipo di file non supportato). |
| 401    | Non autorizzato        | Token JWT non valido o mancante.                                  |
| 413    | Payload troppo grande  | Il file caricato supera il limite di dimensione.                  |
| 500    | Errore interno del server | Errore imprevisto del server.                                   |

## Come utilizzare l'API Converti intervallo in immagine con gli SDK?

### Specifica OpenAPI

La [Specifiche OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToImage) descrive un'API pubblicamente accessibile, consentendo interazioni REST direttamente da un browser web.

Puoi utilizzare lo strumento a riga di comando cURL per accedere facilmente ai servizi web Aspose.Cells. L'esempio seguente mostra come effettuare chiamate all'API Cloud con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Richiesta" tabName12="Risposta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/image?format=png&worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.png"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="report.png"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

## Utilizzare gli SDK di Aspose.Cells Cloud

L'utilizzo dell'SDK rappresenta il modo più rapido per sviluppare, poiché nasconde i dettagli a basso livello, consentendo di convertire un intervallo di dati in un file immagine con un codice minimo.  
Esplora l'elenco completo degli SDK di Aspose.Cells Cloud nel nostro [repository GitHub](https://github.com/aspose-cells-cloud).

I seguenti esempi di codice illustrano come chiamare i servizi web Aspose.Cells utilizzando vari SDK. Se il caricamento da Gist è bloccato, puoi scaricare direttamente gli esempi dal repository.

---