---
title: "AutoFitterOptions – Guía de propiedades y uso | Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "AutoFitterOptions"
type: docs
url: /es/auto-fitter-options/
keywords: "AutoFitterOptions, Aspose.Cells, ajuste automático de Excel, altura de fila, celdas fusionadas, API"
description: "Aprenda cómo controlar el ajuste automático de la altura de fila, el manejo de celdas fusionadas, filas/columnas ocultas, configuraciones de idioma y opciones de renderizado mediante el objeto AutoFitterOptions en la API de Aspose.Cells Cloud."
weight: 79
ArticleTitle: "AutoFitterOptions – Guía de propiedades y uso para Aspose.Cells Cloud"
---

# Propiedades de AutoFitterOptions

El objeto `AutoFitterOptions` le permite ajustar finamente el ajuste automático de altura de fila realizado por Aspose.Cells Cloud. Es útil cuando necesita un control preciso sobre el manejo de celdas fusionadas, filas/columnas ocultas, formato específico por idioma o comportamiento específico para renderizado.

**Prerrequisitos** – Para usar estas opciones, debe estar autenticado con un token de acceso válido de OAuth 2.0 que incluya el ámbito **Cells.ReadWrite**. La solicitud funciona con cualquier versión del SDK que soporte la API v3.0.

| Nombre                     | Tipo        | Descripción                                                                                     | Notas                                                                                                       |
| -------------------------- | ----------- | ----------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------- |
| **AutoFitMergedCellsType** | **string**  | Determina cómo se ajustan automáticamente las celdas fusionadas.                              | Valores permitidos: `All`, `First`, `None`. Valor predeterminado: `All`. Ejemplo JSON: `"AutoFitMergedCellsType":"All"` |
| **IgnoreHidden**           | **boolean** | Si es **true**, se ignoran las filas y columnas ocultas durante el proceso de ajuste automático. | Valor predeterminado: `false`. Ejemplo JSON: `"IgnoreHidden":false`                                       |
| **OnlyAuto**               | **boolean** | Indica si solo deben ajustarse automáticamente las filas cuya altura no se haya personalizado manualmente. | Valor predeterminado: `false`. Ejemplo JSON: `"OnlyAuto":false`                                           |
| **DefaultEditLanguage**    | **string**  | Establece el idioma de edición predeterminado para el libro de trabajo.                        | Valor predeterminado: idioma del sistema (p. ej., `"es-ES"`). Ejemplo JSON: `"DefaultEditLanguage":"en-US"` |
| **MaxRowHeight**           | **double**  | Altura máxima de fila (en puntos) aplicada al ajustar automáticamente las filas. Un valor de **0** significa sin límite. | Valor predeterminado: `0`. Ejemplo JSON: `"MaxRowHeight":0`                                                |
| **AutoFitWrappedTextType** | **string**  | Controla cómo se ajusta automáticamente el texto ajustado dentro de las celdas.               | Valores permitidos: `All`, `OnlyWrapped`, `None`. Valor predeterminado: `All`. Ejemplo JSON: `"AutoFitWrappedTextType":"All"` |
| **FormatStrategy**         | **string**  | Especifica la estrategia de formato utilizada durante la operación de ajuste automático.      | Valores comunes: `AutoFit`, `PreserveExisting`. Valor predeterminado: `AutoFit`. Ejemplo JSON: `"FormatStrategy":"AutoFit"` |
| **ForRendering**           | **string**  | Indica si el ajuste automático debe realizarse con fines de renderizado (p. ej., PDF, imagen). | Valores permitidos: `True`, `False`. Valor predeterminado: `False`. Ejemplo JSON: `"ForRendering":"False"` |

A continuación se muestra una carga JSON típica que puede enviarse a la API al configurar `AutoFitterOptions`.

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

Una solicitud `cURL` de ejemplo que aplica estas opciones a un libro de trabajo:

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/workbook/autoFitter" \
  -H "Authorization: Bearer {access_token}" \
  -H "Content-Type: application/json" \
  -d @autoFitterOptions.json
```

**Referencia de puntos de conexión**

| Método | URL | Parámetros obligatorios | Descripción |
|--------|-----|-------------------------|-------------|
| PUT    | `/cells/workbook/autoFitter` | `autoFitterOptions` (cuerpo JSON) | Aplica las `AutoFitterOptions` especificadas al libro de trabajo objetivo. |
| GET    | `/cells/workbook/autoFitter` | *ninguno* | Recupera la configuración actual de `AutoFitterOptions` para el libro de trabajo. |

**Parámetros de solicitud para el punto de conexión PUT**

| Parámetro                | Tipo    | Obligatorio | Descripción |
|--------------------------|---------|-------------|-------------|
| AutoFitMergedCellsType   | string  | Sí          | Cómo se ajustan automáticamente las celdas fusionadas (`All`, `First`, `None`). |
| IgnoreHidden             | boolean | No          | Si se ignoran las filas/columnas ocultas. |
| OnlyAuto                 | boolean | No          | Ajustar solo filas sin configuración manual de altura. |
| DefaultEditLanguage      | string  | No          | Idioma de edición (p. ej., `es-ES`). |
| MaxRowHeight             | double  | No          | Altura máxima de fila en puntos; `0` = ilimitado. |
| AutoFitWrappedTextType   | string  | No          | Cómo se maneja el texto ajustado (`All`, `OnlyWrapped`, `None`). |
| FormatStrategy           | string  | No          | Estrategia de formato (`AutoFit`, `PreserveExisting`). |
| ForRendering             | string  | No          | Aplicar ajuste automático para renderizado (`True`, `False`). |

Códigos de respuesta típicos:

- **200 OK** – Operación completada correctamente.  
- **400 Bad Request** – Carga JSON inválida o valor no admitido.  
- **401 Unauthorized** – Token de autenticación ausente o inválido.  
- **500 Internal Server Error** – Error inesperado del servidor.

**Respuesta GET de ejemplo**

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

Estos ejemplos ilustran cómo configurar e invocar el modelo `AutoFitterOptions` dentro de la API de Aspose.Cells Cloud.