---
title: CopiaOpzione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/copyoptions/
description: "Aspose.Cells Specifica del modello cloud: CopyOptions. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, CopyOptions
weight: 50
---
## **copyOptions**

 Rappresenta le opzioni di copia.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Larghezza carattere colonna| Booleano| VERO| Falso|| Indica se copiare la larghezza della colonna in unità di caratteri.|
| CopiaInvalidFormulasAsValues| Booleano| VERO| Falso|| Se la formula non è valida per la destinazione, copia solo i valori.|
| CopiaNomi| Booleano| VERO| Falso||Indica se copiare i nomi.|
| Estendi all'intervallo adiacente| Booleano| VERO| Falso|| Indica se estendere gli intervalli quando si copia l'intervallo in un intervallo adiacente.|
| Fare riferimento al foglio di destinazione| Booleano| VERO| Falso|| Quando si copia l'intervallo nello stesso file e il grafico fa riferimento al foglio di origine, False significa che l'origine dati del grafico copiato non verrà modificata. Vero significa che l'origine dati del grafico copiato fa riferimento al foglio di destinazione.|
| Fare riferimento al foglio con lo stesso nome| Booleano| VERO| Falso|| In MS Excel, quando si copiano formule che fanno riferimento ad altri fogli di lavoro mentre si copia un foglio di lavoro su un altro, le formule copiate dovrebbero fare riferimento alla cartella di lavoro di origine. Tuttavia, in alcune situazioni l'utente potrebbe aver bisogno che le formule copiate facciano riferimento a fogli di lavoro con lo stesso nome nella stessa cartella di lavoro, ad esempio quando tali fogli di lavoro sono stati copiati prima di questa operazione di copia, quindi questa proprietà deve essere mantenuta su true.|

