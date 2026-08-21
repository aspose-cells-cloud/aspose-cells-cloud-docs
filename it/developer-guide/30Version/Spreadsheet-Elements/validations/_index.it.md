---
title: "Lavorare con la convalida dei dati di Excel"
second_title: "Documento"
linktype: "Convalide"
type: docs
url: /it/validations/
keywords: "convalida dei dati di Excel, Aspose.Cells Cloud, REST API, foglio di calcolo, Office Cloud"
description: "Scopri come aggiungere, recuperare, aggiornare, eliminare e cancellare le regole di convalida dei dati di Excel in modo programmatico con l'API REST di Aspose.Cells Cloud. Include esempi per .NET, Java, Python e PHP."
weight: 100
ArticleTitle: "Lavorare con la convalida dei dati di Excel - Documentazione API Aspose.Cells Cloud"
---

La convalida dei dati di Excel è una funzionalità di Microsoft Excel utilizzata per controllare ciò che un utente può inserire in una cella di un foglio di calcolo. Può limitare le inserzioni a un intervallo di date specifico, a numeri interi solo o persino creare elenchi a discesa che risparmiano spazio e visualizzano i valori in una singola cella. È inoltre possibile definire un messaggio personalizzato che appare quando un utente immette un valore errato o un formato non valido.

Ad esempio, un utente può specificare un appuntamento programmato tra le 9:00 e le 18:00.

La convalida dei dati può essere utilizzata per garantire che un valore sia un numero positivo, una data compresa tra il 15° e il 30° giorno di un mese, una data che si verifica nei prossimi 30 giorni o una voce di testo contenente meno di 25 caratteri, e così via.

### Riepilogo dell'API

| Operazione | Metodo HTTP | Endpoint | Descrizione |
|-----------|-------------|----------|-------------|
| Aggiungi | POST | `/cells/{file}/worksheets/{sheet}/validations` | Crea una regola di convalida |
| Ottieni | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Recupera una regola specifica |
| Ottieni tutte | GET | `/cells/{file}/worksheets/{sheet}/validations` | Elenca tutte le regole |
| Aggiorna | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Modifica una regola |
| Elimina | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Rimuove una regola |
| Cancella | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Rimuove tutte le regole |

## Lavorare con le convalide in un file Excel

- [Come aggiungere una regola di convalida a un foglio di calcolo Excel](/cells/validations/add/)
- [Come recuperare una regola di convalida da un foglio di calcolo Excel](/cells/validations/get/)
- [Come recuperare tutte le regole di convalida da un foglio di calcolo Excel](/cells/validations/get-all/)
- [Come eliminare una regola di convalida da un foglio di calcolo Excel](/cells/validations/delete/)
- [Come cancellare tutte le regole di convalida da un foglio di calcolo Excel](/cells/validations/clear/)
- [Come aggiornare una regola di convalida su un foglio di calcolo Excel](/cells/validations/update/)
---