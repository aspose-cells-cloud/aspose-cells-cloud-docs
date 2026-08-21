---
title: "AutoFitterOptions – Eigenschaften & Gebrauchsanleitung | Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "AutoFitterOptions"
type: docs
url: /de/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel automatische Anpassung, Zeilenhöhe, verbundene Zellen, API"
description: "Erfahren Sie, wie Sie die automatische Anpassung der Zeilenhöhe, die Behandlung verbundener Zellen, ausgeblendete Zeilen/Spalten, sprachspezifische Formatierungen und renderungsspezifische Verhalten mit dem AutoFitterOptions-Objekt in der Aspose.Cells Cloud API steuern können."
weight: 79
ArticleTitle: "AutoFitterOptions – Eigenschaften & Gebrauchsanleitung für Aspose.Cells Cloud"
---

# AutoFitterOptions-Eigenschaften

Das `AutoFitterOptions`-Objekt ermöglicht es Ihnen, die automatische Anpassung der Zeilenhöhe durch Aspose.Cells Cloud fein abzustimmen. Es ist nützlich, wenn Sie präzise Kontrolle über die Behandlung verbundener Zellen, ausgeblendeter Zeilen/Spalten, sprachspezifischer Formatierung oder renderungsspezifischer Verhalten benötigen.

**Voraussetzungen** – Um diese Optionen nutzen zu können, müssen Sie mit einem gültigen OAuth 2.0-Zugriffstoken authentifiziert sein, das den Bereich **Cells.ReadWrite** umfasst. Die Anfrage funktioniert mit jeder SDK-Version, die die v3.0-API unterstützt.

| Name                       | Typ         | Beschreibung                                                                                      | Hinweise                                                                                                       |
| -------------------------- | ----------- | ------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Legt fest, wie verbundene Zellen automatisch angepasst werden.                                   | Zulässige Werte: `All`, `First`, `None`. Standardwert: `All`. Beispiel-JSON: `"AutoFitMergedCellsType":"All"`  |
| **IgnoreHidden**           | **boolean** | Wenn **true**, werden ausgeblendete Zeilen und Spalten während des automatischen Anpassungsvorgangs ignoriert. | Standardwert: `false`. Beispiel-JSON: `"IgnoreHidden":false`                                                   |
| **OnlyAuto**               | **boolean** | Gibt an, ob nur Zeilen mit nicht manuell angepasster Höhe automatisch angepasst werden sollen.    | Standardwert: `false`. Beispiel-JSON: `"OnlyAuto":false`                                                       |
| **DefaultEditLanguage**    | **string**  | Legt die Standardsprache für die Bearbeitung der Arbeitsmappe fest.                              | Standardwert: Systemsprache (z. B. `"de-DE"`). Beispiel-JSON: `"DefaultEditLanguage":"de-DE"`                   |
| **MaxRowHeight**           | **double**  | Maximale Zeilenhöhe (in Punkten), die bei der automatischen Anpassung angewendet wird. Ein Wert von **0** bedeutet keine Begrenzung. | Standardwert: `0`. Beispiel-JSON: `"MaxRowHeight":0`                                                           |
| **AutoFitWrappedTextType** | **string**  | Steuert, wie umgebrochener Text innerhalb von Zellen automatisch angepasst wird.                 | Zulässige Werte: `All`, `OnlyWrapped`, `None`. Standardwert: `All`. Beispiel-JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Gibt die Formatierungsstrategie an, die während des automatischen Anpassungsvorgangs verwendet wird. | Typische Werte: `AutoFit`, `PreserveExisting`. Standardwert: `AutoFit`. Beispiel-JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Gibt an, ob die automatische Anpassung für Rendierungszwecke (z. B. PDF, Bild) durchgeführt werden soll. | Zulässige Werte: `True`, `False`. Standardwert: `False`. Beispiel-JSON: `"ForRendering":"False"`                |

Im Folgenden finden Sie eine typische JSON-Payload, die an die API gesendet werden kann, um `AutoFitterOptions` zu konfigurieren.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "de-DE",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Ein Beispiel für eine `cURL`-Anfrage, die diese Optionen auf eine Arbeitsmappe anwendet:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Referenz zur API-Endpunkt**

| Methode | URL | Erforderliche Parameter | Beschreibung |
|--------|-----|------------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (JSON-Body) | Wendet die angegebenen `AutoFitterOptions` auf die Zielarbeitsmappe an. |
| GET    | `/cells/workbook/autoFitter` | *keine* | Ruft die aktuellen `AutoFitterOptions`-Einstellungen für die Arbeitsmappe ab. |

**Anforderungsparameter für den PUT-Endpunkt**

| Parameter                | Typ     | Erforderlich | Beschreibung |
|--------------------------|---------|--------------|-------------|
| AutoFitMergedCellsType   | string  | Ja           | Wie verbundene Zellen automatisch angepasst werden (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | Nein         | Ob ausgeblendete Zeilen/Spalten ignoriert werden. |
| OnlyAuto                 | boolean | Nein         | Nur Zeilen ohne manuelle Höheneinstellungen anpassen. |
| DefaultEditLanguage      | string  | Nein         | Bearbeitungssprache (z. B. `de-DE`). |
| MaxRowHeight             | double  | Nein         | Maximale Zeilenhöhe in Punkten; `0` = unbegrenzt. |
| AutoFitWrappedTextType   | string  | Nein         | Wie umgebrochener Text behandelt wird (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | Nein         | Formatierungsstrategie (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | Nein         | Automatische Anpassung für Rendierung anwenden (`True`, `False`). |

Typische Antwortcodes:

- **200 OK** – Vorgang erfolgreich abgeschlossen.  
- **400 Bad Request** – Ungültige JSON-Payload oder nicht unterstützter Wert.  
- **401 Unauthorized** – Fehlender oder ungültiger Authentifizierungstoken.  
- **500 Internal Server Error** – Unerwarteter Serverfehler.

**Beispiel für eine GET-Antwort**

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "de-DE",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

Diese Beispiele veranschaulichen, wie das `AutoFitterOptions`-Modell innerhalb der Aspose.Cells Cloud API konfiguriert und aufgerufen wird.