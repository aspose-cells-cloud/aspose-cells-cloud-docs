---
title: "Convertir rango de Excel a CSV – Aspose.Cells Cloud API"
second_title: "Documentos"
ArticleTitle: "Cómo convertir un rango local de hoja de cálculo a un archivo CSV: guía paso a paso"
linktitle: "Convertir rango a CSV"
type: docs
url: /convert-range-to-csv/
keywords: "Aspose Cells, convertir rango a CSV, Excel a CSV, API de Excel, hoja de cálculo en la nube, convertir, Excel, CSV, Aspose.Cells, API en la nube"
description: "Aprenda a convertir un rango específico de un libro local de Excel (XLSX o XLS) a CSV mediante la API REST de Aspose.Cells Cloud. Incluye sintaxis de solicitud, parámetros, manejo de errores y ejemplos de SDK."
---

Exporte un rango específico de un archivo local de Excel a CSV mediante la API de Aspose.Cells Cloud.

## **Convertir rango a CSV (API)**

**Requisitos previos**  
Para llamar a este punto de conexión, debe tener un **client ID** y un **client secret** válidos de Aspose Cloud, obtener un **token de acceso JWT** y asegurarse de que la hoja de cálculo de origen esté en formato **XLSX** o **XLS**.

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

**Ejemplo con cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Hoja1&range=A1:C10" \
     -H "Authorization: Bearer {token_de_acceso}" \
     -F "Spreadsheet=@ejemplo.xlsx"
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta/Cadena de consulta/Cuerpo HTTP | Descripción                                                                 |
| :------------------- | :----- | :---------------------------------- | :--------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                            | Cargue el archivo de hoja de cálculo.                                       |
| worksheet            | String | Query                               | Nombre de la hoja de cálculo.                                               |
| range                | String | Query                               | Especifique el rango de celdas (por ejemplo, A1:C10).                      |
| outPath              | String | Query                               | Ruta de la carpeta donde se almacenará el libro (opcional). Valor predeterminado: null. |
| outStorageName       | String | Query                               | Nombre del almacenamiento de salida.                                        |
| fontsLocation        | String | Query                               | Especifique fuentes personalizadas si es necesario.                         |
| region               | String | Query                               | Define la configuración de región de la hoja de cálculo.                    |
| password             | String | Query                               | Contraseña necesaria para abrir el archivo de hoja de cálculo.              |

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

_Ejemplo de contenido CSV devuelto (primeras filas):_

```csv
Nombre,Fecha,Cantidad
Juan Pérez,2023-01-15,1250.00
María López,2023-01-16,980.50
```

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                       |
| ------ | ------------------------ | ----------------------------------------------------------------- |
| 200    | Correcto                 | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta     | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT no válido o ausente.                                    |
| 413    | Carga demasiado grande    | El archivo cargado excede el límite de tamaño.                   |
| 500    | Error interno del servidor | Error inesperado en el servidor.                                 |

## ¿Dónde debe utilizar la API Convert Range to CSV?

### **1. Escenarios de exportación y migración de datos**

- **Integración con bases de datos**: Exporte rangos específicos de Excel directamente a sistemas de bases de datos.
- **Integración con aplicaciones**: Alimente datos seleccionados de la hoja de cálculo a aplicaciones SaaS.
- **Migración de sistemas**: Transfiera rangos de datos específicos entre sistemas heredados y modernos.
- **Interoperabilidad multiplataforma**: Comparta subconjuntos de datos específicos entre distintas plataformas.

### **2. Informes y análisis**

- **Informes dirigidos**: Exporte secciones específicas de informes a CSV para análisis focalizado.
- **Flujos de datos para paneles de control**: Proporcione rangos de datos específicos a herramientas de paneles de BI.
- **Métricas de rendimiento**: Extraiga rangos de indicadores clave para sistemas de seguimiento de rendimiento.
- **Informes financieros**: Exporte secciones de estados financieros para auditorías externas.

### **3. Desarrollo y pruebas**

- **Gestión de datos de prueba**: Exporte rangos de datos específicos para fines de pruebas.
- **Entornos de desarrollo**: Comparta rangos de datos de ejemplo con equipos de desarrollo.
- **Pruebas de API**: Genere datos de prueba en formato CSV a partir de secciones específicas de la hoja de cálculo.
- **Desarrollo de prototipos**: Proporcione conjuntos de datos focalizados para prototipos de aplicaciones.

### **4. Operaciones empresariales**

- **Compartir datos selectivos**: Comparta rangos de datos específicos con socios externos.
- **Copia de seguridad parcial de datos**: Haga copias de seguridad de rangos críticos en formato CSV.
- **Transferencia interdepartamental**: Comparta datos específicos entre departamentos.
- **Informes de cumplimiento**: Exporte rangos de datos regulatorios para presentaciones de cumplimiento.

### **5. Flujos de trabajo automatizados**

- **Exportación programada de rangos**: Exporte automáticamente rangos específicos según un horario.
- **Extracción basada en eventos**: Exporte rangos según eventos o desencadenantes empresariales.
- **Integración en flujos de trabajo**: Integre las exportaciones de rangos en flujos de trabajo de procesos empresariales.
- **Procesamiento por lotes de rangos**: Procese múltiples rangos específicos en operaciones por lotes.

## ¿Por qué debería utilizar la API Convert Range to CSV?

- Puede convertir un rango de hoja de cálculo sin cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.
- El desarrollo puede completarse rápidamente utilizando los SDK existentes de Aspose.Cells Cloud.
- **Integración sencilla**: API REST con documentación clara.
- **Arquitectura escalable**: Maneja operaciones desde pequeñas hasta de escala empresarial.

## ¿Cómo usar la API Convert Range to CSV con SDK?

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCSV) define una API públicamente accesible, lo que permite interacciones REST directamente desde un navegador web.

## Utilice los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstraen los detalles de bajo nivel, permitiéndole convertir un rango de datos a un archivo CSV con un código mínimo.  
Explore la lista completa de SDK de Aspose.Cells Cloud en nuestro [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código ilustran cómo llamar a los servicios web de Aspose.Cells mediante varios SDK. Si la carga desde Gist está bloqueada, puede descargar los ejemplos directamente desde el repositorio.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToCSV.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToCSV.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToCSV.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToCSV.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToCSV.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToCSV.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToCSV.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToCSV.go" >}}
{{</tab>}}
{{< /tabs >}}