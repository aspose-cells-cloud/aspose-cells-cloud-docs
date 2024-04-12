---
title: Crea richieste tabella pivot
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/createpivottablerequest/
description: "Aspose.Cells Specifica del modello cloud: CreatePivotTableRequest. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **createPivotTableRequest**

 Indica la richiesta di creazione di una tabella pivot

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Nome| Corda| VERO| Falso|| Nome della tabella pivot|
| Dati di origine| Corda| VERO| Falso|| I dati per la nuova cache della tabella pivot.|
| NomeCellaDest| Corda| VERO| Falso|| La cella nell'angolo superiore sinistro dell'intervallo di destinazione del rapporto di tabella pivot.|
| UsaSameSource| Booleano| VERO| Falso|| Indica se si utilizza la stessa origine dati quando un'altra tabella pivot esistente ha utilizzato questa origine dati. Se la proprietà è true, verrà risparmiata memoria.|
| Righe del campo pivot|Vettore<Integer> | VERO| Falso|| Rappresenta i campi riga in un rapporto di tabella pivot.|
| Colonne del campo pivot|Vettore<Integer> | VERO| Falso||Rappresenta i campi colonna in un rapporto di tabella pivot.|
|Dati campo pivot|Vettore<Integer> | VERO| Falso|| Rappresenta i campi dati in un rapporto di tabella pivot.|

