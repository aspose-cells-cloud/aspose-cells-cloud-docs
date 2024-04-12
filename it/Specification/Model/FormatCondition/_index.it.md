---
title: FormatoCondizione
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/formatcondition/
description: "Aspose.Cells Specifica del modello cloud: FormatCondition. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **formatCondizione**

 

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Priorità| Numero intero| VERO| Falso|| La priorità di questa regola di formattazione condizionale. Questo valore viene utilizzato per determinare quale formato deve essere valutato e sottoposto a rendering. I valori numerici più bassi hanno una priorità più alta rispetto ai valori numerici più alti, dove "1" è la priorità più alta.|
| Tipo| Corda| VERO| Falso|| Ottiene e imposta se il formato condizionale Type.|
| StopIfTrue| Booleano| VERO| Falso|| È vero, nessuna regola con priorità inferiore può essere applicata a questa regola, quando questa regola risulta vera. Vale solo per Excel 2007;|
| Sopra la media| Classe: sopra la media| VERO| Falso||Ottieni l'istanza "AboveAverage" della formattazione condizionale. La regola dell'istanza predefinita evidenzia le celle che sono al di sopra della media per tutti i valori nell'intervallo. Valido solo per tipo = Sopra la media.|
| ColorScale| Classe: ColorScale| VERO| Falso|| Ottieni l'istanza "ColorScale" della formattazione condizionale. L'istanza predefinita è un 3ColorScale "verde-giallo-rosso". Valido solo per type = ColorScale.|
| DataBar| Classe:DataBar| VERO| Falso|| Ottieni l'istanza "DataBar" della formattazione condizionale. Il colore dell'istanza predefinita è blu. Valido solo per il tipo DataBar.|
| Formula 1| Corda| VERO| Falso|| Ottiene e imposta il valore o l'espressione associata alla formattazione condizionale.|
| Formula2| Corda| VERO| Falso|| Ottiene e imposta il valore o l'espressione associata alla formattazione condizionale.|
| Set di icone| Classe:IconSet| VERO| Falso||Ottieni l'istanza "IconSet" della formattazione condizionale. L'IconSetType dell'istanza predefinita è TrafficLights31. Valido solo per type = IconSet.|
| Operatore| Corda| VERO| Falso|| Ottiene e imposta il tipo di operatore del formato condizionale.|
| Stile| Classe: stile| VERO| Falso|| Ottiene o imposta lo stile degli intervalli di celle formattati condizionali.|
| Testo| Corda| VERO| Falso|| Il valore del testo in una regola di formattazione condizionale "il testo contiene". Valido solo per type = contieneText, notContainsText, BeginsWith e EndsWith. Il valore predefinito è null.|
| Periodo di tempo| Corda| VERO| Falso|| Il periodo di tempo applicabile in una regola di formattazione condizionale "data che si verifica...". Valido solo per type = timePeriod. Il valore predefinito è TimePeriodType.Today.|
| Top10| Classe:Top10| VERO| Falso||Ottieni l'istanza "Top10" della formattazione condizionale. La regola dell'istanza predefinita evidenzia le celle i cui valori rientrano nella parentesi dei primi 10. Valido solo per il tipo Top10.|
| collegamento| Classe: collegamento| VERO| Falso|||

**Nome del genitore** : (ElementoLink)[elementolink]**Nome dei bambini** : 
	-  [StyleFormatCondition](styleformatcondition) 
