---
title: AbstractCalculationEngin
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/abstractcalculationengine/
description: "Aspose.Cells Specifica del modello cloud: AbstractCalculationEngine. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, AbstractCalculationEngine
weight: 50
---
## **abstractCalculationEngine**

Rappresenta il motore di calcolo personalizzato dell'utente per estendere il motore di calcolo predefinito di Aspose.Cells.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| IsParamLiteralRequired| Booleano| VERO| Falso|| Indica se questo motore necessita del testo letterale del parametro durante l'esecuzione del calcolo. Il valore predefinito è falso.|
| IsParamArrayMode obbligatorio| Booleano| VERO| Falso|| Indica se questo motore necessita che il parametro venga calcolato in modalità array. Il valore predefinito è falso. Se è richiesto durante il calcolo delle funzioni personalizzate, questa proprietà deve essere impostata come true.|
| ProcessBuiltInFunctions| Booleano| VERO| Falso|| Se le funzioni integrate supportate dal motore integrato devono essere controllate ed elaborate da questa implementazione. L'impostazione predefinita è falsa. Se l'utente ha bisogno di modificare la logica di calcolo di alcune funzioni integrate, questa proprietà deve essere impostata su true. In caso contrario, lasciare questa proprietà come false per considerazioni sulle prestazioni.|

