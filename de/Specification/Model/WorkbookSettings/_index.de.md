---
title: Arbeitsmappeneinstellung
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/workbooksettings/
description: "Aspose.Cells Cloud-Modellspezifikation: WorkbookSettings. Bearbeiten Sie mühelos Excel und andere Tabellenkalkulationsdokumente mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
weight: 50
---
## **Arbeitsmappeneinstellungen**

 

| Name des Anwesens| Art der Immobilie| Nullbar| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Bilder automatisch komprimieren| Boolescher Wert| WAHR| FALSCH|| Gibt einen booleschen Wert an, der angibt, dass die Anwendung automatisch komprimierte Bilder in der Arbeitsmappe enthält.|
| Automatische Wiederherstellung| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Datei für die automatische Wiederherstellung markiert ist.|
| BuildVersion| Zeichenfolge| WAHR| FALSCH|| Gibt die inkrementelle öffentliche Veröffentlichung der Anwendung an.|
| Berechnungsmodus| Zeichenfolge| WAHR| FALSCH||Es gibt an, ob Formeln manuell, automatisch oder automatisch berechnet werden sollen, mit Ausnahme mehrerer Tabellenoperationen.|
| Berechnungs-ID| Zeichenfolge| WAHR| FALSCH|| Gibt die Version der Berechnungs-Engine an, die zum Berechnen von Werten in der Arbeitsmappe verwendet wird.|
| Kompatibilität prüfen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Speichern der Arbeitsmappe die Kompatibilität überprüft wird. Anmerkungen: Der Standardwert ist true.|
| CheckExcelRestriction| Boolescher Wert| WAHR| FALSCH||Ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert. Excel erlaubt beispielsweise keine Eingabe von Zeichenfolgenwerten, die länger als 32 KB sind. Wenn Sie einen Wert eingeben, der länger als 32 KB ist, z. B. durch Cell.PutValue(string), erhalten Sie eine Ausnahme, wenn diese Eigenschaft wahr ist. Wenn diese Eigenschaft „false“ ist, akzeptieren wir Ihren eingegebenen Zeichenfolgenwert als Zellwert, sodass Sie später den vollständigen Zeichenfolgenwert für andere Dateiformate wie CSV ausgeben können. Wenn Sie jedoch einen Wert festgelegt haben, der für das Excel-Dateiformat ungültig ist, sollten Sie die Arbeitsmappe später nicht im Excel-Dateiformat speichern. Andernfalls kann es zu einem unerwarteten Fehler in der generierten Excel-Datei kommen.|
| CrashSave| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Anwendung die Arbeitsmappendatei zuletzt nach einem Absturz gespeichert hat.|
| CreateCalcChain| Boolescher Wert| WAHR| FALSCH|| Ob eine Kette berechneter Formeln erstellt wird. Der Standardwert ist falsch.|
| DataExtractLoad| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Anwendung die Arbeitsmappe zuletzt zur Datenwiederherstellung geöffnet hat.|
| Datum 1904| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt diesen fest, der angibt, ob die Arbeitsmappe das Datumssystem 1904 verwendet.|
| DisplayDrawingObjects| Zeichenfolge| WAHR| FALSCH|| Gibt an, ob und wie Objekte in der Arbeitsmappe angezeigt werden.|
| Makros aktivieren| Boolescher Wert| WAHR| FALSCH|| Makros aktivieren;|
| FirstVisibleTab| Ganze Zahl| WAHR| FALSCH|| Ruft die erste sichtbare Arbeitsblattregisterkarte ab oder legt sie fest.|
| PivotFieldList ausblenden| Boolescher Wert| WAHR| FALSCH|| Ruft ab und legt fest, ob die Feldliste für die PivotTable ausgeblendet wird.|
| IsDefaultEncrypted| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Arbeitsmappe mit dem Standardkennwort verschlüsselt wird, wenn Struktur und Windows der Arbeitsmappe gesperrt sind.|
| Ist versteckt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Arbeitsmappe ausgeblendet ist.|
| IsHScrollBarVisible| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob die generierte Tabelle eine horizontale Bildlaufleiste enthält, oder legt diesen fest.|
| IstMinimiert| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die generierte Tabelle minimiert geöffnet wird.|
| IsVScrollBarVisible| Boolescher Wert| WAHR| FALSCH||Ruft einen Wert ab, der angibt, ob die generierte Tabelle eine vertikale Bildlaufleiste enthält, oder legt diesen fest.|
| Wiederholung| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die iterative Berechnung zum Auflösen von Zirkelverweisen aktiviert ist.|
| Sprachcode| Zeichenfolge| WAHR| FALSCH|| Ruft die Benutzeroberflächensprache der Arbeitsmappenversion basierend auf dem CountryCode ab, der die Datei gespeichert hat, oder legt diese fest.|
| MaxChange| Schwebend| WAHR| FALSCH|| Gibt die maximale Anzahl von Änderungen zum Auflösen eines Zirkelverweises zurück oder legt diese fest.|
| MaxIteration| Ganze Zahl| WAHR| FALSCH|| Gibt die maximale Anzahl von Iterationen zum Auflösen eines Zirkelverweises zurück oder legt diese fest.|
| Speichereinstellung| Zeichenfolge| WAHR| FALSCH|| Ruft die Speichernutzungsoptionen ab oder legt diese fest. Die neue Option wird als Standardoption für neu erstellte Arbeitsblätter übernommen, hat jedoch keine Auswirkungen auf vorhandene Arbeitsblätter.|
| NumberDecimalSeparator| Zeichenfolge| WAHR| FALSCH|| Ruft das Dezimaltrennzeichen für die Formatierung/Analyse numerischer Werte ab oder legt dieses fest. Standard ist das Dezimaltrennzeichen der aktuellen Region.|
| NumberGroupSeparator| Zeichenfolge| WAHR| FALSCH|| Ruft das Zeichen ab, das in numerischen Werten Gruppen von Ziffern links von der Dezimalstelle trennt, oder legt dieses fest. Standard ist das Gruppentrennzeichen der aktuellen Region.|
| ParsingFormulaOnOpen| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Formel beim Lesen der Datei analysiert wird.|
| PrecisionAsDisplayed| Boolescher Wert| WAHR| FALSCH|| True, wenn Berechnungen in dieser Arbeitsmappe nur mit der Genauigkeit der angezeigten Zahlen durchgeführt werden|
| Neu berechnenBeforeSave| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob vor dem Speichern des Dokuments eine Neuberechnung durchgeführt werden soll.|
| ReCalculateOnOpen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob alle Formeln beim Öffnen der Datei neu berechnet werden.|
| RecommendReadOnly| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Option „Schreibgeschützt empfohlen“ ausgewählt ist.|
| Region| Zeichenfolge| WAHR| FALSCH|| Ruft die regionalen Einstellungen für die Arbeitsmappe ab oder legt diese fest.|
| Persönliche Informationen entfernen| Boolescher Wert| WAHR| FALSCH|| True, wenn persönliche Informationen aus der angegebenen Arbeitsmappe entfernt werden können.|
| RepairLoad| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Anwendung die Arbeitsmappe zuletzt im abgesicherten Modus oder im Reparaturmodus geöffnet hat.|
| Geteilt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob die Arbeitsmappe freigegeben ist, oder legt diesen fest.|
| SheetTabBarWidth| Ganze Zahl| WAHR| FALSCH|| Breite der Registerkartenleiste des Arbeitsblatts (in 1/1000 der Fensterbreite).|
| Tabs anzeigen| Boolescher Wert| WAHR| FALSCH||Ruft einen Wert ab, ob die Arbeitsmappenregisterkarten angezeigt werden, oder legt diesen fest.|
| UpdateAdjacentCellsBorder| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob der Rand benachbarter Zellen aktualisiert wird.|
| UpdateLinksType| Zeichenfolge| WAHR| FALSCH|| Ruft ab und legt fest, wie externe Links aktualisiert werden, wenn die Arbeitsmappe geöffnet wird.|
| Fensterhöhe| Schwebend| WAHR| FALSCH|| Die Höhe des Fensters in der Einheit Punkt.|
| FensterLinks| Schwebend| WAHR| FALSCH|| Der Abstand vom linken Rand des Clientbereichs zum linken Rand des Fensters in Punkteinheiten.|
| WindowTop| Schwebend| WAHR| FALSCH|| Der Abstand vom oberen Rand des Clientbereichs zum oberen Rand des Fensters in Punkteinheiten.|
| Fensterbreite| Schwebend| WAHR| FALSCH|| Die Breite des Fensters in Punkteinheiten.|
| Autor| Zeichenfolge| WAHR| FALSCH|| Ruft den Autor der Datei ab und legt ihn fest.|
| CheckCustomNumberFormat| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Festlegen von Style.Custom das benutzerdefinierte Zahlenformat überprüft wird.|
| Schutztyp| Zeichenfolge| WAHR| FALSCH|| Ruft den Schutztyp der Arbeitsmappe ab.|
| Globalisierungseinstellungen| Klasse:GlobalizationSettings| WAHR| FALSCH|| Ruft die Globalisierungseinstellungen ab und legt sie fest.|
| Passwort| Zeichenfolge| WAHR| FALSCH||Stellt das Verschlüsselungskennwort für die Arbeitsmappendatei dar.|
| Schreibschutz| Klasse:WriteProtection| WAHR| FALSCH|| Bietet Zugriff auf die Schreibschutzoptionen der Arbeitsmappe.|
| IsEncrypted| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob zum Öffnen dieser Arbeitsmappe ein Kennwort erforderlich ist.|
| Ist geschützt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob die Struktur oder das Fenster der Arbeitsmappe geschützt ist.|
| MaxRow| Ganze Zahl| WAHR| FALSCH|| Ruft den maximalen Zeilenindex nullbasiert ab.|
| MaxColumn| Ganze Zahl| WAHR| FALSCH|| Ruft den maximalen Spaltenindex nullbasiert ab.|
| Wichtige Ziffer| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der signifikanten Ziffern ab und legt sie fest. Der Standardwert ist .|
| Überprüfen Sie die Kompatibilität| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Speichern der Arbeitsmappe die Kompatibilität mit früheren Versionen überprüft werden soll.|
| Papier größe| Zeichenfolge| WAHR| FALSCH|| Ruft das Standarddruckpapierformat ab und legt es fest.|
| MaxRowsOfSharedFormula| Ganze Zahl| WAHR| FALSCH|| Ruft die maximale Zeilenanzahl der gemeinsam genutzten Formel ab und legt diese fest.|
| Einhaltung| Zeichenfolge| WAHR| FALSCH|| Gibt die OOXML-Version für das Ausgabedokument an. Der Standardwert ist Ecma376_2006.|
| QuotePrefixToStyle| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Eigenschaft festgelegt wird, wenn der Zeichenfolgewert (der mit einem einfachen Anführungszeichen beginnt) in die Zelle eingegeben wird|
| Formeleinstellungen| Klasse:FormulaSettings| WAHR| FALSCH|| Ruft die Einstellungen für formelbezogene Funktionen ab.|
| ForceFullCalculate| Boolescher Wert| WAHR| FALSCH|| Führt jedes Mal eine vollständige Berechnung durch, wenn eine Berechnung ausgelöst wird.|

