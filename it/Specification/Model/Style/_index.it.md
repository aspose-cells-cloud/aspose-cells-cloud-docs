---
title: Stile
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/style/
description: "Aspose.Cells Specifica modello Cloud: Stile. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Stile
weight: 50
---
## **stile**

 Rappresenta lo stile di visualizzazione del documento Excel, come carattere, colore, allineamento, bordo, ecc. L'oggetto Style contiene tutti gli attributi di stile (carattere, formato numero, allineamento e così via) come proprietà.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Font| Classe: carattere| VERO| Falso|| Ottiene un oggetto.|
| Nome| Corda| VERO| Falso|| Ottiene o imposta il nome dello stile.|
| CulturaCustom| Corda| VERO| Falso|| Ottiene e imposta la stringa di modello dipendente dalle impostazioni cultura per il formato numerico. Se per questo oggetto non è stato impostato alcun formato numerico, verrà restituito null. Se il formato numerico è incorporato, verrà restituita la stringa del modello corrispondente al numero incorporato.|
| Costume| Corda| VERO| Falso|| Rappresenta la stringa di formato numero personalizzato di questo oggetto di stile. Se il formato numero personalizzato non è impostato (ad esempio, il formato numero è integrato), verrà restituito "".|
| Colore di sfondo| Classe: colore| VERO| Falso|| Ottiene o imposta il colore di sfondo di uno stile.|
| Colore di primo piano| Classe: colore| VERO| Falso|| Ottiene o imposta il colore di primo piano di uno stile.|
| La formula è nascosta| Booleano| VERO| Falso||Indica se la formula verrà nascosta quando il foglio di lavoro sarà protetto.|
| IsDateTime| Booleano| VERO| Falso|| Indica se il formato numero è un formato data.|
| IsTextWrapped| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se il testo all'interno di una cella va a capo.|
| ÈGradiente| Booleano| VERO| Falso|| Indica se l'ombreggiatura della cella è un modello sfumato.|
| È bloccato| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se una cella può essere modificata o meno.|
| È percentuale| Booleano| VERO| Falso|| Indica se il formato numero è un formato percentuale.|
| Rimpicciolirsi per starci dentro| Booleano| VERO| Falso|| Rappresenta se il testo si riduce automaticamente per adattarsi alla larghezza della colonna disponibile.|
| Livello di rientro| Numero intero| VERO| Falso|| Rappresenta il livello di rientro per la cella o l'intervallo. Può essere solo un numero intero compreso tra 0 e 250.|
| Numero| Numero intero| VERO| Falso|| Ottiene o imposta il formato di visualizzazione di numeri e date. I modelli di formattazione sono diversi per le diverse regioni.|
| Angolo di rotazione| Numero intero| VERO| Falso|| Rappresenta l'angolo di rotazione del testo.|
| Modello| Corda| VERO| Falso|| Ottiene o imposta il tipo di motivo di sfondo della cella.|
| DirezioneTesto| Corda| VERO| Falso|| Rappresenta l'ordine di lettura del testo.|
| Allineamento verticale| Corda| VERO| Falso||Ottiene o imposta il tipo di allineamento verticale del testo in una cella.|
| Allineamento orizzontale| Corda| VERO| Falso|| Ottiene o imposta il tipo di allineamento orizzontale del testo in una cella.|
| Collezione Border| Contenitore| VERO| Falso|||
| BackgroundThemeColor| Classe: TemaColore| VERO| Falso|| Ottiene e imposta il colore del tema di sfondo.|
| PrimopianoTemaColore| Classe: TemaColore| VERO| Falso|| Ottiene e imposta il colore del tema di primo piano.|

