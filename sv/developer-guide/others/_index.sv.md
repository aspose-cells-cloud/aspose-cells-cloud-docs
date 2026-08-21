---
title: "Aspise.Cells molnwebb-API – Övriga funktioner:hälsokontroll, hämta offentlig nyckel"
linktitle: "Övriga funktioner"
ArticleTitle: "Övriga funktioner: hälsokontroll, hämta offentlig nyckel"
second_title: "Dokument"
type: docs
url: /sv/other-features/
keywords: "Aspose.Cells, moln-API, hälsokontroll, offentlig nyckel, åtkomsttoken, Excel, REST"
description: "Utforska Aspose.Cells moln andra funktioner: hälsokontrolländpunkt, hämtning av offentlig nyckel och tokengenerering för att säkra dina Excel-API-integrationer."
weight: 180
---

**Förutsättningar** – För att kunna använda de funktioner som listas nedan måste du ha ett giltigt Aspose Cloud-prenumeration och ett aktivt **Client ID** / **Client Secret**-par för autentisering.

Dessa “övriga funktioner” tillhandahåller viktiga stödåtgärder för Aspose.Cells moln-API, såsom bekräftelse av tjänstens tillgänglighet, hämtning av kryptografiska nycklar och utgivning av åtkomsttoken. De anropas vanligtvis innan du arbetar med arbetsboksrelaterade slutpunkter.

- **[Aspose.Cells molnhälsokontroll](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Kontrollera att Aspose.Cells molntjänsten är nåbar och fungerar korrekt. Ett lyckat anrop returnerar **HTTP 200** med JSON `{ "status": "OK" }`. Använd denna slutpunkt tidigt i din arbetsflödesprocess för att undvika onödiga fel.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Läs mer</a>

- **[Hämta Aspose.Cells moln driftstatus](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Hämta den aktuella driftstatusen för tjänsten. Svaret anger om API:t är helt funktionsdugligt, i underhållsläge eller upplever problem.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Läs mer</a>

- **[Hämta offentlig nyckel](https://docs.aspose.cloud/cells/get-public-key/)**  
  Få tag på den RSA-offentliga nyckeln (i PEM-format) som används för att verifiera JWT-token som utfärdats av Aspose.Cells moln. Denna nyckel krävs när du validerar token på din serversida.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Läs mer</a>

- **[Hämta åtkomsttoken med Client ID och hemlighet](https://docs.aspose.cloud/cells/post-access-token/)**  
  Generera en OAuth 2.0-åtkomsttoken med grant-typen **client_credentials**. Inkludera ditt **Client ID** och **Client Secret** i begärandetexten; svaret innehåller `access_token`, `token_type` och `expires_in`. Denna token måste skickas i `Authorization`-headern för alla efterföljande API-anrop.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Läs mer</a>