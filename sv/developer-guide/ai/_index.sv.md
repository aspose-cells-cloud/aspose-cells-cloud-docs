---
title: "Aspose.Cells Cloud AI – Uppgiftsdelning, kalkylark och textöversättning"
second_title: "Dokument"
ArticleTitle: "Förbättra dina AI-färdigheter: Lär dig Excel-översättning, uppdelning av uppgifter och mer"
linktitle: "AI"
type: docs
url: /ai/
keywords: "Aspose.Cells, Cloud AI, Excel-översättning, uppgiftsdelning, REST API"
description: "Utforska Aspose.Cells Cloud AI för att dela upp uppgifter, översätta Excel-arbetsböcker och textfiler. Inkluderar REST-slutpunkter, exempelkod och bästa praxis."
weight: 20
---

Aspose.Cells Cloud AI erbjuder tre kraftfulla AI-drivna tjänster som förenklar arbetet med Excel- och textdata: **Dela upp användaruppgift**, **Översätt kalkylark** och **Översätt textfil**. Dessa API:er möjliggör för utvecklare att programmeringsmässigt dela upp komplexa användarmål i åtgärdssteg, översätta hela arbetsböcker eller textfiler i klartextformat samt integrera resultaten i egna applikationer. Använd slutpunkterna nedan för att komma igång snabbt, och hänvisa till detaljerade begäran/svar-specifikationer för varje tjänst.

- **[Dela upp användaruppgift](https://docs.aspose.cloud/cells/decompose-user-task/)** – Omvandla användarmål till sekventiella åtgärdsplaner med Aspose.Cells Cloud AI.  
  - **Begäran:** `POST`  
  - **Slutpunkts-URL:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **Rubriker:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **Begärandetext (JSON):**  
    ```json
    {
      "task": "Skapa en kvartalsvis försäljningsrapport med diagram och pivot-tabeller"
    }
    ```  
  - **Svar:** Returnerar filen med kalkylarket som innehåller uppgiftslistan som en hätningsbar fil.  
  - **Statuskoder:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`  
  - **Förutsättningar:** En giltig åtkomsttoken med scope **CellsAI**.  
  - **Exempelsvar (JSON-utdrag):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **Anteckningar:** Den genererade arbetsboken innehåller ett kalkylblad med namnet **TaskList** med ordnade steg. Begränsning: 100 begärningar per minut.

- **[Översätt kalkylark](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – Översätt ett helt kalkylark med Aspose.Cells Cloud AI.  
  - **Begäran:** `POST`  
  - **Slutpunkts-URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **Rubriker:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Begärandeparametrar:**  
    - `file` – Den Excel-fil som ska översättas (binär data).  
    - `targetLanguage` – ISO-språkkod (t.ex. `sv`, `de`).  
  - **Svar:** Returnerar den översatta arbetsboken som en hätningsbar fil.  
  - **Statuskoder:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Förutsättningar:** Åtkomsttoken med scope **CellsAI** och tillräckligt ledigt lagringsutrymme.  
  - **Exempelsvar (JSON-utdrag):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **Anteckningar:** Alla cellvärden, kommentarer och kalkylbladsnamn översätts. Begränsning: 100 begärningar per minut.

- **[Översätt textfil](https://docs.aspose.cloud/cells/translate-text-file/)** – Översätt en helt textfil med Aspose.Cells Cloud AI.  
  - **Begäran:** `POST`  
  - **Slutpunkts-URL:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **Rubriker:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **Begärandeparametrar:**  
    - `file` – Den textfil som ska översättas (binär data).  
    - `targetLanguage` – ISO-språkkod (t.ex. `es`, `ja`).  
  - **Svar:** Returnerar den översatta textfilen.  
  - **Statuskoder:** `200 OK`, `400 Bad Request`, `401 Unauthorized`, `415 Unsupported Media Type`, `500 Internal Server Error`  
  - **Förutsättningar:** Giltig åtkomsttoken med scope **CellsAI**.  
  - **Exempelsvar (JSON-utdrag):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **Anteckningar:** Stödjer UTF-8-kodade textfiler upp till 5 MB. Begränsning: 100 begärningar per minut.