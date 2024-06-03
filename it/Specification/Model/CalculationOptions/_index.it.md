---
title: Opzione di calcolo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/calculationoptions/
description: "Aspose.Cells Specifica del modello cloud: CalculationOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Opzioni di calcolo
weight: 50
---
## **calcoloOpzioni**

 Rappresenta le opzioni per il calcolo.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| CalcStackSize| Numero intero| VERO| Falso|| Specifica la dimensione dello stack per il calcolo ricorsivo delle celle.|
| Ignora errore| Booleano| VERO| Falso|| Indica se gli errori riscontrati durante il calcolo delle formule devono essere ignorati. L'errore potrebbe essere una funzione non supportata, collegamenti esterni, ecc. Il valore predefinito è true.|
| PrecisionStrategia| Corda| VERO| Falso|| Specifica la strategia per l'elaborazione della precisione del calcolo.|
| Ricorsivo| Booleano| VERO| Falso|| Indica se calcolare ricorsivamente le celle dipendenti quando si calcola una cella e dipende da altre celle. Il valore predefinito è vero.|
| Motore personalizzato|Classe: Motore di calcolo astratto| VERO| Falso|| Il motore di calcolo della formula personalizzata per estendere il motore di calcolo predefinito di Aspose.Cells.|
| Calcolo Monitor| Classe:MonitorCalcoloAstratto| VERO| Falso|| Il monitor che consente all'utente di monitorare l'avanzamento del calcolo della formula.|
| Origini dati collegate|Vettore<Class:Workbook> | VERO| Falso|| Specifica le origini dati per i collegamenti esterni utilizzati nelle formule.|

