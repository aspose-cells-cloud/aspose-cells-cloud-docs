---
title: "Arbeta med Excel-metadata och dokumentegenskaper"
second_title: "Dokument"
linktitle: "Metadata och egenskaper"
type: docs
url: /sv/metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel-metadata, dokumentegenskaps-API, REST-API, hämta metadata, uppdatera Excel-egenskaper, ta bort Excel-metadata"
description: "Lär dig hur du läser, lägger till, uppdaterar och tar bort Excel-filmetadata med Aspose.Cells Cloud REST API. Innehåller exempel för cURL och SDK:er för Java, .NET, Python, Node.js och mer."
ArticleTitle: "Arbeta med Excel-metadata och dokumentegenskaper – Aspose.Cells Cloud"
weight: 100
---

Excel-filer kan lagra en mängd metadata som hjälper till att identifiera, organisera och hantera dokumenten. Aspose.Cells Cloud tillhandahåller ett enkelt REST-API för att läsa, lägga till, uppdatera och ta bort denna metadata, vilket gör att utvecklare kan integrera hantering av dokumentegenskaper i sina applikationer. Denna guide täcker de två huvudkategorier av egenskaper – standard och anpassade – förklarar hur du arbetar med dem och innehåller direktlänkar till relevanta API-slutpunkter. Du hittar också en kompakt API-referenstabell med begärandeförfarandeförfaranden för att påskynda implementeringen.

**Senast uppdaterad:** 8 juli 2026  

**Typer av dokumentegenskaper**

Innan du lär dig hur du använder Aspose.Cells Cloud API:er för att visa, ändra och ta bort dokumentegenskaper (metadata) i Excel, ska vi klargöra vilka typer av egenskaper ett Excel-dokument kan ha.

- **Standardegenskaper** är gemensamma för Excel. De innehåller grundläggande information såsom Titel, Ämne, Författare, Kategori, etc. Du kan tilldela anpassade textvärden till dessa egenskaper för att göra filen lättare att hitta.

- **Anpassade egenskaper** är användardefinierade. De tillåter dig att lägga till ytterligare metadata till ditt Excel-dokument.

**Hur man arbetar med dokumentegenskaper i en Excel-fil**

- [Hur man får en specifik dokumentegenskap med hjälp av lagring](/cells/document-properties/get/)
- [Hur man får dokumentegenskaper utan att använda lagring](/cells/metadata/get/)
- [Hur man får alla dokumentegenskaper med hjälp av lagring](/cells/document-properties/get-all/)
- [Hur man uppdaterar en specifik dokumentegenskap med hjälp av lagring](/cells/document-properties/update/)
- [Hur man uppdaterar en specifik dokumentegenskap utan att använda lagring](/cells/metadata/update/)
- [Hur man tar bort en specifik dokumentegenskap med hjälp av lagring](/cells/document-properties/delete/)
- [Hur man tar bort dokumentegenskaper utan att använda lagring](/cells/metadata/delete/)
- [Hur man tar bort alla dokumentegenskaper med hjälp av lagring](/cells/document-properties/clear/)

**API-referens (utan lagring)**  

| Metod | Slutpunkt | Beskrivning |
|-------|-----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Hämtar alla dokumentegenskaper för arbetsboken som är lagrade i molnet. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Hämtar värdet för en specifik egenskap (standard eller anpassad) identifierad av `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Uppdaterar värdet på en befintlig egenskap. Begärandetexten innehåller det nya värdet i JSON-format. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Tar bort en specifik egenskap från arbetsboken. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Rensar alla anpassade och standardegenskaper från arbetsboken. |

*Alla begäranden kräver en OAuth 2.0-åtkomsttoken och kan innehålla valfria frågeparametrar såsom `storage` och `folder` när en specifik lagringsplats används.*