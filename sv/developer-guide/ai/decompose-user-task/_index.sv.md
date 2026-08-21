---
title: "Aspose.Cells Cloud AI – API för uppdelning av användaruppgifter (v4.0) | SMART-uppgiftsplanering"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar användarmål till sekventiella åtgärdsplaner med Aspose.Cells Cloud AI:s API för uppdelning av uppgifter"
linktitle: "Uppdelning av användaruppgift"
type: docs
url: /decompose-user-task/
keywords: "Aspose.Cells AI, API för uppdelning av uppgifter, SMART-uppgiftsplanering, Redmine-import, projektautomatisering"
description: "Omvandla fritt formuleringa mål till SMART, tidsuppskattade uppgiftslistor med Aspose.Cells Cloud AI. Få CSV/XLSX-utdata för Redmine, Jira eller Azure DevOps med ett enda PUT-anrop."
weight: 100
---

**DecomposeUserTask**-ändpunkten tillhandahåller en REST-ändpunkt för att omvandla en fritt formulering uppgiftsbeskrivning till en detaljerad, sekventiell åtgärdsplan som följer SMART-kriterier. Den allokerar automatiskt tidsuppskattningar i timmar, formaterar utdata för Redmine-kompatibel import och skapar projektmejlstensnoder. Genom att endast ange den råa uppgiftslistan och valfria tidsuppskattningar returnerar API:t en direkt använderbar fil (CSV, XLSX, etc.) som kan importeras direkt till projektledningsverktyg, vilket automatiserar uppdelningen av uppgifter och minskar manuellt arbete.

## **API för uppdelning av användaruppgift**

### Webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

### **Parametrar för begäran:**

| Parameternamn   | Typ    | Plats  | Obligatoriskt/fakultativt | Beskrivning                                                                                                                                                                                                                              |
| :-------------- | :----- | :----- | :------------------------ | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription | string | Brödtext | Obligatoriskt             | En textbaserad beskrivning av användarens övergripande mål. Tjänsten tolkar beskrivningen och genererar individuella uppgifter. Exempel: “Starta marknadsföringskampanj för Q3, inklusive innehållsskapande, e-postutskick och sociala medierannonser.” |

### **Svar**

Lyckat svar (200 OK)  
Content‑Type: `application/octet-stream` (binär filström)

Rubriker:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <storlek i byte>`

Samma struktur används för XLSX/ODS-format, med kolumner placerade i det första kalkylbladet.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                      |
| --- | --------------------- | ---------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärd detaljer. |
| 400 | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Inte auktoriserad     | Ogiltig eller saknad JWT-token.                                  |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                |
| 500 | Internt serverfel     | Oväntat serverfel.                                               |

**Exempel på felaktigt svar (400 Felaktig begäran)**

```json
{
  "code": "InvalidParameter",
  "message": "Fältet 'TaskDescription' är obligatoriskt och får inte vara tomt."
}
```

**Exempel på begärandetext (JSON)**

```json
{
  "TaskDescription": "Utveckla ett webb-API för en funktion för uppdelning av uppgifter i det befintliga systemet."
}
```

**Exempel på svar**  
API:et returnerar en binär ström som innehåller den genererade filen. För att förhandsgranska de första raderna i ett CSV-svar kan du avkoda strömmen och visa rubrikraden, t.ex.:

```
ID,Ämne,Ansvarig,Uppskattad varaktighet,Beskrivning
1	InSamling av krav för task‑splitting API	Business Analyst	8	Samla in funktionella och icke-funktionella krav, användarhistorier och acceptanskriterier för den nya task‑splitting-ändpunkten.
2	API-specifikation (OpenAPI)	Business Analyst	6	Definiera OpenAPI-kontraktet för POST /tasks/split, inklusive begäranschema, svarsformat, felkoder och säkerhetskrav.
3	Uppdelningsalgoritm & datamodelldesign	Solution Architect	5	Designa kärnalgoritmen som delar en överordnad uppgift i deluppgifter, och utöka datamodellen (databastabeller/entiteter) för att lagra hierarki och metadata.
4	Översikt över arkitekturintegration	Solution Architect	4	Analysera påverkan på befintliga tjänster, händelseflöden och databasmigreringar; skapa integrationsplan.
...
```

## Var bör vi använda API:et för uppdelning av användaruppgift?

- **Projektstart**: Omvandla en övergripande projektöversikt till en Redmine-kompatibel uppgiftslista med tidsuppskattningar, vilket möjliggör omedelbar sprintplanering.
- **Marknadsföringsautomatisering**: Dela upp kampanjmål i exekverbara steg, exportera som CSV och importera till uppgiftsledningsverktyg för tvärtimmar-samarbete.
- **Resursallokering**: Generera timbaserade uppskattningar för varje deluppgift, vilket gör att ledare kan balansera arbetsbelastningen mellan teammedlemmar innan projektet påbörjas.
- **Milestonespårning**: Skapa automatiskt mejlstensnoder som kan synkroniseras med Gantt-diagramverktyg, vilket säkerställer att varje fas har ett tydligt leveransmål.

## Varför bör du använda API:et för uppdelning av användaruppgift?

- **SMART-kompatibel utdata** säkerställer att varje genererad uppgift uppfyller kriterierna Specific, Measurable, Achievable, Relevant och Time-bound.
- **Inbyggda timbaserade tidsuppskattningar** eliminierar behovet av manuella beräkningar och förbättrar noggrannheten i prognoser.
- **Direkt importbara filformat** (CSV, XLSX, etc.) underlättar integration med Redmine, Jira, Azure DevOps och andra projektledningsplattformar.
- **Automatisering med ett enda anrop** möjliggör uppdelning av uppgifter via ett enda anrop, vilket påskyndar projektstarten och minskar manuellt arbete.

## Hur man använder API:et för uppdelning av användaruppgift med SDK:er

### API-specifikation för uppdelning av användaruppgift

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">API-specifikation för uppdelning av användaruppgift</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

## Excel API SDK

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på lågnivå och låter dig anropa DecomposeUserTask-ändpunkten med koncis kod.  
Kolla in <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-förrådet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.  
Följande kodexempel visar hur man interagerar med Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---