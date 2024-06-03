---
title: Digitale Signatur
second_title: Aspose.Cells Cloud Documen
type: docs
url: /de/specification/model/digitalsignature/
description: "Aspose.Cells Cloud-Modellspezifikation: DigitalSignature. Müheloses Bearbeiten von Excel und anderen Tabellenkalkulationsdokumenten mit Funktionen wie Öffnen, Generieren, Bearbeiten, Teilen, Zusammenführen, Vergleichen und Konvertieren"
kwords: Excel, Office, Tabellenkalkulation, Cloud REST API, Digitale Signatur
weight: 50
---
## **Digitale Unterschrift**

 Signatur in der Datei.

| Name des Anwesens| Art der Immobilie| Nullwerte zulassen| Schreibgeschützt| Standardwert| Beschreibung|
|:- |:- |:- |:- |:- |:- |
| Kommentare| Zeichenfolge| WAHR| FALSCH|| Der Zweck der Unterschrift.|
| ZeichenZeit| Zeichenfolge| WAHR| FALSCH|| Der Zeitpunkt, zu dem das Dokument unterzeichnet wurde.|
| Ausweis| Zeichenfolge| WAHR| FALSCH|| Gibt eine GUID an, die mit der GUID der im Dokumentinhalt gespeicherten Signaturzeile abgeglichen werden kann. Der Standardwert ist eine leere GUID (alles Nullen).|
| Passwort| Zeichenfolge| WAHR| FALSCH|| Gibt den Text der tatsächlichen Signatur in der digitalen Signatur an. Der Standardwert ist „Leer“.|
| Bild|Anordnung<Byte> | WAHR| FALSCH|| Gibt ein Bild für die digitale Signatur an. Der Standardwert ist null.|
| Anbieter-ID| Zeichenfolge| WAHR| FALSCH|| Gibt die Klassen-ID des Signaturanbieters an. Der Standardwert ist eine leere GUID (alles Nullen).|
| Ist gültig| Boolescher Wert| WAHR| FALSCH|| Wenn diese digitale Signatur gültig ist und das Dokument nicht manipuliert wurde, ist dieser Wert wahr.|
| XAdESTyp| Zeichenfolge| WAHR| FALSCH|| XAdES-Typ. Der Standardwert ist „Keine“ (XAdES ist deaktiviert).|

