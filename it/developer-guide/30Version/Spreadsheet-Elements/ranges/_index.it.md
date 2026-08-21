---
title: "Lavorare con gli intervalli di Excel"
second_title: "Documento"
linktype: "intervalli"
type: docs
url: /it/ranges/
aliases: [/it/working-with-ranges/]
keywords: "Aspose.Cells, intervallo Excel, REST API, SDK, .NET, Java, Python, unire celle, copiare intervalli, impostare valore intervallo"
description: "Scopri come recuperare, modificare, formattare, unire, spostare e copiare intervalli di Excel utilizzando l'API REST di Aspose.Cells Cloud. Include esempi di codice SDK per .NET, Java, Python e altri linguaggi."
weight: 100
ArticleTitle: "Lavorare con gli intervalli di Excel – Documentazione di Aspose.Cells Cloud"
---

Un **intervallo** rappresenta una singola cella, un'intera riga, un'intera colonna, un blocco contiguo di celle o un intervallo tridimensionale (3‑D) che si estende su più fogli di lavoro.

## Lavorare con gli intervalli in un file Excel

L'API REST di Aspose.Cells Cloud fornisce endpoint dedicati per ogni operazione sugli intervalli. L'elenco seguente contiene link agli esempi dettagliati di utilizzo e include il metodo HTTP e l'endpoint corrispondenti per un rapido riferimento.

- [Ottenere gli intervalli con nome all'interno del foglio di calcolo](/it/cells/get-named-ranges-inside-the-workbook/) – Recupera tutti gli intervalli con nome definiti in un foglio di calcolo, restituendone gli indirizzi e l'ambito di validità. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges`.
- [Ottenere i dati delle celle in base all'intervallo con nome](/it/cells/get-cells-data-based-on-named-range/) – Restituisce i valori delle celle appartenenti a un intervallo con nome specificato. **API**: `GET /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/cells`.
- [Modificare l’altezza delle righe all'interno dell'intervallo](/it/cells/cells/change-heights-of-rows-inside-the-range/) – Regola l’altezza di ciascuna riga compresa nell'intervallo dato. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/rows/height`.
- [Modificare la larghezza delle colonne all'interno dell'intervallo](/it/cells/cells/change-widths-of-columns-inside-the-range/) – Modifica la larghezza di tutte le colonne intersecanti l'intervallo. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/columns/width`.
- [Unire un intervallo di celle in una singola cella](/it/cells/combines-a-range-of-cells-into-a-single-cell/) – Unisce le celle selezionate in una singola cella, preservando il valore in alto a sinistra. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/merge`.
- [Copiare un intervallo in un foglio di calcolo con opzioni di incolla](/it/cells/copy-range-in-a-worksheet-with-paste-options/) – Copia un intervallo di origine in un intervallo di destinazione, con opzioni facoltative di incolla (valori, formati, formule, ecc.). **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{sourceRange}/copy?destCell={destRange}&pasteType={type}`.
- [Impostare lo stile dell'intervallo](/it/cells/set-the-style-of-the-range/) – Applica stili di carattere, riempimento, bordi e allineamento a tutte le celle dell'intervallo. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/style`.
- [Annullare l’unione delle celle unite dell’intervallo](/it/cells/unmerge-merged-cells-of-the-range/) – Annulla un’operazione di unione precedente, ripristinando le celle individuali originali. **API**: `POST /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/unmerge`.
- [Spostare un intervallo con nome in un foglio di calcolo Excel](/it/cells/move-a-named-ranged-with-a-excel-worksheet/) – Riposiziona un intervallo con nome a un nuovo indirizzo all’interno dello stesso foglio di calcolo o in un altro foglio di calcolo. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/namedranges/{rangeName}/move`.
- [Impostare il valore dell’intervallo nel foglio di calcolo Excel](/it/cells/ranges/set-value/) – Scrive un singolo valore o un array di valori nell’intervallo specificato. **API**: `PUT /cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}/value`.

Tutte le richieste e le risposte sono in formato JSON. Includere l’header `Authorization` con il proprio token di accesso per l’autenticazione.