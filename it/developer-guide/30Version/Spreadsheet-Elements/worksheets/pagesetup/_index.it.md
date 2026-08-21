---
---
title: "Configurazione della pagina del foglio di lavoro"
second_title: "Documento"
linktitle: "Configurazione pagina"
type: docs
url: /it/page-setup/
keywords: "Aspose.Cells, pageSetup, foglio di lavoro, impostazioni di stampa, margini, orientamento, dimensione carta, intestazione, piè di pagina, ridimensionamento"
description: "Scopri come configurare il layout di stampa del foglio di lavoro Excel con l'oggetto PageSetup di Aspose.Cells Cloud. Include elenco delle proprietà, valori predefiniti, intervalli e campioni di codice per C#, Java e Python."
weight: 20
ArticleTitle: "Configurazione della pagina del foglio di lavoro – Configura il layout di stampa con Aspose.Cells Cloud"
---

# **PageSetup**

Impostazioni di stampa della pagina Excel

## Panoramica

L'oggetto **PageSetup** definisce le opzioni di layout di stampa per un foglio di lavoro Excel, come margini, orientamento, ridimensionamento, intestazioni, piè di pagina e altre impostazioni relative alla stampa. Configurare queste proprietà consente agli sviluppatori di produrre cartelle di lavoro stampabili che corrispondano all'aspetto e alla suddivisione in pagine desiderati.

Di seguito è riportato un breve esempio in C# che mostra come impostare le proprietà comuni di PageSetup utilizzando l'SDK di Aspose.Cells Cloud:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Inizializza il client API (sostituisci con le tue credenziali)
var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");

// Definisci le impostazioni PageSetup
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Applica le impostazioni al primo foglio di lavoro della cartella di lavoro
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Questo frammento imposta il foglio di lavoro in orientamento orizzontale, utilizza carta A4, centra il contenuto e applica un fattore di ridimensionamento al 100%.

## Proprietà

| Nome proprietà        | Tipo proprietà | Nullable | ReadOnly | Valore predefinito | Descrizione                                                                  |
| --------------------- | -------------- | -------- | -------- | ------------------ | ---------------------------------------------------------------------------- |
| BlackAndWhite         | bool           | false    | false    | false              | Stampa il foglio di lavoro in modalità bianco e nero.                        |
| BottomMargin          | float          | true     | false    | 2,54 cm            | Dimensione del margine inferiore in centimetri.                               |
| CenterHorizontally    | bool           | false    | false    | false              | Centra il foglio orizzontalmente durante la stampa.                          |
| CenterVertically      | bool           | false    | false    | false              | Centra il foglio verticalmente durante la stampa.                            |
| FirstPageNumber       | int            | true     | false    | 1                  | Il numero della prima pagina utilizzato quando il foglio viene stampato.     |
| FitToPagesTall        | int            | false    | false    | 1                  | Numero di pagine in altezza a cui verrà ridimensionato il foglio di lavoro.  |
| FitToPagesWide        | int            | false    | false    | 1                  | Numero di pagine in larghezza a cui verrà ridimensionato il foglio di lavoro.|
| FooterMargin          | float          | true     | false    | 2,54 cm            | Distanza dal fondo della pagina al piè di pagina, in centimetri.             |
| HeaderMargin          | float          | true     | false    | 2,54 cm            | Distanza dall'alto della pagina all'intestazione, in centimetri.             |
| IsAutoFirstPageNumber | bool           | false    | false    | false              | Assegna automaticamente il numero della prima pagina.                        |
| IsHFAlignMargins      | bool           | false    | false    | true               | Se true, i margini dell'intestazione/piede di pagina sono allineati con i margini della pagina. |
| IsHFDiffFirst         | bool           | false    | false    | false              | Indica che l'intestazione/piede di pagina nella prima pagina è diverso da quello delle altre pagine. |
| IsHFDiffOddEven       | bool           | false    | false    | false              | Indica che l'intestazione/piede di pagina nelle pagine dispari è diverso da quello nelle pagine pari. |
| IsHFScaleWithDoc      | bool           | false    | false    | false              | Ridimensiona intestazione e piè di pagina insieme al documento (Excel 2007+).|
| IsPercentScale        | bool           | false    | false    | true               | Se false, `FitToPagesWide` e `FitToPagesTall` controllano il ridimensionamento. |
| LeftMargin            | float          | true     | false    | 2,54 cm            | Dimensione del margine sinistro in centimetri.                               |
| Order                 | string         | true     | false    | "DownThenOver"     | Ordine con cui Excel numera le pagine durante la stampa di un foglio di lavoro di grandi dimensioni. |
| Orientation           | string         | false    | false    | "Portrait"         | Orientamento pagina: **Landscape** (orizzontale) o **Portrait** (verticale).|
| PaperSize             | string         | true     | false    | "A4"               | Dimensione carta utilizzata per la stampa.                                   |
| PrintArea             | string         | true     | false    | (nessuno)          | Intervallo di celle da stampare (es. `"A1:D20"`).                            |
| PrintComments         | string         | true     | false    | "NoComments"       | Modalità di stampa dei commenti con il foglio.                              |
| PrintCopies           | int            | true     | false    | 1                  | Numero di copie da stampare.                                                 |
| PrintDraft            | bool           | false    | false    | false              | Stampa il foglio di lavoro in modalità bozza (nessuna grafica).             |
| PrintErrors           | string         | true     | false    | "Display"          | Tipo di errore di stampa visualizzato.                                       |
| PrintGridlines        | bool           | false    | false    | false              | Stampa le linee di griglia delle celle.                                      |
| PrintHeadings         | bool           | false    | false    | false              | Stampa le intestazioni di riga e colonna.                                    |
| PrintQuality          | int            | true     | false    | 600                | Impostazione qualità di stampa (punti per pollice).                          |
| PrintTitleColumns     | string         | true     | false    | (nessuno)          | Colonne da ripetere sul lato sinistro di ogni pagina stampata.              |
| PrintTitleRows        | string         | true     | false    | (nessuno)          | Righe da ripetere nella parte superiore di ogni pagina stampata.            |
| RightMargin           | float          | true     | false    | 2,54 cm            | Dimensione del margine destro in centimetri.                                 |
| TopMargin             | float          | true     | false    | 2,54 cm            | Dimensione del margine superiore in centimetri.                              |
| Zoom                  | int            | false    | false    | 100                | Fattore di ridimensionamento in percentuale (10–400%).                       |
| Header                | object         | true     | false    | (nessuno)          | Configurazione dell'intestazione di pagina.                                  |
| Footer                | object         | true     | false    | (nessuno)          | Configurazione del piè di pagina.                                            |

## Oggetti correlati

- **Header** – Configura l'intestazione del foglio di lavoro.  
- **Footer** – Configura il piè di pagina del foglio di lavoro.  
- **PrintOptions** – Ulteriori impostazioni relative alla stampa, come interruzioni di pagina e area di stampa.  
---