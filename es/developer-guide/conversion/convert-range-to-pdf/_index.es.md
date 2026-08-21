---
title: "Convertir un rango de Excel a PDF con la API de Aspose.Cells Cloud"
second_title: "Documentos"
ArticleTitle: "Cómo convertir datos de rango de una hoja de cálculo local a un archivo PDF: Guía paso a paso"
linktitle: "Convertir rango a PDF"
type: docs
url: /es/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, convertir rango de Excel a PDF, Excel a PDF, conversión en la nube"
description: "Convierte un rango específico de una hoja de cálculo local de Excel a PDF mediante la API REST de Aspose.Cells Cloud."
weight: 100
---

Exporta un rango de datos desde un archivo local de Excel a un archivo [PDF](https://docs.fileformat.com/pdf/) utilizando la API en la nube.

**Requisitos previos**: Antes de utilizar esta API, necesitas una cuenta válida de Aspose.Cells Cloud, un token de acceso JWT y opcionalmente un SDK de Aspose.Cells Cloud para tu lenguaje de programación. Asegúrate de que el almacenamiento de destino (predeterminado o personalizado) esté configurado si planeas usar el parámetro `outStorageName`.

## **API Convertir rango a PDF**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                   |
| -------------------- | ------ | --------------------------------------- | ----------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                                | Carga el archivo de hoja de cálculo.                                          |
| worksheet            | String | Query                                   | Nombre de la hoja dentro de la hoja de cálculo.                              |
| range                | String | Query                                   | Área de celdas a convertir, por ejemplo, A1:C10.                             |
| outPath              | String | Query                                   | (Opcional) Ruta de carpeta donde se guarda el libro. El valor predeterminado es null. |
| outStorageName       | String | Query                                   | Nombre del almacenamiento del archivo de salida.                             |
| fontsLocation        | String | Query                                   | Ubicación para almacenar fuentes personalizadas para uso personal.           |
| region               | String | Query                                   | Configuración de la región de la hoja de cálculo.                            |
| password             | String | Query                                   | Contraseña para abrir el archivo de hoja de cálculo.                          |

### **Respuesta**

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

_La respuesta típica es un flujo binario PDF devuelto como descarga de archivo._

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                     |
| 413    | Carga demasiado grande   | El archivo subido excede el límite de tamaño.                    |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                |

## **¿Dónde debes utilizar la API Convertir rango a PDF?**

- **Estados financieros**: Convierte balances, estados de resultados (rangos específicos) a PDF para documentación lista para auditoría.
- **Informes de ventas**: Transforma paneles de control de ventas o cálculos de comisiones en PDF para distribución.
- **Métricas operativas**: Exporta tablas de KPI y métricas de desempeño como informes formales en PDF.
- **Datos contractuales**: Exporta tablas de precios y acuerdos de nivel de servicio desde hojas de cálculo a PDF como archivos adjuntos.
- **Registros de auditoría**: Preserva rangos de datos financieros como pruebas PDF no editables.
- **Resúmenes de cartera**: Exporta rangos de rendimiento de inversiones como estados de cuenta en PDF listos para clientes.
- **Informes de control de calidad**: Exporta rangos de datos de inspección a PDF para registros de cumplimiento.
- **Resúmenes de inventario**: Transforma tablas de niveles de existencias a PDF para revisión por parte de la dirección.

## ¿Por qué debes utilizar la API Convertir rango a PDF?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación completa. En comparación con la creación de soluciones personalizadas de renderizado de gráficos, esto reduce significativamente la carga de desarrollo.
- **Rentable**: Puedes convertir datos de rango sin necesidad de cargar primero todo el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- **Preserva el formato complejo de Excel** en un formato PDF universalmente accesible.

## ¿Cómo utilizar la API Convertir rango a PDF con los SDK?

### Especificación de la API Convertir rango a PDF

La [Especificación de la API Convertir rango a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

Puedes utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Sheet1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/path/to/file.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndote convertir un rango de datos a un archivo PDF con código conciso. Consulta el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}