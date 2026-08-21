---
---
title: "Kom igång med Aspose.Cells Cloud API – bearbeta Excel-filer i 3 enkla steg"
second_title: "Dokument"
ArticleTitle: "Aspose.Cells Cloud – Kom igång"
linktitle: "Kom igång"
type: docs
url: /sv/getting-started/
description: "Lär dig hur du laddar upp, konverterar och hämtar Excel-filer med Aspose.Cells Cloud REST API i tre enkla steg. Innehåller cURL-kodexempel."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, kalkylbladskonvertering, Excel till PDF, molnbaserat kalkylblad, Aspose.Cells Cloud API"
---

- [Översikt](/sv/overview/)
- [Snabbstart](/sv/quickstart/)
- [Tillgängliga SDK:er](/sv/available-sdks/)
- [Stödda plattformar](/sv/supported-platforms/)
- [Stödda filformat](/sv/supported-file-formats/)
- [Testa Aspose.Cells Cloud](/sv/evaluate-aspose-cells/)
- [Prenumerationsplan](/sv/pricing-plan/)
- [Teknisk support](/sv/technical-support/)
- [Så här kör du en Docker-container](/sv/how-to-run-docker-container/)

**Kom igång-guide**

Innan du börjar, se till att du har en giltig **Aspose Cloud API-nyckel** och ett giltigt **lagringsnamn**. Dessa autentiseringsuppgifter krävs för alla efterföljande API-anrop.

**Steg 1: Ladda upp en Excel-fil**  
Ladda upp din källarbok till Aspose Cloud-lagringen.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

* Begärandetext: Filen skickas som en binär ström (`application/octet-stream`).  
* Nödvändiga parametrar:

- `path` – lagrings sökväg där filen ska sparas (t.ex. `mapp/sample.xlsx`).

**Steg 2: Konvertera arbetsboken till PDF**  
Skicka en konverteringsförfrågan efter att filen har lagrats.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

* Nödvändiga parametrar:

- `name` – namn på den uppladdade arbetsboken (t.ex. `sample.xlsx`).  
- `format` – målformat (`pdf`).  
- `outputPath` – lagrings sökväg för den konverterade filen (t.ex. `mapp/result.pdf`).

* Exempel på svarspayload (JSON):

```json
{
  "status": "OK",
  "outputPath": "mapp/result.pdf"
}
```

**Steg 3: Hämta den konverterade PDF-filen**  
Hämta den resulterande PDF-filen från lagringen.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

* Nödvändiga parametrar:

- `outputPath` – sökvägen till PDF-filen som genererades i föregående steg.

**Sammanfattning av exempelbegäran/svar**

| Åtgärd | HTTP-metod | Endpoint (exempel) | Parametrar | Status vid lyckad åtgärd |
|--------|------------|---------------------|------------|---------------------------|
| Ladda upp | PUT | /cells/storage/file/{path} | `path` (lagringsplats) | 200 OK |
| Konvertera | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| Hämta | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**Vanliga felkoder**

- **400 Bad Request (Ogiltig begäran)** – Saknade eller ogiltiga parametrar.  
- **401 Unauthorized (Obehörig)** – Ogiltig eller saknad åtkomsttoken.  
- **404 Not Found (Ej hittad)** – Den angivna filen eller sökvägen finns inte.  
- **500 Internal Server Error (Internt serverfel)** – Oväntat serverfel; försök igen eller kontakta support.  
---