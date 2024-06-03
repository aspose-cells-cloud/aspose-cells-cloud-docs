---
title: Arbeitsmappeneinstellung
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/workbooksettings/
description: "Aspose.Cells Cloud-Modellspezifikation: WorkbookSettings. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, WorkbookSettings
weight: 50
---
## **Arbeitsmappeneinstellungen**

 Stellt alle Einstellungen der Arbeitsmappe dar.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Bilder automatisch komprimieren| Boolescher Wert| WAHR| FALSCH||Gibt einen Booleschen Wert an, der angibt, dass die Anwendung die Bilder in der Arbeitsmappe automatisch komprimiert hat.|
| AutoWiederherstellen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Datei zur automatischen Wiederherstellung markiert ist.|
| BuildVersion| Zeichenfolge| WAHR| FALSCH|| Gibt die inkrementelle öffentliche Version der Anwendung an.|
| Berechnungsmodus| Zeichenfolge| WAHR| FALSCH|| Es gibt an, ob Formeln mit Ausnahme mehrerer Tabellenoperationen manuell, automatisch oder automatisch berechnet werden sollen.|
| Berechnungs-ID| Zeichenfolge| WAHR| FALSCH|| Gibt die Version der Berechnungs-Engine an, die zum Berechnen von Werten in der Arbeitsmappe verwendet wird.|
| Kompatibilität prüfen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Speichern der Arbeitsmappe die Kompatibilität überprüft wird. Hinweise: Der Standardwert ist „true“.|
| CheckExcelRestriction| Boolescher Wert| WAHR| FALSCH||Ob die Einschränkung der Excel-Datei überprüft wird, wenn der Benutzer zellenbezogene Objekte ändert. Beispielsweise erlaubt Excel keine Eingabe von Zeichenfolgenwerten, die länger als 32 KB sind. Wenn Sie einen Wert eingeben, der länger als 32 KB ist, z. B. mit Cell.PutValue(string), und diese Eigenschaft auf „true“ gesetzt ist, erhalten Sie eine Ausnahme. Wenn diese Eigenschaft auf „false“ gesetzt ist, akzeptieren wir Ihren eingegebenen Zeichenfolgenwert als Zellenwert, sodass Sie später den vollständigen Zeichenfolgenwert für andere Dateiformate wie CSV ausgeben können. Wenn Sie jedoch einen Wert festgelegt haben, der für das Excel-Dateiformat ungültig ist, sollten Sie die Arbeitsmappe später nicht im Excel-Dateiformat speichern. Andernfalls kann es zu unerwarteten Fehlern bei der generierten Excel-Datei kommen.|
| Absturz speichern| Boolescher Wert| WAHR| FALSCH|| gibt an, ob die Anwendung die Arbeitsmappendatei nach einem Absturz zuletzt gespeichert hat.|
| Kalkulationskette erstellen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob eine Kette berechneter Formeln erstellt wird. Der Standardwert ist „false“.|
| DatenextraktionLaden| Boolescher Wert| WAHR| FALSCH||gibt an, ob die Anwendung die Arbeitsmappe zuletzt zur Datenwiederherstellung geöffnet hat.|
| Datum1904| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Arbeitsmappe das Datumssystem von 1904 verwendet.|
| AnzeigeZeichnungsobjekte| Zeichenfolge| WAHR| FALSCH|| Gibt an, ob und wie Objekte in der Arbeitsmappe angezeigt werden.|
| Makros aktivieren| Boolescher Wert| WAHR| FALSCH|| Makros aktivieren;|
| Erstes sichtbares Tab| Ganze Zahl| WAHR| FALSCH|| Ruft die erste sichtbare Arbeitsblattregisterkarte ab oder legt sie fest.|
| PivotFeldListeAusblenden| Boolescher Wert| WAHR| FALSCH|| Ruft ab und legt fest, ob die Feldliste für die PivotTable ausgeblendet wird.|
| Ist standardmäßig verschlüsselt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Arbeitsmappe mit dem Standardkennwort verschlüsselt wird, wenn Struktur und Windows der Arbeitsmappe gesperrt sind.|
| Ist versteckt| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob diese Arbeitsmappe ausgeblendet ist.|
| Ist die Scrollleiste sichtbar?| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die generierte Tabelle eine horizontale Bildlaufleiste enthält.|
| IstMinimiert| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die generierte Tabelle minimiert geöffnet wird.|
| IstVScrollBarSichtbar?| Boolescher Wert| WAHR| FALSCH||Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die generierte Tabelle eine vertikale Bildlaufleiste enthält.|
| Wiederholung| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die iterative Berechnung zum Auflösen von Zirkelbezügen aktiviert wird.|
| Sprachcode| Zeichenfolge| WAHR| FALSCH|| Ruft die Benutzeroberflächensprache der Arbeitsmappenversion basierend auf dem Ländercode ab, in dem die Datei gespeichert ist, oder legt diese fest.|
| MaxÄnderung| Schwimmend| WAHR| FALSCH|| Gibt die maximale Anzahl von Änderungen zum Auflösen eines Zirkelverweises zurück oder legt sie fest.|
| MaxIteration| Ganze Zahl| WAHR| FALSCH|| Gibt die maximale Anzahl von Iterationen zum Auflösen eines Zirkelverweises zurück oder legt sie fest.|
| Speichereinstellung| Zeichenfolge| WAHR| FALSCH|| Ruft die Speichernutzungsoptionen ab oder legt sie fest. Die neue Option wird als Standardoption für neu erstellte Arbeitsblätter verwendet, hat jedoch keine Auswirkung auf vorhandene Arbeitsblätter.|
| ZahlDezimalTrennzeichen| Zeichenfolge| WAHR| FALSCH|| Ruft das Dezimaltrennzeichen zum Formatieren/Analysieren numerischer Werte ab oder legt es fest. Standardmäßig wird das Dezimaltrennzeichen der aktuellen Region verwendet.|
| Nummerngruppentrennzeichen| Zeichenfolge| WAHR| FALSCH|| Ruft das Zeichen ab oder legt es fest, das Zifferngruppen links vom Dezimaltrennzeichen in numerischen Werten trennt. Standardmäßig wird das Gruppentrennzeichen der aktuellen Region verwendet.|
| ParsingFormulaOnOpen| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Formel beim Lesen der Datei analysiert wird.|
| Angezeigte Präzision| Boolescher Wert| WAHR| FALSCH|| True, wenn Berechnungen in dieser Arbeitsmappe nur mit der Genauigkeit der angezeigten Zahlen durchgeführt werden.|
| Vor dem Speichern neu berechnen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob vor dem Speichern des Dokuments eine Neuberechnung durchgeführt werden soll.|
| Beim Öffnen neu berechnen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Öffnen der Datei alle Formeln neu berechnet werden sollen.|
| EmpfehlenReadOnly| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Option „Nur Lesen empfohlen“ ausgewählt ist.|
| Region| Zeichenfolge| WAHR| FALSCH|| Ruft die regionalen Einstellungen für die Arbeitsmappe ab oder legt sie fest.|
| Persönliche Informationen entfernen| Boolescher Wert| WAHR| FALSCH|| Wahr, wenn persönliche Informationen aus der angegebenen Arbeitsmappe entfernt werden können.|
| ReparaturLaden| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Anwendung die Arbeitsmappe zuletzt im abgesicherten Modus oder im Reparaturmodus geöffnet hat.|
| Geteilt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Arbeitsmappe freigegeben ist.|
| Blattregisterkartenbalkenbreite| Ganze Zahl| WAHR| FALSCH|| Breite der Arbeitsblattregisterkartenleiste (in 1/1000 der Fensterbreite).|
| Tabs anzeigen| Boolescher Wert| WAHR| FALSCH||Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die Arbeitsmappenregisterkarten angezeigt werden.|
| AktualisierenderRahmenAngrenzenderZellen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob die Grenzen benachbarter Zellen aktualisiert werden sollen.|
| Linktyp aktualisieren| Zeichenfolge| WAHR| FALSCH|| Ruft ab und legt fest, wie externe Links beim Öffnen der Arbeitsmappe aktualisiert werden.|
| Fensterhöhe| Schwimmend| WAHR| FALSCH|| Die Höhe des Fensters in Punkteinheiten.|
| Fenster links| Schwimmend| WAHR| FALSCH|| Der Abstand vom linken Rand des Clientbereichs zum linken Rand des Fensters in Punkten.|
| FensterTop| Schwimmend| WAHR| FALSCH|| Der Abstand von der oberen Kante des Clientbereichs zur oberen Kante des Fensters in Punkteinheiten.|
| Fensterbreite| Schwimmend| WAHR| FALSCH|| Die Breite des Fensters in Punkten.|
| Autor| Zeichenfolge| WAHR| FALSCH|| Ruft den Autor der Datei ab und legt ihn fest.|
| CheckCustomNumberFormat| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Festlegen von Style.Custom das benutzerdefinierte Zahlenformat überprüft wird.|
| Schutztyp| Zeichenfolge| WAHR| FALSCH|| Ruft den Schutztyp der Arbeitsmappe ab.|
| Globalisierungseinstellungen| Klasse:Globalisierungseinstellungen| WAHR| FALSCH|| Ruft die Globalisierungseinstellungen ab und legt sie fest.|
| Passwort| Zeichenfolge| WAHR| FALSCH||Stellt das Kennwort zur Arbeitsmappendateiverschlüsselung dar.|
| Schreibschutz| Klasse:Schreibschutz| WAHR| FALSCH|| Bietet Zugriff auf die Schreibschutzoptionen der Arbeitsmappe.|
| Ist verschlüsselt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob zum Öffnen dieser Arbeitsmappe ein Kennwort erforderlich ist.|
| Ist geschützt| Boolescher Wert| WAHR| FALSCH|| Ruft einen Wert ab, der angibt, ob die Struktur oder das Fenster der Arbeitsmappe geschützt ist.|
| MaxRow| Ganze Zahl| WAHR| FALSCH|| Ruft den maximalen Zeilenindex ab, nullbasiert.|
| MaxSpalte| Ganze Zahl| WAHR| FALSCH|| Ruft den maximalen Spaltenindex ab, nullbasiert.|
| Wichtige Ziffer| Ganze Zahl| WAHR| FALSCH|| Ruft die Anzahl der signifikanten Ziffern ab und legt sie fest. Der Standardwert ist .|
| Kompatibilität prüfen| Boolescher Wert| WAHR| FALSCH|| Gibt an, ob beim Speichern der Arbeitsmappe die Kompatibilität mit früheren Versionen überprüft wird.|
| Papier größe| Zeichenfolge| WAHR| FALSCH|| Ruft die Standardpapiergröße für den Druck ab und legt sie fest.|
| MaxZeilenGemeinsameFormel| Ganze Zahl| WAHR| FALSCH|| Ruft die maximale Zeilenanzahl der gemeinsam genutzten Formel ab und legt sie fest.|
| Einhaltung| Zeichenfolge| WAHR| FALSCH|| Gibt die OOXML-Version für das Ausgabedokument an. Der Standardwert ist Ecma376_2006.|
| ZitatPräfixZuStil| Boolescher Wert| WAHR| FALSCH||Gibt an, ob die Eigenschaft beim Eingeben des Zeichenfolgenwerts (der mit einem einfachen Anführungszeichen beginnt) in die Zelle festgelegt wird|
| Formeleinstellungen| Klasse:Formeleinstellungen| WAHR| FALSCH|| Ruft die Einstellungen für formelbezogene Funktionen ab.|
| Volle Berechnung erzwingen| Boolescher Wert| WAHR| FALSCH|| Führt jedes Mal eine vollständige Berechnung durch, wenn eine Berechnung ausgelöst wird.|

