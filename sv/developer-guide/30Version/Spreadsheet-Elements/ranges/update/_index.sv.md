---
title: "Så här uppdaterar du innehåll i ett interval från ett Excel-ark"
second_title: "Dokument"
linktype: "Uppdatera"
type: docs
url: /ranges/update/
keywords: "Excel, intervaluppdatering, Aspose.Cells Cloud, REST API, kalkylark, intervallstil, intervallvärden, radhöjd, kolumnbredd"
description: "Uppdatera intervalldata i ett Excel-ark med Aspose.Cells Cloud REST API. Ändra stilar, värden, radhöjder och kolumnbredder via stödda SDK:er."
weight: 20
ArticleTitle: "Så här uppdaterar du intervalldata från ett Excel-ark – Aspose.Cells Cloud-dokumentation"
---

## Arbeta med uppdatering av intervalldata i ett Excel-ark

Innan du använder uppdateringsåtgärderna, se till att du har ett giltigt Aspose.Cells Cloud API-token och att målarboksdokumentet finns lagrat i din molnlagring. API:et finns tillgängligt via SDK:er för Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift.

En kort sammanfattning av de fyra huvudsakliga uppdateringsåtgärderna ges nedan. Denna tabell ger utvecklare en snabb referens för HTTP-metod, slutpunktsschema, nyckelparametrar och typiskt lyckat svar (200-OK) för varje åtgärd.

| Åtgärd          | HTTP-metod | Slutpunktsschema                                                                                     | Nyckelparametrar              | 200‑OK-svar                  |
|-----------------|------------|------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------|
| Ställ in stil   | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | `style`-objekt                | Uppdaterad intervallstil     |
| Ställ in värden | POST       | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | `values`-array                | Uppdaterade intervallvärden  |
| Radhöjd         | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | `height` (nummer)             | Uppdaterad radhöjd           |
| Kolumnbredd     | PUT        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | `width` (nummer)              | Uppdaterad kolumnbredd       |

Den här sidan ger snabb tillgång till de fyra huvudsakliga uppdateringsåtgärderna: ställa in stil för ett intervall, ställa in värden för ett intervall, justera radhöjder och justera kolumnbredder.

- [Så här ställer du in stil för ett intervall i ett Excel-ark.](/cells/ranges/update/style/) 
- [Så här ställer du in värden för ett intervall i ett Excel-ark.](/cells/ranges/update/values/) 
- [Så här ställer du in radhöjder för ett intervall i ett Excel-ark.](/cells/ranges/update/row-height/) 
- [Så här ställer du in kolumnbredder för ett intervall i ett Excel-ark.](/cells/ranges/update/column-width/)