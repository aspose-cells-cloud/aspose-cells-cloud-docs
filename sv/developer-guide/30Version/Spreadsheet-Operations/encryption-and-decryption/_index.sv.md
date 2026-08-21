---
title: "Kryptera, dekryptera och digitalt signera Excel-filer"
second_title: "Dokument"
linktitle: "Säkerställ Excel"
type: docs
url: /sv/protect/
aliases: [/sv/workbook/password/]
keywords: "Excel, säkerställ, kryptera, dekryptera, digital signatur, Aspose.Cells Cloud, REST API, lösenord, säkerhet"
description: "Lär dig hur du säkerställer, krypterar, dekrypterar och digitalt signerar Excel-arbetsböcker med Aspose.Cells Cloud REST API – kodexempel för Android, C#, Java, Python och mer."
ArticleTitle: "Kryptera, dekryptera, digitalt signera och säkerställ Excel-filer med Aspose.Cells Cloud API"
weight: 36
---

## **Säkerställa och av säkerställa Excel-filer**

**Vad innebär "säkerställa" i Aspose.Cells Cloud?**  
**Säkerställnings**-åtgärden skyddar en Excel-arbetsbok genom att tillämpa ett lösenord som begränsar möjligheten att öppna, redigera eller ändra filens struktur. API:et stöder även kryptering av arbetsboken, dekryptering samt tillägg av en digital signatur för ändringsbevis.

**API-referens**  

| HTTP-metod | Endpoint | Nödvändiga fråge- eller brödparametrar | Exempel på brödtext | Typiska svar |
|-------------|----------|-----------------------------------|---------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (sökväg), `password` (fråga) | `{ "password": "MySecret123" }` | `200 OK` – skydd tillämpat, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (sökväg), `password` (fråga) | Ingen | `200 OK` – skydd borttaget, felkoder enligt ovan |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (sökväg), `password` (fråga) | Ingen | `200 OK` – filen krypterad |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (sökväg), `password` (fråga) | Ingen | `200 OK` – filen dekrypterad |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (sökväg) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "certPass" }` | `200 OK` – digital signatur tillagd |

**Kodexempel (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Initiera API-klienten
var config = new Configuration
{
    AppSid = "DIN_APP_SID",
    AppKey = "DIN_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Säkerställ arbetsboken
var protectRequest = new PostProtectWorkbookRequest(
    name: "Sample.xlsx",
    password: "MySecret123"
);
api.PostProtectWorkbook(protectRequest);
```

**Förutsättningar**  
- En aktiv Aspose.Cells Cloud-prenumeration.  
- `AppSid` och `AppKey` för autentisering.  

**Autentisering**  
Alla förfrågningar måste inkludera `Authorization`-huvudet med ett giltigt JWT-token hämtat från autentiseringsendpointen hos Aspose Cloud.

**Felhantering**  
Kontrollera HTTP-statuskoden och `Error`-objektet som returneras i svarets brödtext. Vanliga fel inkluderar ogiltigt lösenord (`400`), saknad fil (`404`) samt autentiseringsfel (`401`).

**Anteckningar**  
- Samma endpoint kan användas för att **kryptera** eller **dekryptera** genom att ändra åtgärdssegmentet (`/encrypt`, `/decrypt`).  
- Digitala signaturer kräver en giltig certifikatfil som är tillgänglig för API:et.

- [Kryptera en Excel-fil med Aspose.Cells Cloud API](/sv/cells/excel-file-encrypt/)
- [Säkerställ en Excel-fil med Aspose.Cells Cloud API](/sv/cells/protect-excel-file/)
- [Lägg till en digital signatur i en Excel-fil](/sv/cells/excel-digital-signature/)
- [Säkerställ Excel-filer – detaljerad guide](/sv/cells/protect-excel-files/)
- [Ange ett lösenord för en Excel-fil](/sv/cells/workbook/password/modify/)
- [Dekryptera en Excel-fil](/sv/cells/excel-file-decrypt/)
- [Av säkerställ en Excel-fil](/sv/cells/excel-file-unprotect/)
- [Lås upp Excel-filer](/sv/cells/unlock-excel-files/)
- [Rensa lösenordet från en Excel-fil](/sv/cells/clear-excel-files-password/)