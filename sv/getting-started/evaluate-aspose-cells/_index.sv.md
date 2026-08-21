---
title: "Utvärdera Aspose.Cells Cloud"
second_title: "Dokument"
ArticleTitle: "Utvärdera Aspose.Cells Cloud"
LinkTitle: "Utvärdera"
type: docs
url: /sv/evaluate-aspose-cells/
description: "Utforska Aspose.Cells Cloud, REST API:et för att skapa, konvertera, sammanfoga, dela, skydda och manipulera Excel-filer och andra kalkylbladsformat."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - kalkylbladsmanipulering
  - kostnadsfri provperiod
  - utvärdera
---

Du kan utvärdera **Aspose.Cells Cloud** REST API:er genom att skapa ett kostnadsfritt provkonto på Aspose Cloud Dashboard. Efter registrering får du en **Client Id** och ett **Client Secret**, vilket tillåter upp till 150 API-anrop per månad.

**Förutsättningar**  
Innan du börjar, se till att du har en aktiv internetanslutning och en supportad utvecklingsmiljö. API:et kan anropas direkt via HTTP, eller så kan du använda ett av Aspose.Cells SDK:erna (t.ex. .NET, Java, Python, PHP) för enklare integration.

**Snabbstartssteg**

1. **Skapa ett kostnadsfritt provkonto** – besök [Aspose Cloud Dashboard](https://dashboard.aspose.cloud), registrera dig och bekräfta din e-postadress.  
2. **Hämta autentiseringsuppgifter** – hitta *Client Id* och *Client Secret* i dashboardens avsnitt **Authentication** (Autentisering).  
3. **Generera en åtkomsttoken** – skicka en `POST`-begäran till `https://api.aspose.cloud/connect/token` med dina autentiseringsuppgifter (se API-referensen för exakt begärandetext).  
4. **Gör ditt första API-anrop** – inkludera token i `Authorization: Bearer <token>`-huvudet och anropa en enkel slutpunkt, t.ex. `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

Den kostnadsfria provperioden ger dig en praktisk känsla för tjänstens funktioner och möjlighet till tidig utveckling och testning utan några kostnader.

**Sammanfattning av API-referens**

| Åtgärd | Metod | URL | Krävda parametrar | Exempelsvar |
|--------|-------|-----|-------------------|-------------|
| Hämta åtkomsttoken | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (form-URL-encoded) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| Lista kalkylblad | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | Sökväg: `{file}` – namn på den uppladdade arbetsboken; Huvud: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Sheet1" }, { "Name": "Sheet2" } ] } }` |

För detaljerad prisinformation, användningsbegränsningar och ytterligare planalternativ, se sidan [Trial Plan](https://purchase.aspose.cloud/trial).