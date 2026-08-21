---
title: "Aspose.Cells Cloud Web API – Traducir hoja de cálculo al idioma de destino"
second_title: "Documento"
ArticleTitle: "Cómo traducir una hoja de cálculo completa utilizando la API de traducción por IA de Aspose.Cells Cloud"
linktitle: "Traducir hoja de cálculo"
type: docs
url: /translate-spreadsheet/
keywords: "Aspose.Cells Cloud, API de traducción de hojas de cálculo, traducción por IA, traducción de hojas de cálculo, targetLanguage, traducción multi-hoja, procesamiento en la nube de hojas de cálculo, traducción de Aspose.Cells Cloud"
description: "Traduzca un libro de Excel completo con Aspose.Cells Cloud por IA. Preserva fórmulas, gráficos y formato al convertir el texto a cualquier idioma admitido. Aprenda sobre el punto final, los parámetros, ejemplos de SDK, límites y manejo de errores."
weight: 100
---

El punto final **TranslateSpreadsheet**, parte de la **API de traducción de hojas de cálculo**, lee cada elemento de texto en un libro, envía el contenido a un servicio de traducción impulsado por IA y devuelve un nuevo archivo de hoja de cálculo donde todos los datos textuales se presentan en el **targetLanguage** especificado. La operación mantiene intacta la estructura original, los estilos de celda, las fórmulas y **la** estructura multi-hoja, lo que la hace ideal para internacionalizar informes, paneles de control y documentos basados en datos. Los formatos de archivo admitidos incluyen XLS, XLSX, XLSM, CSV y ODS. Se devuelven errores para códigos de idioma inválidos, fallos de autenticación o interrupciones del servicio de traducción.

## **API de traducción de hojas de cálculo**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/spreadsheet
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                                                                                 |
| :------------------- | :----- | :-------- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | Archivo | Obligatorio | FormData             | El libro de Excel que se va a traducir. Las extensiones aceptables: .xls, .xlsx, .xlsm, .csv, .ods. Tamaño máximo del archivo: 50 MB. Ejemplo: `budget.xlsx`.                                               |
| targetLanguage       | string | Obligatorio | Query                | Código de idioma ISO 639‑1 para el idioma de salida deseado (por ejemplo, "es" para español, "fr" para francés, "de" para alemán). Debe ser un idioma admitido por el servicio de IA subyacente.              |
| region               | string | Opcional    | Query                | Identificador de región de la hoja de cálculo que influye en el formato específico de la configuración regional, como fechas, números y monedas. Valores comunes: "US", "EU", "CN". Si se omite, se utiliza la configuración de región original del libro. |
| password             | string | Opcional    | Query                | Contraseña para abrir un libro protegido. Déjelo en blanco si el archivo no está protegido con contraseña.                                                                                                             |

### **Respuesta**

Respuesta correcta (200 OK)  
Encabezados:  
Content‑Type: application/octet-stream // o text/csv cuando se solicita salida en CSV  
Content‑Disposition: attachment; filename="translated.xlsx"  
Content‑Length: <tamaño en bytes>

Cuerpo:  
<flujo binario que contiene el archivo de hoja de cálculo traducido>

Las respuestas de error siguen el modelo estándar de errores de Aspose.Cells Cloud (application/json) con campos `code`, `message` y `details` (opcional).

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros faltantes o inválidos (por ejemplo, tipo de archivo no admitido).      |
| 401    | No autorizado           | Token JWT inválido o faltante.                                     |
| 413    | Carga útil demasiado grande | El archivo subido excede el límite de tamaño.                                 |
| 500    | Error interno del servidor | Error inesperado del servidor.                                          |

## ¿Dónde debemos utilizar la API de traducción de hojas de cálculo?

- **Informes financieros internacionales** – Convertir informes trimestrales en Excel a múltiples idiomas para oficinas regionales, preservando fórmulas y diseños de gráficos.
- **Paneles de control de marketing multilingües** – Generar automáticamente versiones localizadas de paneles de rendimiento de ventas para equipos globales.
- **Distribución de contenido educativo** – Traducir libretas de calificaciones, hojas de tareas u hojas de cálculo curriculares para estudiantes en diferentes países sin necesidad de copiar y pegar manualmente.
- **Cumplimiento normativo** – Generar hojas de cálculo específicas por idioma para cumplimiento normativo, conservando reglas de validación y listas de validación de datos.

## ¿Por qué debería utilizar la API de traducción de hojas de cálculo?

- **Precisión impulsada por IA** – Utiliza modelos avanzados de traducción neuronal para conversiones lingüísticas contextualmente conscientes y de alta calidad.
- **Sin interrupción del diseño** – Mantiene fórmulas de celda, formato condicional, gráficos y orden de hojas de cálculo exactamente como en el archivo original.
- **Procesamiento multi-hoja en una sola llamada** – Traduce todas las hojas de cálculo en una sola solicitud, eliminando la necesidad de bucles por hoja.
- **Integración fluida en la nube** – Funciona con la autenticación de Aspose.Cells Cloud, permitiendo canalizaciones automatizadas en CI/CD, funciones sin servidor o sistemas back-end empresariales.

## Cómo utilizar la API de traducción de hojas de cálculo con SDK

### Especificación de la API de traducción de hojas de cálculo

La [Especificación de la API de traducción de hojas de cálculo](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/TranslateSpreadsheet) proporciona una interfaz de programación accesible públicamente para realizar interacciones REST directamente desde un navegador web.

## SDK de API de Excel

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel, permitiéndole fusionar una hoja de cálculo en otra con un código breve.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateSpreadsheet.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateSpreadsheet.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateSpreadsheet.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateSpreadsheet.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateSpreadsheet.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateSpreadsheet.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateSpreadsheet.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateSpreadsheet.go" >}}  
{{</tab>}}  
{{< /tabs >}}