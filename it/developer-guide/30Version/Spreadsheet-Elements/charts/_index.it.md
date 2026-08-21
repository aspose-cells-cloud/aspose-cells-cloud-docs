---
title: "Lavorare con i grafici di Excel"
second_title: "Documento"
linktitle: "Grafici"
type: docs
url: /it/charts/
aliases: [/it/working-with-charts/]
keywords: "Aspose, Cells, Excel, grafico, API, REST, Cloud, foglio di calcolo"
description: "Scopri come gestire i grafici di Excel con l'API Aspose.Cells Cloud. Guide passo-passo, esempi di codice e gestione degli errori per recuperare, aggiungere, aggiornare, eliminare e convertire i grafici in immagini."
weight: 100
ArticleTitle: "Lavorare con i grafici di Excel – Documentazione di Aspose.Cells Cloud"
---

## Lavorare con i grafici in un file Excel

**Ultimo aggiornamento:** luglio 2026  

I grafici di Excel sono rappresentazioni visive dei dati che aiutano gli utenti a comprendere rapidamente tendenze e schemi.  
L'API Aspose.Cells Cloud consente agli sviluppatori di lavorare programmaticamente con questi grafici all'interno di cartelle di lavoro Excel archiviate nel cloud. Con l'API è possibile recuperare i grafici esistenti, aggiungerne di nuovi, modificarne le proprietà (come titoli, assi e legende), eliminare i grafici non necessari e convertire i grafici in formati immagine per la generazione di report o per elaborazioni successive. I link seguenti forniscono l'accesso diretto alle pagine operative dettagliate per ciascuna azione supportata relativa ai grafici.

### Riferimento rapido

| Operazione | Metodo HTTP | Endpoint (modello) | Documentazione |
|-----------|-------------|---------------------|---------------|
| Recupera grafico | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Recupera un grafico da un foglio di calcolo](/it/cells/get-chart-from-a-worksheet/) |
| Aggiungi grafico | POST | `/cells/{file}/worksheets/{sheet}/charts` | [Aggiungi un grafico in un foglio di calcolo](/it/cells/add-a-chart-in-a-worksheet/) |
| Elimina tutti i grafici | DELETE | `/cells/{file}/worksheets/{sheet}/charts` | [Elimina tutti i grafici da un foglio di calcolo](/it/cells/delete-all-charts-from-a-worksheet/) |
| Elimina grafico | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Elimina un grafico da un foglio di calcolo](/it/cells/delete-a-chart-from-a-worksheet/) |
| Converti grafico in immagine | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/image` | [Converti grafico in immagine](/it/cells/convert-chart-to-image/) |
| Recupera area grafico | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area` | [Recupera area grafico da un foglio di calcolo](/it/cells/get-chart-area-from-a-worksheet/) |
| Recupera formato riempimento | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/area/fillformat` | [Recupera il formato di riempimento dell'area di un grafico da un foglio di calcolo](/it/cells/get-fill-format-of-a-chart-area-from-a-worksheet/) |
| Recupera legenda | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Recupera la legenda del grafico da un foglio di calcolo](/it/cells/get-chart-legend-from-a-worksheet/) |
| Aggiorna legenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend` | [Aggiorna la legenda del grafico in un foglio di calcolo](/it/cells/update-chart-legend-in-a-worksheet/) |
| Mostra legenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/show` | [Mostra la legenda del grafico in un foglio di calcolo](/it/cells/show-chart-legend-in-a-worksheet/) |
| Nascondi legenda | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/legend/hide` | [Nascondi la legenda del grafico in un foglio di calcolo](/it/cells/hide-chart-legend-in-a-worksheet/) |
| Recupera titolo | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Recupera il titolo del grafico da un foglio di calcolo](/it/cells/get-chart-title-from-a-worksheet/) |
| Imposta titolo | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Imposta il titolo del grafico in un foglio di calcolo Excel](/it/cells/set-chart-title-in-excel-worksheet/) |
| Aggiorna titolo | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Aggiorna il titolo del grafico in un foglio di calcolo Excel](/it/cells/update-chart-title-in-excel-worksheet/) |
| Elimina titolo | DELETE | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/title` | [Elimina il titolo del grafico in un foglio di calcolo](/it/cells/delete-chart-title-in-a-worksheet/) |
| Aggiorna proprietà del grafico | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}` | [Aggiorna le proprietà del grafico](/it/cells/charts/properties/update/) |
| Recupera asse delle categorie | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Recupera l'asse delle categorie del grafico](/it/cells/charts/category-axis/get/) |
| Recupera asse dei valori | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Recupera l'asse dei valori del grafico](/it/cells/charts/value-axis/get/) |
| Recupera secondo asse delle categorie | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Recupera il secondo asse delle categorie del grafico](/it/cells/charts/second-category-axis/get/) |
| Recupera secondo asse dei valori | GET | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Recupera il secondo asse dei valori del grafico](/it/cells/charts/second-value-axis/get/) |
| Aggiorna asse delle categorie | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/categoryaxis` | [Aggiorna l'asse delle categorie del grafico](/it/cells/charts/category-axis/update/) |
| Aggiorna asse dei valori | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/valueaxis` | [Aggiorna l'asse dei valori del grafico](/it/cells/charts/value-axis/update/) |
| Aggiorna secondo asse delle categorie | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondcategoryaxis` | [Aggiorna il secondo asse delle categorie del grafico](/it/cells/charts/second-category-axis/update/) |
| Aggiorna secondo asse dei valori | POST | `/cells/{file}/worksheets/{sheet}/charts/{chartIndex}/secondvalueaxis` | [Aggiorna il secondo asse dei valori del grafico](/it/cells/charts/second-value-axis/update/) |

- [Recupera un grafico da un foglio di calcolo](/it/cells/get-chart-from-a-worksheet/)
- [Aggiungi un grafico in un foglio di calcolo](/it/cells/add-a-chart-in-a-worksheet/)
- [Elimina tutti i grafici da un foglio di calcolo](/it/cells/delete-all-charts-from-a-worksheet/)
- [Elimina un grafico da un foglio di calcolo](/it/cells/delete-a-chart-from-a-worksheet/)
- [Converti grafico in immagine](/it/cells/convert-chart-to-image/)
- [Recupera area grafico da un foglio di calcolo](/it/cells/get-chart-area-from-a-worksheet/)
- [Recupera il formato di riempimento dell'area di un grafico da un foglio di calcolo](/it/cells/get-fill-format-of-a-chart-area-from-a-worksheet/)
- [Recupera la legenda del grafico da un foglio di calcolo](/it/cells/get-chart-legend-from-a-worksheet/)
- [Aggiorna la legenda del grafico in un foglio di calcolo](/it/cells/update-chart-legend-in-a-worksheet/)
- [Mostra la legenda del grafico in un foglio di calcolo](/it/cells/show-chart-legend-in-a-worksheet/)
- [Nascondi la legenda del grafico in un foglio di calcolo](/it/cells/hide-chart-legend-in-a-worksheet/)
- [Recupera il titolo del grafico da un foglio di calcolo](/it/cells/get-chart-title-from-a-worksheet/)
- [Imposta il titolo del grafico in un foglio di calcolo Excel](/it/cells/set-chart-title-in-excel-worksheet/)
- [Aggiorna il titolo del grafico in un foglio di calcolo Excel](/it/cells/update-chart-title-in-excel-worksheet/)
- [Elimina il titolo del grafico in un foglio di calcolo](/it/cells/delete-chart-title-in-a-worksheet/)
- [Aggiorna le proprietà del grafico](/it/cells/charts/properties/update/)
- [Recupera l'asse delle categorie del grafico](/it/cells/charts/category-axis/get/)
- [Recupera l'asse dei valori del grafico](/it/cells/charts/value-axis/get/)
- [Recupera il secondo asse delle categorie del grafico](/it/cells/charts/second-category-axis/get/)
- [Recupera il secondo asse dei valori del grafico](/it/cells/charts/second-value-axis/get/)
- [Aggiorna l'asse delle categorie del grafico](/it/cells/charts/category-axis/update/)
- [Aggiorna l'asse dei valori del grafico](/it/cells/charts/value-axis/update/)
- [Aggiorna il secondo asse delle categorie del grafico](/it/cells/charts/second-category-axis/update/)
- [Aggiorna il secondo asse dei valori del grafico](/it/cells/charts/second-value-axis/update/)