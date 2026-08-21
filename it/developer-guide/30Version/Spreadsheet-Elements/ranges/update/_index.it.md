---
title: "Come aggiornare il contenuto di un intervallo in un foglio di calcolo Excel"
second_title: "Document"
linktype: "Aggiornamento"
type: docs
url: /it/ranges/update/
keywords: "Excel, aggiornamento intervallo, Aspose.Cells Cloud, REST API, foglio di calcolo, stile intervallo, valori intervallo, altezza riga, larghezza colonna"
description: "Aggiorna il contenuto di un intervallo in un foglio di calcolo Excel utilizzando l'API REST di Aspose.Cells Cloud. Modifica stili, valori, altezze riga e larghezze colonna tramite gli SDK supportati."
weight: 20
ArticleTitle: "Come aggiornare il contenuto di un intervallo in un foglio di calcolo Excel – Documentazione Aspose.Cells Cloud"
---

## Lavorare con l'aggiornamento del contenuto di un intervallo in un foglio di calcolo Excel

Prima di utilizzare le operazioni di aggiornamento, assicurati di disporre di un token valido per l'API REST di Aspose.Cells Cloud e che il workbook di destinazione sia archiviato nel tuo archivio cloud. L'API è disponibile tramite SDK per Android, .NET, Go, Java, Node.js, Perl, PHP, Python, Ruby e Swift.

Di seguito è riportato un riepilogo conciso delle quattro azioni principali di aggiornamento. Questa tabella fornisce agli sviluppatori un riferimento rapido per il metodo HTTP, il modello di endpoint, i parametri chiave e la risposta tipica in caso di esito positivo per ciascuna operazione.

| Azione             | Metodo HTTP | Modello di endpoint                                                                                  | Parametri chiave              | Risposta 200‑OK               |
|--------------------|-------------|------------------------------------------------------------------------------------------------------|-------------------------------|------------------------------|
| Imposta stile      | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/style`                                      | Oggetto `style`               | Stile intervallo aggiornato  |
| Imposta valori     | POST        | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/values`                                    | Array `values`                | Valori intervallo aggiornati |
| Altezza riga       | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/rowheight`                                 | Numero `height`               | Altezza riga aggiornata       |
| Larghezza colonna  | PUT         | `/cells/{fileName}/worksheets/{sheetName}/ranges/{range}/columnwidth`                               | Numero `width`                | Larghezza colonna aggiornata |

Questa pagina fornisce un accesso rapido alle quattro principali azioni di aggiornamento: impostazione dello stile di un intervallo, impostazione dei valori di un intervallo, regolazione dell'altezza delle righe e regolazione della larghezza delle colonne.

- [Come impostare lo stile di un intervallo in un foglio di calcolo Excel.](/cells/ranges/update/style/) 
- [Come impostare i valori di un intervallo in un foglio di calcolo Excel.](/cells/ranges/update/values/) 
- [Come impostare l'altezza delle righe di un intervallo in un foglio di calcolo Excel.](/cells/ranges/update/row-height/) 
- [Come impostare la larghezza delle colonne di un intervallo in un foglio di calcolo Excel.](/cells/ranges/update/column-width/)