---
title: Car
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/chart/
description: "Aspose.Cells Specifica del modello Cloud: Grafico. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
kwords: Excel, Office, Foglio di calcolo, Cloud REST API, Grafico
weight: 50
---
## **grafico**

 Incapsula l'oggetto che rappresenta un singolo grafico Excel.

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Scalabilità automatica| Booleano| VERO| Falso|| Vero se Microsoft Excel ridimensiona un grafico 3D in modo che sia di dimensioni più vicine al grafico 2D equivalente. La proprietà RightAngleAxes deve essere True.|
| Parete di fondo| Classe:Muri| VERO| Falso|| Restituisce un oggetto che rappresenta la parete posteriore di un grafico 3D.|
| CategoriaAsse| Classe: Asse| VERO| Falso|| Ottiene l'asse X del grafico.|
| ChartArea| Classe: ChartArea| VERO| Falso|| Ottiene l'area del grafico nel foglio di lavoro.|
| GraficoDataTable| Classe: ChartDataTable| VERO| Falso|| Rappresenta la tabella dei dati del grafico.|
| Oggetto grafico| Classe:LinkElement| VERO| Falso|| Rappresenta chartShape;|
| ProfonditàPercentuale| Numero intero| VERO| Falso||Rappresenta la profondità di un grafico 3D come percentuale della larghezza del grafico (tra il 20 e il 2000%).|
| Elevazione| Numero intero| VERO| Falso|| Rappresenta l'elevazione della vista della carta 3D, in gradi.|
| AngoloPrimaSlice| Numero intero| VERO| Falso|| Ottiene o imposta l'angolo della prima sezione del grafico a torta o ad anello, in gradi (in senso orario dalla verticale). Si applica solo ai grafici a torta, a torta 3D e ad anello, da 0 a 360.|
| Pavimento| Classe: pavimento| VERO| Falso|| Restituisce un oggetto che rappresenta le pareti di un grafico 3D.|
| GapDepth| Numero intero| VERO| Falso|| Ottiene o imposta la distanza tra le serie di dati in un grafico 3D, come percentuale della larghezza dell'indicatore. Il valore di questa proprietà deve essere compreso tra 0 e 500.|
| Larghezza gap| Numero intero| VERO| Falso|| Restituisce o imposta lo spazio tra i gruppi di barre o colonne, come percentuale della larghezza della barra o della colonna. Il valore di questa proprietà deve essere compreso tra 0 e 500.|
| AltezzaPercentuale| Numero intero| VERO| Falso||Restituisce o imposta l'altezza di un grafico 3D come percentuale della larghezza del grafico (tra il 5 e il 500%).|
| Nascondi pulsanti campo pivot| Booleano| VERO| Falso|| Indica se nascondere i pulsanti del campo del grafico pivot solo quando il grafico è grafico pivot.|
| È 3D| Booleano| VERO| Falso|| Indica se il grafico è un grafico 3D.|
| È rettangolare con angoli| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se l'area del grafico ha gli angoli rettangolari. L'impostazione predefinita è vera.|
| Leggenda| Classe: Leggenda| VERO| Falso|| Ottiene la legenda del grafico.|
| Nome| Corda| VERO| Falso|| Rappresenta il nome del grafico.|
| Serie N| Classe:Articoli di serie| VERO| Falso|| Ottiene una raccolta che rappresenta le serie di dati nel grafico.|
| Impostazione della pagina| Classe:LinkElement| VERO| Falso|| Rappresenta la descrizione dell'impostazione della pagina in questo grafico.|
| Prospettiva| Numero intero| VERO| Falso|| Restituisce o imposta la prospettiva per la vista della carta 3D. Deve essere compreso tra 0 e 100. Questa proprietà viene ignorata se la proprietà RightAngleAxes è True.|
| PivotSource| Corda| VERO| Falso||L'origine sono i dati della tabella pivot. Se PivotSource non è vuoto, il grafico è Grafico pivot.|
| Posizionamento| Corda| VERO| Falso|| Rappresenta il modo in cui il grafico è collegato alle celle sottostanti.|
| Area del grafico| Classe:PlotArea| VERO| Falso|| Ottiene l'area del tracciato del grafico che include le etichette dei segni di graduazione degli assi.|
| PlotEmptyCellsType| Corda| VERO| Falso|| Ottiene e imposta come tracciare le celle vuote.|
| PlotVisibleCells| Booleano| VERO| Falso|| Indica se tracciare solo le celle visibili.|
| Stampadimensione| Corda| VERO| Falso|| Ottiene e imposta la dimensione del grafico stampato.|
| Assi ad angolo retto| Booleano| VERO| Falso|| Vero se gli assi del grafico sono ad angolo retto. Si applica solo ai grafici 3D (eccetto i grafici a colonna 3D e a torta 3D).|
| Angolo di rotazione| Numero intero| VERO| Falso|| Rappresenta la rotazione della vista del grafico 3D (la rotazione dell'area del tracciato attorno all'asse z, in gradi).|
| Secondo asse di categoria| Classe:LinkElement| VERO| Falso|| Ottiene il secondo asse X del grafico.|
| SecondoAsseValore| Classe:LinkElement| VERO| Falso|| Ottiene il secondo asse Y del grafico.|
| SerieAsse| Classe:LinkElement| VERO| Falso|| Ottiene l'asse delle serie del grafico.|
| Forme| Classe:LinkElement| VERO| Falso|| Restituisce tutte le forme di disegno in questo grafico.|
|Mostra tabella dati| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se il grafico visualizza una tabella dati.|
| MostraLegend| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se verrà visualizzata la legenda del grafico. L'impostazione predefinita è vera.|
| Parete laterale| Classe:LinkElement| VERO| Falso|| Restituisce un oggetto che rappresenta la parete laterale di un grafico 3D.|
| Dimensioni con finestra| Booleano| VERO| Falso|| Vero se Microsoft Excel ridimensiona il grafico in modo che corrisponda alla dimensione della finestra del foglio grafico.|
| Stile| Numero intero| VERO| Falso|| Ottiene e imposta lo stile incorporato.|
| Titolo| Classe:LinkElement| VERO| Falso|| Rappresenta il titolo del grafico.|
| Tipo| Corda| VERO| Falso|| Rappresenta il tipo di grafico.|
| Assevalore| Classe: Asse| VERO| Falso|| Ottiene l'asse Y del grafico.|
| Muri| Classe:LinkElement| VERO| Falso|| Restituisce un oggetto che rappresenta le pareti di un grafico 3D.|
| MuriEGriglia2D| Booleano| VERO| Falso|| Vero se le linee della griglia vengono disegnate bidimensionalmente su un grafico 3D.|
| collegamento| Classe: collegamento| VERO| Falso|||

**Nome del genitore** : [Elemento di collegamento](/specification/model/linkelement)

