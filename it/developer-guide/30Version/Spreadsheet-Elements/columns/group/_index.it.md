---
title: "Raggruppa Colonne – Documentazione Aspise.Cells Cloud API"
description: "Raggruppa le colonne del foglio di lavoro in un foglio di calcolo Excel utilizzando l'API REST Aspose.Cells Cloud (v3.0). Include la sintassi della richiesta, i parametri, esempi cURL e SDK e i dettagli della risposta."
keywords: "Aspose.Cells, raggruppa colonne, API Excel, REST, SDK cloud"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# Raggruppare Colonne su un Foglio di Lavoro Excel

**Versione API:** v3.0  
**Operazione:** `PostGroupWorksheetColumns` – Raggruppa le colonne del foglio di lavoro nel foglio di lavoro.

---

## Panoramica

Questa API REST consente di raggruppare un intervallo di colonne in un foglio di lavoro. Le colonne raggruppate possono essere mostrate o nascoste, consentendo di creare sezioni comprimibili simili a quelle di Microsoft Excel.

---

## Prerequisiti

- Un **token di accesso JWT** valido ottenuto dal servizio di autenticazione di Aspose Cloud.  
- Il workbook deve essere memorizzato in una posizione accessibile ad Aspose.Cells Cloud (archivio predefinito o un nome di archivio personalizzato).  
- Versione SDK richiesta (se si utilizza un SDK): l'ultima release che supporta la versione API **v3.0**.  

---

## Autenticazione

Tutte le richieste richiedono l'autenticazione con **token Bearer**.

```http
Authorization: Bearer <access_token>
```

Per maggiori dettagli su come ottenere un token, consulta la [guida all'autenticazione JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## Richiesta HTTP

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| Parametro | Posizione | Obbligatorio | Descrizione |
|-----------|----------|--------------|-------------|
| `name` | Path | Sì | Nome del file del workbook (es. `test.xlsx`). |
| `sheetName` | Path | Sì | Nome del foglio di lavoro contenente le colonne da raggruppare. |
| `firstIndex` | Query | Sì | Indice in base zero della prima colonna da includere nel gruppo. |
| `lastIndex` | Query | Sì | Indice in base zero dell'ultima colonna da includere nel gruppo. |
| `hide` | Query | No | Se `true`, le colonne raggruppate vengono nascoste; altrimenti rimangono visibili. |
| `folder` | Query | No | Percorso della cartella contenente il workbook. |
| `storageName` | Query | No | Nome del servizio di archiviazione in cui si trova il file. |

---

## Esempio di Richiesta (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **Nota:** La richiesta utilizza **HTTPS** per garantire la crittografia della comunicazione.

---

## Risposta

### Successo (200)

| Campo | Tipo | Descrizione |
|-------|------|-------------|
| `Code` | integer | Codice di stato HTTP (`200`). |
| `Status` | string | Stato testuale dell'operazione (`OK`). |

**Esempio**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Errore (es. 400 Bad Request)

| Campo | Tipo | Descrizione |
|-------|------|-------------|
| `Code` | integer | Codice di stato HTTP (`400`, `401`, `404`, `500`, …). |
| `Status` | string | Stato testuale (`Error`). |
| `ErrorMessage` | string | Descrizione leggibile dell'errore. |
| `ErrorCode` | string | Identificatore programmatico dell'errore. |

**Esempio – Richiesta non valida**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "Indice di colonna non valido.",
  "ErrorCode": "InvalidParameter"
}
```

---

## Esempi SDK

I seguenti frammenti mostrano come chiamare l'operazione **Raggruppa Colonne Foglio di Lavoro** utilizzando gli SDK supportati.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## Note

- **Comportamento del raggruppamento:** L'API crea un gruppo di colonne che può essere espanso o compresso in Excel. Impostando `hide=true`, il gruppo viene immediatamente compresso.  
- **Indicizzazione in base zero:** Sia `firstIndex` che `lastIndex` iniziano da **0**; la prima colonna in un foglio di lavoro ha indice 0.  
- **Considerazioni sull'archiviazione:** Se il workbook si trova in un archivio non predefinito, fornire entrambi i parametri di query `folder` e `storageName`.  

---

## Vedi Anche

- [Autenticazione – Token JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [Specifica OpenAPI per Raggruppa Colonne Foglio di Lavoro](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDK Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [Raggruppare Righelle su un Foglio di Lavoro Excel](/rows/group/)  

---

> *Illustrazione:* ![Schermata che mostra colonne raggruppate in un foglio di lavoro Excel](./images/group-columns.png){: .img-fluid alt="Schermata che mostra colonne raggruppate in un foglio di lavoro Excel" }

*L'immagine di seguito è un segnaposto e dovrebbe essere sostituita con una schermata reale che dimostri il risultato visivo del raggruppamento delle colonne.*