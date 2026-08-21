---
title: "Aspose.Cells Cloud Web API: Eliminar automáticamente filas en blanco/vacías"
second_title: "Documento"
ArticleTitle: "Cómo eliminar todas las filas en blanco/vacías en Excel: Guía completa para limpieza de datos"
linktitle: "Eliminar filas en blanco"
type: docs
url: /es/delete-spreadsheet-blank-rows/
keywords: "Aspose.Cells, Excel, filas en blanco, eliminar filas, limpieza de hojas de cálculo, API"
description: "Elimine todas las filas vacías de archivos de Excel mediante la API de Aspose.Cells Cloud. Rápida, lista para procesamiento por lotes y totalmente programable: vea ejemplos de código en C#, Java, Python y más."
weight: 100
---

Elimine automáticamente todas las filas en blanco de hojas de cálculo de Excel mediante la API de Aspose.Cells Cloud. Nuestra API inteligente detecta y elimina filas que no contienen datos, fórmulas, comentarios u objetos, preservando todo demás contenido. Admite procesamiento por lotes, automatización en la nube e integración fluida para flujos de trabajo empresariales de limpieza de datos.

## API DeleteSpreadsheetBlankRows

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-rows
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```


### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                    |
| -------------------- | ------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData  | El archivo de Excel (`.xlsx`, `.xls`, `.ods`, etc.) que se procesará.                                                                         |
| outPath              | String | Query     | (Opcional) Directorio de destino en su almacenamiento en la nube para el libro limpio. Si se omite, el archivo se guarda junto al archivo original. |
| outStorageName       | String | Query     | Nombre del almacenamiento en la nube configurado (por ejemplo, `MyDropbox`, `CorporateOneDrive`). Obligatorio si desea que la salida se guarde en un almacenamiento específico. |
| region               | String | Query     | Configuración regional (por ejemplo, `es-ES`, `fr-FR`) aplicada durante el procesamiento.                                                     |
| password             | String | Query     | Contraseña para abrir una hoja de cálculo cifrada. Omita si el archivo no está protegido.                                                       |

**Autenticación**  
Todas las llamadas deben incluir el encabezado `Authorization: Bearer <access_token>`. Obtenga el token de acceso mediante el flujo OAuth2 de Aspose Cloud, descrito en la guía de autenticación.

**Requisitos previos y notas**  
- Asegúrese de que su almacenamiento de Aspose Cloud esté configurado y de que el libro original ya esté cargado antes de invocar la API.  
- Los formatos de archivo admitidos incluyen `.xlsx`, `.xls`, `.ods` y otros tipos comunes de hojas de cálculo.  
- El tamaño máximo de archivo por solicitud es de 150 MB; los archivos más grandes deben procesarse en fragmentos.  

### Respuesta

La API devuelve un array JSON que contiene una referencia al archivo procesado.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Códigos de error

- **400 Bad Request (Solicitud incorrecta)**: URI inválido para la API de Aspose.Cells Cloud.
- **401 Unauthorized (No autorizado)**: Token de acceso o credenciales de cliente inválidos.
- **404 Not Found (No encontrado)**: No se puede acceder al archivo de hoja de cálculo.
- **500 Server Error (Error del servidor)**: Ocurrió un error inesperado durante el procesamiento del archivo.

## ¿Dónde debe utilizarse la API para eliminar filas en blanco de hojas de cálculo?

- **Flujos de trabajo de importación y limpieza de datos**: Limpie filas en blanco finales o estructurales inmediatamente después de importar datos desde archivos CSV, bases de datos o API web.
- **Generación de informes y paneles**: Asegure un diseño profesional eliminando filas vacías innecesarias antes de finalizar informes financieros, de ventas u operativos.
- **Preparación de datos para análisis (ETL)**: Preprocese datos de Excel en pipelines ETL antes de cargarlos en almacenes de datos (Snowflake, BigQuery) o herramientas de BI (Tableau, Power BI).
- **Integración de sistemas y feeds API**: Normalice archivos de Excel recibidos desde sistemas de socios, CRM o ERP eliminando filas no utilizadas.
- **Automatización de documentos y procesamiento por lotes**: Elimine filas de marcador de posición generadas por motores de plantillas antes de distribuirlas.
- **Procesamiento de contenido generado por usuarios**: Estandarice cargas de Excel desde portales web o aplicaciones antes de su procesamiento o almacenamiento adicional.
- **Migración de datos heredados**: Simplifique archivos antiguos de hojas de cálculo eliminando filas históricamente vacías o de marcador de posición.

## ¿Por qué debería utilizar la API para eliminar filas en blanco de hojas de cálculo?

- **Amigable para desarrolladores**: Los SDK están disponibles para múltiples lenguajes, reduciendo el esfuerzo de desarrollo comparado con la creación de soluciones personalizadas.
- **Reducción de costos laborales**: Elimina la necesidad de limpieza manual de hojas de cálculo o personal dedicado.
- **Pago por uso**: Solo paga por las llamadas a la API que realmente realice.
- **Costos cero de mantenimiento**: Sin servidores que administrar, sin actualizaciones de software ni preocupaciones por compatibilidad.

## Cómo utilizar la API para eliminar filas en blanco de hojas de cálculo con SDK

### Especificación de la API Delete Spreadsheet Blank Rows

La [Especificación de la API Delete Spreadsheet Blank Rows](https://reference.aspose.cloud/cells/#/TransformController/DeleteSpreadsheetBlankRows) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que oculta los detalles de bajo nivel y le permite eliminar filas en blanco de hojas de cálculo con código breve.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}  
{{<tab tabNum="1" >}}  
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankRows.cs" >}}  
{{</tab>}}  
{{<tab tabNum="2" >}}  
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankRows.java" >}}  
{{</tab>}}  
{{<tab tabNum="3" >}}  
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankRows.php" >}}  
{{</tab>}}  
{{<tab tabNum="4" >}}  
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankRows.rb" >}}  
{{</tab>}}  
{{<tab tabNum="5" >}}  
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankRows.ts" >}}  
{{</tab>}}  
{{<tab tabNum="6" >}}  
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankRows.py" >}}  
{{</tab>}}  
{{<tab tabNum="7" >}}  
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankRows.pl" >}}  
{{</tab>}}  
{{<tab tabNum="8" >}}  
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankRows.go" >}}  
{{</tab>}}  
{{< /tabs >}}
---