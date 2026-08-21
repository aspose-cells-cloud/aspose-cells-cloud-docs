---
title: Converti Excel in HTML  
description: Converti un cartella di lavoro Excel in un file HTML utilizzando l'API Aspose.Cells Cloud v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Converti Excel in HTML  

Aspose.Cells Cloud fornisce un robusto endpoint REST che converte una cartella di lavoro Excel (XLS, XLSX, CSV, ecc.) in un documento HTML. L'operazione restituisce un oggetto **FileInfo** contenente il file HTML generato (nome, dimensione e contenuto codificato in Base64).

---

## Prerequisiti

| Requisito | Come soddisfarlo |
|-----------|------------------|
| **Account Aspose Cloud** | Iscriviti su [aspose.cloud](https://www.aspose.cloud). |
| **Token di accesso JWT** | Ottieni un token bearer tramite l'endpoint OAuth 2.0 `POST /connect/token`. |
| **Archiviazione (opzionale)** | Se desideri che l'API legga/scriva file da un'archiviazione specifica, creala prima (ad esempio Amazon S3, Azure Blob o l'archiviazione Aspose Cloud). |
| **cURL / SDK** | Qualsiasi client HTTP capace di gestire `multipart/form-data` (cURL, Postman o uno degli SDK di Aspose.Cells). |

---

## Autenticazione

Tutte le richieste alle API di Aspose.Cells Cloud richiedono l'**autenticazione basata su token JWT**.

```http
Authorization: Bearer <access-token>
```

Il token deve essere incluso nell'intestazione `Authorization` di ogni richiesta.

---

## Endpoint

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Nota** – La richiesta deve essere inviata come `multipart/form-data`. Il file Excel rappresenta la prima parte del corpo multipart.

---

### **Sicurezza e autenticazione**

Le API di Aspose.Cells Cloud sono sicure e richiedono l'<a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticazione basata su token JWT</a>.

## Parametri della richiesta  

### Parametri di query  

| Nome                     | Tipo    | Obbligatorio | Predefinito | Descrizione |
|--------------------------|---------|--------------|-------------|-------------|
| `password`               | string  | No           | –           | Password per aprire una cartella di lavoro protetta. |
| `storageName`            | string  | No           | –           | Nome dell'archiviazione in cui risiede il file sorgente. |
| `checkExcelRestriction` | boolean | No           | `true`      | Se `true`, il servizio convalida le restrizioni specifiche di Excel (ad esempio, fogli protetti). |
| `region`                 | string  | No           | –           | Impostazioni locali per la cartella di lavoro (ad esempio, `it-IT`). |
| `FontsLocation`          | string  | No           | –           | URL o percorso di una cartella contenente i caratteri personalizzati necessari per il rendering. |

### Form‑Data (Multipart)  

| Nome | Tipo | Obbligatorio | Descrizione |
|------|------|--------------|-------------|
| **File** | file | **Sì** | La cartella di lavoro Excel da convertire. Deve essere fornita come prima parte della richiesta multipart. |

---

## Esempio di richiesta (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/percorso/del/tuo_cartella_lavoro.xlsx"
```

---

## Risposta corretta  

**Codice di stato:** `200 OK`

| Campo        | Tipo   | Descrizione |
|--------------|--------|-------------|
| `Filename`   | string | Nome del file HTML generato (ad esempio, `esempio.html`). |
| `FileSize`   | int    | Dimensione del file HTML in byte. |
| `FileContent`| string | Contenuto HTML codificato in Base64. |

```json
{
  "Filename": "esempio.html",
  "FileSize": 12345,
  "FileContent": "stringa_in_base64"
}
```

Lo schema di risposta è definito dal modello **FileInfo**: [/cells/file-info](/cells/file-info/).

---

## Risposte di errore  

| Codice | Significato | Payload di esempio |
|--------|-------------|--------------------|
| `400` | Richiesta non valida – parametri mancanti o non validi | ```json { "Code": "BadRequest", "Message": "La parte 'File' è obbligatoria." } ``` |
| `401` | Non autorizzato – token JWT non valido o mancante | ```json { "Code": "InvalidToken", "Message": "Il token di accesso è mancante o scaduto." } ``` |
| `404` | Non trovato – file sorgente non trovato nell'archiviazione specificata | ```json { "Code": "FileNotFound", "Message": "Il file 'mio.xlsx' non esiste nell'archiviazione 'MioArchivio'." } ``` |
| `413` | Payload troppo grande – il file caricato supera la dimensione massima consentita | ```json { "Code": "RequestEntityTooLarge", "Message": "Il file caricato supera il limite di 100 MB." } ``` |
| `429` | Troppa richieste – limite di frequenza superato | ```json { "Code": "TooManyRequests", "Message": "Limite di frequenza di 60 chiamate al minuto superato." } ``` |
| `500` | Errore interno del server – condizione imprevista del server | ```json { "Code": "InternalError", "Message": "Si è verificato un errore imprevisto. Riprova più tardi." } ``` |

---

## Limiti di frequenza  

| Limite | Descrizione |
|--------|-------------|
| **60 richieste al minuto** per account (impostazione predefinita) | Superare questo limite restituisce `429 Too Many Requests`. Regola la logica del client o richiedi una quota superiore tramite il portale Aspose Cloud. |

---

## Supporto SDK  

Aspose fornisce SDK di prima classe che incapsulano questo endpoint per diverse linguaggi. Gli esempi seguenti mostrano la stessa conversione utilizzando gli SDK ufficiali.

| Linguaggio | Esempio |
|------------|---------|
| C#         | <details><summary>Visualizza esempio</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("tuo.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java       | <details><summary>Visualizza esempio</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("tuo.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python     | <details><summary>Visualizza esempio</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('tuo.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js    | <details><summary>Visualizza esempio</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('tuo.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go         | <details><summary>Visualizza esempio</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("tuo.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP        | <details><summary>Visualizza esempio</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('tuo.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby       | <details><summary>Visualizza esempio</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('tuo.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl       | <details><summary>Visualizza esempio</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'tuo.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Per l'elenco completo degli SDK supportati e le istruzioni per l'installazione, consulta il repository **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>.

---

## Endpoint correlati  

| Endpoint | Descrizione |
|----------|-------------|
| `POST /cells/{name}/saveAs` | Salva un file Excel esistente come HTML (o altri formati) direttamente nell'archiviazione. |
| `PUT /cells/convert` | Converte una cartella di lavoro in HTML con opzioni di conversione aggiuntive; il risultato viene restituito nel corpo della risposta. |
| `GET /cells/{name}` | Recupera una cartella di lavoro già memorizzata come HTML (o altri formati), con parametri di query facoltativi. |

---

## Domande frequenti  

**Domanda:** *Come eseguo l'autenticazione quando chiamo l'API di conversione da Excel a HTML?*  
**Risposta:** Includi l'intestazione `Authorization: Bearer <access-token>` ottenuta dall'endpoint OAuth 2.0 `/connect/token`.

**Domanda:** *Cosa contiene la risposta `FileInfo`?*  
**Risposta:** Tre campi: `Filename` (string), `FileSize` (intero, in byte) e `FileContent` (contenuto HTML codificato in Base64).

**Domanda:** *Quali codici di errore potrei incontrare?*  
**Risposta:** `400` (Richiesta non valida), `401` (Non autorizzato), `404` (File non trovato), `413` (Payload troppo grande), `429` (Troppa richieste), `500` (Errore interno del server). Ognuno restituisce un payload JSON contenente `Code` e `Message`.

**Domanda:** *Posso specificare una posizione personalizzata per i caratteri?*  
**Risposta:** Sì. Utilizza il parametro di query `FontsLocation` per indicare una cartella o un URL contenente i caratteri richiesti.

**Domanda:** *Esiste un limite di frequenza per questa operazione?*  
**Risposta:** Il limite predefinito è **60 chiamate al minuto** per account. Superarlo restituisce `429 Too Many Requests`.

---

## Breadcrumb JSON‑LD (dati strutturati)

L'aggiunta di questo blocco migliora il SEO consentendo breadcrumb di tipo rich snippet nei risultati di ricerca.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Developer Center", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversion", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel to HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Registro delle modifiche  

| Versione | Data | Modifiche |
|----------|------|-----------|
| **v3.0** | 2024‑10‑01 | Rilascio iniziale pubblico di `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Aggiunti i parametri di query `region` e `FontsLocation`; aggiornato il formato del payload di errore. |
| **v3.2** | 2026‑03‑20 | Introdotta la documentazione sui limiti di frequenza e gli esempi di risposte di errore. |

--- 

*Per ulteriore assistenza, contatta il supporto Aspose o consulta la documentazione ufficiale dell'API:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---