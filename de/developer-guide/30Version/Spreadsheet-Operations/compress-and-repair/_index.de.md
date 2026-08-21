---
title: "Excel-Dateien komprimieren und reparieren"
second_title: "Dokument"
type: docs
url: /de/compress-and-repair-excel-files/
linktitle: "Komprimieren und Reparieren"
keywords: "Aspose.Cells, Excel-Komprimierung, Excel-Reparatur, Cloud-API, Excel-Dateigröße reduzieren, beschädigte Arbeitsmappe wiederherstellen, Excel-Datei komprimieren, Excel-Arbeitsmappe reparieren"
description: "Erfahren Sie, wie Sie große Excel-Arbeitsmappen komprimieren und beschädigte Dateien mit der Aspose.Cells Cloud-API reparieren können. Schritt-für-Schritt-Beispiele, unterstützte Sprachen und Best Practices."
weight: 100
ArticleTitle: "Excel-Dateien komprimieren und reparieren – Aspose.Cells Cloud-API"
---

Das Komprimieren einer Excel-Arbeitsmappe reduziert ihre Dateigröße, indem ungenutzte Formatvorlagen, Bilder und gemeinsam genutzte Zeichenfolgen entfernt werden, während die Reparatur die Integrität beschädigter Arbeitsmappen wiederherstellt. Die Aspose.Cells Cloud-API stellt dafür spezielle Endpunkte bereit.

- **[Daten in einer Excel-Datei komprimieren](https://docs.aspose.cloud/cells/compress-excel-files/)**
- **[Excel-Dateien reparieren](https://docs.aspose.cloud/cells/repair-excel-files/)**

**Compress Workbook API (Arbeitsmappe komprimieren)**  
Der **Compress**-Vorgang verwendet eine einfache POST-Anfrage. Nachfolgend finden Sie die vollständige Anfrage-/Antwort-Spezifikation:

| Methode | Endpunkt | Erforderliche Parameter | Anforderungstext | Beispiel-Antwort | Typische Statuscodes |
|--------|----------|------------------------|------------------|------------------|----------------------|
| POST   | `/cells/compress` | `file` (binär) – die zu komprimierende Arbeitsmappe; optional `outPath` (Zeichenkette) – Zielpfad | *Keine* (Datei wird als multipart/form‑data gesendet) | `{ "compressedSize": 12456, "originalSize": 45678 }` | `200 OK`, `400 Bad Request`, `401 Unauthorized` |

**Repair Workbook API (Arbeitsmappe reparieren)**  
Auch der **Repair**-Vorgang verwendet eine POST-Anfrage. Die Spezifikation lautet:

| Methode | Endpunkt | Erforderliche Parameter | Anforderungstext | Beispiel-Antwort | Typische Statuscodes |
|--------|----------|------------------------|------------------|------------------|----------------------|
| POST   | `/cells/repair` | `file` (binär) – die beschädigte Arbeitsmappe; optional `outPath` (Zeichenkette) – Speicherort der reparierten Datei | *Keine* (Datei wird als multipart/form‑data gesendet) | `{ "isRepaired": true, "message": "Workbook repaired successfully." }` | `200 OK`, `400 Bad Request`, `415 Unsupported Media Type` |

Diese Tabellen liefern Entwicklern die wesentlichen Informationen, um die APIs direkt aufzurufen, ohne andere Quellen durchsuchen zu müssen.

**Zusätzliche Ressourcen**  
- Lesen Sie den vollständigen Leitfaden **[Excel-Dateien komprimieren](/compress-excel-files/)** für erweiterte Optionen wie das Entfernen ungenutzter Zeilen und Spalten.  
- Überprüfen Sie die Dokumentation **[Excel-Dateien reparieren](/repair-excel-files/)** für Tipps zur Fehlerbehebung und Erklärungen zu Fehlercodes.  
- Erforschen Sie verwandte Vorgänge wie **[Dateiinformationen abrufen](/file-info/)** und **[Tabellenkalkulationsoperationen](/spreadsheet-operations/)**, um ein umfassenderes Verständnis der Aspose.Cells Cloud-API zu erlangen.