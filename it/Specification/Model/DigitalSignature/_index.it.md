---
title: Firma digitale
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/digitalsignature/
description: "Aspose.Cells Specifica del modello Cloud: Firma Digitale. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Firma digitale
weight: 50
---
## **firma digitale**

 Firma nel fascicolo.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Commenti| Corda| VERO| Falso|| Lo scopo della firma.|
| SignTime| Corda| VERO| Falso|| L'ora in cui è stato firmato il documento.|
| Id| Corda| VERO| Falso|| Specifica un GUID a cui è possibile fare riferimento incrociato con il GUID della riga della firma archiviata nel contenuto del documento. Il valore predefinito è Guid vuoto (tutti zeri).|
| Parola d'ordine| Corda| VERO| Falso|| Specifica il testo della firma effettiva nella firma digitale. Il valore predefinito è Vuoto.|
| Immagine|Vettore<Byte> | VERO| Falso|| Specifica un'immagine per la firma digitale. Il valore predefinito è nullo.|
| ProviderId| Corda| VERO| Falso|| Specifica l'ID classe del provider della firma. Il valore predefinito è Guid vuoto (tutti zeri).|
| È valido| Booleano| VERO| Falso|| Se questa firma digitale è valida e il documento non è stato manomesso, questo valore sarà vero.|
| XAdESTType| Corda| VERO| Falso|| Tipo XAdES. Il valore predefinito è Nessuno (XAdES è disattivato).|

