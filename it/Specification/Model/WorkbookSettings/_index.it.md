---
title: Impostazione cartella di lavoro
second_title: Aspose.Cells Cloud Documen
type: docs
url: /it/specification/model/workbooksettings/
description: "Aspose.Cells Specifica del modello cloud: WorkbookSettings. Gestisci facilmente Excel e altri fogli di calcolo con funzionalità come apertura, generazione, modifica, divisione, unione, confronto e conversione"
weight: 50
---
## **workbookSettings**

 

| Nome della proprietà| Tipo di proprietà| Nullabile| Sola lettura| Valore di default| Descrizione|
|:- |:- |:- |:- |:- |:- |
| Compressione automatica delle immagini| Booleano| VERO| Falso|| Specifica un valore booleano che indica le immagini compresse automaticamente dall'applicazione nella cartella di lavoro.|
| Ripristino automatico| Booleano| VERO| Falso|| Indica se il file è contrassegnato per il ripristino automatico.|
| BuildVersion| Corda| VERO| Falso|| Specifica la versione pubblica incrementale dell'applicazione.|
| ModalitàCalc| Corda| VERO| Falso||Specifica se calcolare le formule manualmente, automaticamente o automaticamente ad eccezione di più operazioni su tabelle.|
| ID calcolo| Corda| VERO| Falso|| Specifica la versione del motore di calcolo utilizzato per calcolare i valori nella cartella di lavoro.|
| ControllaComptibilità| Booleano| VERO| Falso|| Indica se verificare la compatibilità durante il salvataggio della cartella di lavoro. Osservazioni: il valore predefinito è true.|
| CheckExcelRestrizione| Booleano| VERO| Falso||Se controllare la restrizione del file Excel quando l'utente modifica gli oggetti correlati alle celle. Ad esempio, Excel non consente l'immissione di valori di stringa più lunghi di 32K. Quando inserisci un valore più lungo di 32 KB come Cell.PutValue(string), se questa proprietà è vera, otterrai un'eccezione. Se questa proprietà è false, accetteremo il valore della stringa di input come valore della cella in modo che in seguito potrai restituire il valore della stringa completo per altri formati di file come CSV. Tuttavia, se hai impostato un tipo di valore che non è valido per il formato di file Excel, non dovresti salvare la cartella di lavoro come formato di file Excel in un secondo momento. Altrimenti potrebbe esserci un errore imprevisto per il file Excel generato.|
| CrashSave| Booleano| VERO| Falso|| indica se l'applicazione ha salvato l'ultima volta il file della cartella di lavoro dopo un arresto anomalo.|
| CreaCalcChain| Booleano| VERO| Falso|| Se crea una catena di formule calcolate. L'impostazione predefinita è falsa.|
| DataExtractLoad| Booleano| VERO| Falso||indica se l'applicazione ha aperto l'ultima volta la cartella di lavoro per il ripristino dei dati.|
| Data1904| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se la cartella di lavoro utilizza il sistema di data 1904.|
| VisualizzaDrawingObjects| Corda| VERO| Falso|| Indica se e come mostrare gli oggetti nella cartella di lavoro.|
| AbilitaMacro| Booleano| VERO| Falso|| Abilita macro;|
| Prima scheda visibile| Numero intero| VERO| Falso|| Ottiene o imposta la prima scheda visibile del foglio di lavoro.|
| Nascondi elenco campi pivot| Booleano| VERO| Falso|| Ottiene e imposta se nascondere l'elenco dei campi per la tabella pivot.|
| IsDefaultEncrypted| Booleano| VERO| Falso|| Indica se crittografare la cartella di lavoro con password predefinita se Struttura e Windows della cartella di lavoro sono bloccati.|
| È nascosto| Booleano| VERO| Falso|| Indica se questa cartella di lavoro è nascosta.|
| IsHScrollBarVisible| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se il foglio di calcolo generato conterrà una barra di scorrimento orizzontale.|
| È ridotto al minimo| Booleano| VERO| Falso|| Indica se il foglio di calcolo generato verrà aperto ridotto a icona.|
| IsVScrollBarVisible| Booleano| VERO| Falso||Ottiene o imposta un valore che indica se il foglio di calcolo generato conterrà una barra di scorrimento verticale.|
| Iterazione| Booleano| VERO| Falso|| Indica se abilitare il calcolo iterativo per risolvere i riferimenti circolari.|
| Codice lingua| Corda| VERO| Falso|| Ottiene o imposta la lingua dell'interfaccia utente della versione Workbook in base al CountryCode che ha salvato il file.|
| MaxChange| Galleggiante| VERO| Falso|| Restituisce o imposta il numero massimo di modifiche per risolvere un riferimento circolare.|
| MaxIterazione| Numero intero| VERO| Falso|| Restituisce o imposta il numero massimo di iterazioni per risolvere un riferimento circolare.|
| Impostazione memoria| Corda| VERO| Falso|| Ottiene o imposta le opzioni di utilizzo della memoria. La nuova opzione verrà presa come opzione predefinita per i fogli di lavoro appena creati ma non avrà effetto per i fogli di lavoro esistenti.|
| NumberDecimalSeparator| Corda| VERO| Falso|| Ottiene o imposta il separatore decimale per la formattazione/analisi dei valori numerici. L'impostazione predefinita è il separatore decimale della regione corrente.|
| NumberGroupSeparator| Corda| VERO| Falso|| Ottiene o imposta il carattere che separa i gruppi di cifre a sinistra del decimale nei valori numerici. L'impostazione predefinita è il separatore di gruppo della regione corrente.|
| Analisi FormulaOnOpen| Booleano| VERO| Falso||Indica se si sta analizzando la formula durante la lettura del file.|
| Precisione come visualizzata| Booleano| VERO| Falso|| Vero se i calcoli in questa cartella di lavoro verranno eseguiti utilizzando solo la precisione dei numeri così come vengono visualizzati|
| Ricalcola prima di salvare| Booleano| VERO| Falso|| Indica se ricalcolare prima di salvare il documento.|
| Ricalcolaall'apertura| Booleano| VERO| Falso|| Indica se ricalcolare tutte le formule all'apertura del file.|
| Consiglia sola lettura| Booleano| VERO| Falso|| Indica se è selezionata l'opzione Consigliata di sola lettura.|
| Regione| Corda| VERO| Falso|| Ottiene o imposta le impostazioni internazionali per la cartella di lavoro.|
| Rimuovi informazioni personali| Booleano| VERO| Falso|| Vero se le informazioni personali possono essere rimosse dalla cartella di lavoro specificata.|
| RepairLoad| Booleano| VERO| Falso|| Indica se l'applicazione ha aperto l'ultima volta la cartella di lavoro in modalità provvisoria o di ripristino.|
| Condiviso| Booleano| VERO| Falso|| Ottiene o imposta un valore che indica se la cartella di lavoro è condivisa.|
| SheetTabBarWidth| Numero intero| VERO| Falso|| Larghezza della barra delle schede del foglio di lavoro (in 1/1000 della larghezza della finestra).|
| Mostra schede| Booleano| VERO| Falso||Ottiene o imposta un valore se vengono visualizzate le schede della cartella di lavoro.|
| Aggiorna bordo celle adiacenti| Booleano| VERO| Falso|| Indica se aggiornare il bordo delle celle adiacenti.|
| UpdateLinksType| Corda| VERO| Falso|| Ottiene e imposta la modalità di aggiornamento dei collegamenti esterni all'apertura della cartella di lavoro.|
| Altezza finestra| Galleggiante| VERO| Falso|| L'altezza della finestra, in unità di punto.|
| Finestra sinistra| Galleggiante| VERO| Falso|| La distanza dal bordo sinistro dell'area client al bordo sinistro della finestra, in unità di punto.|
| Finestra in alto| Galleggiante| VERO| Falso|| La distanza dal bordo superiore dell'area client al bordo superiore della finestra, in unità di punto.|
| Larghezza finestra| Galleggiante| VERO| Falso|| La larghezza della finestra, in unità di punto.|
| Autore| Corda| VERO| Falso|| Ottiene e imposta l'autore del file.|
| ControllaCustomNumberFormat| Booleano| VERO| Falso|| Indica se controllare il formato del numero personalizzato durante l'impostazione di Style.Custom.|
| Tipo di protezione| Corda| VERO| Falso|| Ottiene il tipo di protezione della cartella di lavoro.|
| Impostazioni di globalizzazione| Classe: Impostazioni globalizzazione| VERO| Falso|| Ottiene e imposta le impostazioni di globalizzazione.|
| Parola d'ordine| Corda| VERO| Falso||Rappresenta la password di crittografia dei file della cartella di lavoro.|
| WriteProtection| Classe:ProtezioneScrittura| VERO| Falso|| Fornisce l'accesso alle opzioni di protezione da scrittura della cartella di lavoro.|
| È crittografato| Booleano| VERO| Falso|| Ottiene un valore che indica se è necessaria una password per aprire la cartella di lavoro.|
| È protetto| Booleano| VERO| Falso|| Ottiene un valore che indica se la struttura o la finestra della cartella di lavoro è protetta.|
| MaxRow| Numero intero| VERO| Falso|| Ottiene l'indice di riga massimo, in base zero.|
| Colonna massima| Numero intero| VERO| Falso|| Ottiene l'indice massimo della colonna, in base zero.|
| Cifre significative| Numero intero| VERO| Falso|| Ottiene e imposta il numero di cifre significative. Il valore predefinito è .|
| Controlla compatibilità| Booleano| VERO| Falso|| Indica se verificare la compatibilità con le versioni precedenti durante il salvataggio della cartella di lavoro.|
| Dimensioni del foglio| Corda| VERO| Falso|| Ottiene e imposta il formato carta di stampa predefinito.|
| MaxRowsOfSharedFormula| Numero intero| VERO| Falso|| Ottiene e imposta il numero massimo di righe della formula condivisa.|
| Conformità| Corda| VERO| Falso|| Specifica la versione OOXML per il documento di output. Il valore predefinito è Ecma376_2006.|
| QuotePrefixToStyle| Booleano| VERO| Falso||Indica se impostare la proprietà quando si immette il valore della stringa (che inizia con virgolette singole) nella cella|
| Impostazioni formula| Classe:Impostazioni formula| VERO| Falso|| Ottiene le impostazioni per le funzionalità correlate alla formula.|
| ForceFullCalculate| Booleano| VERO| Falso|| Calcola completamente ogni volta che viene attivato un calcolo.|

