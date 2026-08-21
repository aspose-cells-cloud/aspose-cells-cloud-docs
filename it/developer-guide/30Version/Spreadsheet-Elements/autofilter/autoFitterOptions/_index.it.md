---
---
title: "AutoFitterOptions – Guida alle proprietà e all'utilizzo | Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, adattamento automatico Excel, altezza riga, celle unite, API"
description: "Scopri come controllare l'adattamento automatico dell'altezza delle righe, la gestione delle celle unite, le righe/columne nascoste, le impostazioni linguistiche e le opzioni di rendering mediante l'oggetto AutoFitterOptions nell'API Aspose.Cells Cloud."
weight: 79
ArticleTitle: "AutoFitterOptions – Guida alle proprietà e all'utilizzo per Aspose.Cells Cloud"
---

# Proprietà di AutoFitterOptions

L'oggetto `AutoFitterOptions` consente di regolare con precisione l'adattamento automatico dell'altezza delle righe eseguito da Aspose.Cells Cloud. Risulta utile quando è necessario un controllo preciso sulla gestione delle celle unite, sulle righe/columne nascoste, sulla formattazione specifica della lingua o sul comportamento legato al rendering.

**Prerequisiti** – Per utilizzare queste opzioni è necessario essere autenticati con un token di accesso OAuth 2.0 valido che includa l'ambito **Cells.ReadWrite**. La richiesta funziona con qualsiasi versione dell'SDK che supporti l'API v3.0.

| Nome                       | Tipo        | Descrizione                                                                                     | Note                                                                                                       |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Determina il modo in cui vengono adattate automaticamente le celle unite.                    | Valori ammessi: `All`, `First`, `None`. Valore predefinito: `All`. Esempio JSON: `"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**           | **boolean** | Se **true**, righe e colonne nascoste vengono ignorate durante il processo di adattamento automatico. | Valore predefinito: `false`. Esempio JSON: `"IgnoreHidden":false`                                          |
| **OnlyAuto**               | **boolean** | Indica se adattare automaticamente solo le righe la cui altezza non è stata personalizzata manualmente. | Valore predefinito: `false`. Esempio JSON: `"OnlyAuto":false`                                              |
| **DefaultEditLanguage**    | **string**  | Imposta la lingua predefinita per la modifica del cartella di lavoro.                         | Valore predefinito: lingua di sistema (ad es. `"en-US"`). Esempio JSON: `"DefaultEditLanguage":"en-US"`      |
| **MaxRowHeight**           | **double**  | Altezza massima della riga (in punti) applicata durante l'adattamento automatico. Un valore **0** indica nessun limite. | Valore predefinito: `0`. Esempio JSON: `"MaxRowHeight":0`                                                  |
| **AutoFitWrappedTextType** | **string**  | Controlla come il testo a capo automatico all'interno delle celle viene adattato.             | Valori ammessi: `All`, `OnlyWrapped`, `None`. Valore predefinito: `All`. Esempio JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Specifica la strategia di formattazione utilizzata durante l'operazione di adattamento automatico. | Valori comuni: `AutoFit`, `PreserveExisting`. Valore predefinito: `AutoFit`. Esempio JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Indica se eseguire l'adattamento automatico per scopi di rendering (ad es. PDF, immagine).     | Valori ammessi: `True`, `False`. Valore predefinito: `False`. Esempio JSON: `"ForRendering":"False"`        |

Di seguito è riportato un payload JSON tipico che può essere inviato all'API quando si configura `AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Una richiesta `cURL` di esempio che applica queste opzioni a un cartella di lavoro:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Riferimento all'endpoint**

| Metodo | URL | Parametri obbligatori | Descrizione |
|--------|-----|-----------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (corpo JSON) | Applica le opzioni `AutoFitterOptions` specificate al cartella di lavoro di destinazione. |
| GET    | `/cells/workbook/autoFitter` | *nessuno* | Recupera le impostazioni correnti di `AutoFitterOptions` per il cartella di lavoro. |

**Parametri della richiesta per l'endpoint PUT**

| Parametro                | Tipo    | Obbligatorio | Descrizione |
|--------------------------|---------|--------------|-------------|
| AutoFitMergedCellsType   | string  | Sì           | Modalità di adattamento automatico delle celle unite (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | No           | Indica se ignorare le righe/colonne nascoste. |
| OnlyAuto                 | boolean | No           | Adatta solo le righe senza impostazioni manuali dell'altezza. |
| DefaultEditLanguage      | string  | No           | Lingua di modifica (ad es. `en-US`). |
| MaxRowHeight             | double  | No           | Altezza massima della riga in punti; `0` = illimitata. |
| AutoFitWrappedTextType   | string  | No           | Modalità di gestione del testo a capo (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | No           | Strategia di formattazione (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | No           | Applica l'adattamento automatico per il rendering (`True`, `False`). |

Codici di risposta tipici:

- **200 OK** – Operazione completata con successo.  
- **400 Bad Request** – Payload JSON non valido o valore non supportato.  
- **401 Unauthorized** – Token di autenticazione mancante o non valido.  
- **500 Internal Server Error** – Errore imprevisto del server.

**Esempio di risposta GET**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Questi esempi illustrano come configurare e richiamare il modello `AutoFitterOptions` all'interno dell'API Aspose.Cells Cloud.