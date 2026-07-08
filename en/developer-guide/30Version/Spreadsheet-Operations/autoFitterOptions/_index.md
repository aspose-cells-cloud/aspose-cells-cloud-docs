---
title: "AutoFitterOptions – Properties & Usage Guide | Aspose.Cells Cloud API"
second_title: "Document"
linktitle: "AutoFitterOptions"
type: docs
url: /auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, Excel auto fit, row height, merged cells, API"
description: "Learn how to control row‑height auto‑fitting, merged‑cell handling, hidden rows/columns, language settings, and rendering options with the AutoFitterOptions object in the Aspose.Cells Cloud API."
weight: 79
---

# AutoFitterOptions Properties

The `AutoFitterOptions` object lets you fine‑tune the automatic row‑height adjustment performed by Aspose.Cells Cloud. It is useful when you need precise control over merged‑cell handling, hidden rows/columns, language‑specific formatting, or rendering‑specific behavior.

| Name                       | Type        | Description                                                                                     | Notes                                                                                                       |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Determines how merged cells are auto‑fitted.                                                    | Allowed values: `All`, `First`, `None`. Default: `All`. Sample JSON: `"AutoFitMergedCellsType":"All"`       |
| **IgnoreHidden**           | **boolean** | When **true**, hidden rows and columns are ignored during the auto‑fit process.                 | Default: `false`. Sample JSON: `"IgnoreHidden":false`                                                       |
| **OnlyAuto**               | **boolean** | Indicates whether only rows whose heights are not manually customized should be auto‑fitted.    | Default: `false`. Sample JSON: `"OnlyAuto":false`                                                           |
| **DefaultEditLanguage**    | **string**  | Sets the default editing language for the workbook.                                             | Default: system language (e.g., `"en-US"`). Sample JSON: `"DefaultEditLanguage":"en-US"`                    |
| **MaxRowHeight**           | **double**  | Maximum row height (in points) applied when auto‑fitting rows. A value of **0** means no limit. | Default: `0`. Sample JSON: `"MaxRowHeight":0`                                                               |
| **AutoFitWrappedTextType** | **string**  | Controls how wrapped text within cells is auto‑fitted.                                          | Allowed values: `All`, `OnlyWrapped`, `None`. Default: `All`. Sample JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Specifies the formatting strategy used during the auto‑fit operation.                           | Common values: `AutoFit`, `PreserveExisting`. Default: `AutoFit`. Sample JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Indicates whether the auto‑fit should be performed for rendering purposes (e.g., PDF, image).   | Allowed values: `True`, `False`. Default: `False`. Sample JSON: `"ForRendering":"False"`                    |

Below is a typical JSON payload that can be sent to the API when configuring `AutoFitterOptions`.

```json
{
  "AutoFitMergedCellsType": "All",
  "IgnoreHidden": false,
  "OnlyAuto": false,
  "DefaultEditLanguage": "en-US",
  "MaxRowHeight": 0,
  "AutoFitWrappedTextType": "All",
  "FormatStrategy": "AutoFit",
  "ForRendering": "False"
}
```

A sample `cURL` request that applies these options to a workbook:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Endpoint reference**

| Method | URL | Required Parameters | Description |
|--------|-----|---------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (JSON body) | Applies the specified `AutoFitterOptions` to the target workbook. |
| GET    | `/cells/workbook/autoFitter` | *none* | Retrieves the current `AutoFitterOptions` settings for the workbook. |

Typical response codes:

- **200 OK** – Operation completed successfully.  
- **400 Bad Request** – Invalid JSON payload or unsupported value.  
- **401 Unauthorized** – Missing or invalid authentication token.  
- **500 Internal Server Error** – Unexpected server error.

These examples illustrate how to configure and invoke the `AutoFitterOptions` model within the Aspose.Cells Cloud API.