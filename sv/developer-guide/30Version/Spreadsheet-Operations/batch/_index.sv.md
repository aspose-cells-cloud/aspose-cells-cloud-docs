---
title: "Batchbehandling av Excel-filer: Konvertera, Lås, Skydda, Dela upp och Lås upp"
second_title: "Dokument"
linktitle: "Batch Excel-filer"
type: docs
url: /sv/batch/
keywords: "Batchbehandling, Excel, konvertering, lås, skydda, dela upp, låsa upp, Aspose.Cells Cloud API, API-referens, batchåtgärder"
description: "Aspose.Cells Cloud API möjliggör batchbehandling av flera Excel-filer för konvertering, låsning, skydd, delning och upplåsning. Innehåller detaljerade API-specifikationer och SDK-stöd för Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift."
weight: 35
ArticleTitle: "Batchbehandling av Excel-filer – Konvertera, Lås, Skydda, Dela upp, Låsa upp med Aspose.Cells Cloud API"
---

Aspose.Cells Cloud API tillhandahåller batchslutpunkter som låter dig utföra vanliga åtgärder på flera Excel-filer i en enda förfrågan. Nedan finns en snabb översikt över tillgängliga batchåtgärder tillsammans med korta API-specifikationer för varje.

- **["Batchkonvertera Excel-filer"](https://docs.aspose.cloud/cells/batch/convert "Batchkonvertera Excel-filer")**  
  *Konvertera flera Excel-filer till ett valt utgångsformat i en enda förfrågan.*  

  **API-specifikation**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parametrar**  

  | Namn           | Typ      | Beskrivning                                   |
  |----------------|----------|-----------------------------------------------|
  | files          | file[]   | En eller flera Excel-filer som ska konverteras. |
  | outputFormat   | string   | Önskat utgångsformat (t.ex. pdf, csv, html).  |
  | storage        | string   | (Valfritt) Namn på molnlagring.               |

  **Svar**  

  | Kod  | Beskrivning                                   |
  |------|-----------------------------------------------|
  | 200  | Konvertering lyckades; returnerar filerna.    |
  | 400  | Ogiltiga parametrar angivna.                  |
  | 401  | Autentisering misslyckades – saknad eller ogiltig token. |
  | 500  | Internt serverfel.                            |

- **["Batchlås Excel-filer"](https://docs.aspose.cloud/cells/batch/lock "Batchlås Excel-filer")**  
  *Tillämpa ett lösenordsbaserat lås på flera Excel-filer samtidigt.*  

  **API-specifikation**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametrar**  

  | Namn     | Typ    | Beskrivning                                |
  |----------|--------|--------------------------------------------|
  | files    | array  | Lista med filidentifierare eller URL:er.  |
  | password | string | Lösenord att låsa arbetsböckerna med.      |
  | storage  | string | (Valfritt) Namn på molnlagring.            |

  **Svar**  

  | Kod  | Beskrivning                                   |
  |------|-----------------------------------------------|
  | 200  | Filerna har låsts framgångsrikt.             |
  | 400  | Saknade eller ogiltiga parametrar.           |
  | 401  | Autentisering misslyckades.                   |
  | 500  | Serverfel.                                    |

- **["Batchskydda Excel-filer"](https://docs.aspose.cloud/cells/batch/protect "Batchskydda Excel-filer")**  
  *Lägg till skyddsalternativ (t.ex. skrivskydd, struktur) på flera arbetsböcker.*  

  **API-specifikation**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametrar**  

  | Namn          | Typ    | Beskrivning                                          |
  |---------------|--------|------------------------------------------------------|
  | files         | array  | Lista med filidentifierare eller URL:er.            |
  | protection    | object | Skyddsalternativ (t.ex. readOnly, structure).       |
  | storage       | string | (Valfritt) Namn på molnlagring.                      |

  **Svar**  

  | Kod  | Beskrivning                                   |
  |------|-----------------------------------------------|
  | 200  | Skydd har tillämpats framgångsrikt.            |
  | 400  | Ogiltig förfrågningsdata.                       |
  | 401  | Autentisering misslyckades.                      |
  | 500  | Oväntat serverfel.                              |

- **["Batchdela upp"](https://docs.aspose.cloud/cells/batch/split "Batchdela upp")**  
  *Dela stora Excel-arbetsböcker i mindre filer baserat på kalkylblad eller radintervall.*  

  **API-specifikation**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametrar**  

  | Namn        | Typ    | Beskrivning                                       |
  |-------------|--------|---------------------------------------------------|
  | files       | array  | Filer som ska delas upp.                          |
  | splitBy     | string | Kriterier: "worksheet" eller "rowRange".          |
  | criteria    | object | Detaljer för den valda delningsmetoden.           |
  | storage     | string | (Valfritt) Namn på molnlagring.                   |

  **Svar**  

  | Kod  | Beskrivning                                   |
  |------|-----------------------------------------------|
  | 200  | Delningsåtgärd slutförd; returnerar delarna.    |
  | 400  | Felaktiga delningsparametrar.                   |
  | 401  | Autentisering misslyckades.                     |
  | 500  | Bearbetningsfel.                                |

- **["Batchlås upp"](https://docs.aspose.cloud/cells/batch/unlock "Batchlås upp")**  
  *Ta bort lösenordsskydd från flera Excel-filer i ett enda anrop.*  

  **API-specifikation**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parametrar**  

  | Namn     | Typ    | Beskrivning                                |
  |----------|--------|--------------------------------------------|
  | files    | array  | Lista med identifierare eller URL:er för låsta filer. |
  | password | string | Nuvarande lösenord för filerna.            |
  | storage  | string | (Valfritt) Namn på molnlagring.            |

  **Svar**  

  | Kod  | Beskrivning                                   |
  |------|-----------------------------------------------|
  | 200  | Filerna har låsts upp framgångsrikt.          |
  | 400  | Felaktigt lösenord eller saknade filer.       |
  | 401  | Autentisering misslyckades.                   |
  | 500  | Serverfel.                                    |
---