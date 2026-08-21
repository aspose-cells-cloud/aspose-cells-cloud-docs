---
title: "Aspose.Cells Cloud API: Convertir gráfico de Excel a PDF"
second_title: "Documento"
ArticleTitle: "Cómo convertir un gráfico de hoja de cálculo local a un archivo PDF: Guía paso a paso"
linktitle: "Convertir gráfico a PDF"
type: docs
url: /es/convert-chart-to-pdf/
keywords: "Aspose Cells, gráfico, PDF, Excel, conversión, API en la nube"
description: "Exportar gráficos desde archivos locales de Excel al formato PDF utilizando la API REST de Aspose.Cells Cloud. Admite archivos XLSX y XLS."
weight: 100
---

Exportar gráficos desde un archivo local de Excel al formato [PDF](https://docs.fileformat.com/pdf/) mediante la API en la nube.

## **Convertir gráfico a PDF: API web**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud:**

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                 |
|----------------------|---------|-----------------------------------------|-----------------------------------------------------------------------------|
| Spreadsheet          | Archivo | FormData                                | Cargar el archivo de hoja de cálculo.                                      |
| worksheet            | Cadena  | Consulta                                | Nombre de la hoja de cálculo que contiene el gráfico.                     |
| chartIndex           | Entero  | Consulta                                | Índice del gráfico que se va a convertir.                                  |
| outPath              | Cadena  | Consulta                                | (Opcional) Ruta de la carpeta donde se almacenará el archivo convertido.  |
| outStorageName       | Cadena  | Consulta                                | Nombre del almacenamiento para el archivo de salida.                       |
| fontsLocation        | Cadena  | Consulta                                | Utilizar fuentes personalizadas si es necesario.                           |
| region             | Cadena  | Consulta                                | Configuración de región de la hoja de cálculo.                             |
| password             | Cadena  | Consulta                                | Contraseña para abrir el archivo de hoja de cálculo.                       |

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

**Códigos de estado HTTP**

| Código | Significado              | Descripción                                                     |
|--------|--------------------------|-----------------------------------------------------------------|
| 200    | Correcto                 | Filtro aplicado correctamente; la respuesta contiene detalles. |
| 400    | Solicitud incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado            | Token JWT inválido o ausente.                                   |
| 413    | Carga demasiado grande   | El archivo cargado excede el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## ¿Dónde debe utilizarse la API Convertir gráfico a PDF?

### **1. Informes empresariales y automatización**

- **Departamentos financieros**: Gráficos de informes financieros mensuales → Archivo en PDF  
- **Equipos de ventas**: Gráficos de tendencias de desempeño → Informes en PDF para clientes  
- **Analítica de marketing**: Gráficos de desempeño de campañas → Resúmenes ejecutivos en PDF  
- **Gestión operativa**: Gráficos de monitoreo de producción → Documentos de cumplimiento en PDF  

### **2. Desarrollo de software e integración**

- **Aplicaciones SaaS**: Datos de gráficos generados por usuarios → Informes descargables en PDF  
- **Sistemas empresariales**: Gráficos de sistemas ERP/CRM → Documentación de auditoría en PDF  
- **Aplicaciones móviles**: Gráficos de analíticas dentro de la app → Archivos PDF compartibles  
- **Aplicaciones web**: Gráficos del panel de control → Funcionalidad de exportación a PDF  

### **3. Flujos de trabajo de procesamiento de documentos**

- **Procesamiento por lotes**: Conversión simultánea de varios gráficos de archivos Excel a PDF  
- **Tareas programadas**: Generación automática diaria/semanal de informes con gráficos  
- **Salidas basadas en plantillas**: Formatos estándar de gráficos → Documentos PDF  
- **Ensamblaje de documentos**: Combinar gráficos con otros contenidos en formato PDF  

### **4. Aplicaciones específicas por industria**

- **Instituciones de investigación**: Gráficos de datos experimentales → Figuras para artículos científicos en PDF  
- **Sector educativo**: Gráficos de materiales educativos → Materiales de curso en PDF  
- **Firmas de consultoría**: Gráficos de análisis → Entregables en PDF para clientes  
- **Industria manufacturera**: Gráficos de control de calidad → Informes de inspección en PDF  
- **Salud**: Gráficos de datos de pacientes → Registros médicos en PDF  
- **Gobierno**: Gráficos estadísticos → Publicaciones oficiales en PDF  

### **5. Gestión y distribución de contenido**

- **Gestión de activos digitales**: Archivado de gráficos en formato PDF estandarizado  
- **Bases de conocimiento**: Documentación técnica con PDF de gráficos incrustados  
- **Portales para clientes**: Entrega segura de informes PDF a partes interesadas  
- **Cumplimiento normativo**: Generación de documentación PDF lista para auditoría  

## ¿Por qué debería utilizar la API Convertir gráfico a PDF?

- Puede convertir gráficos **sin cargar previamente el libro de trabajo**, lo que ahorra espacio de almacenamiento y reduce costos.  
- El desarrollo puede completarse rápidamente mediante los SDK existentes de Aspose.Cells Cloud.  
- **Integración sencilla**: API REST con documentación clara.  
- **Arquitectura escalable**: Maneja cargas de trabajo desde operaciones pequeñas hasta de gran escala empresarial.  

## ¿Cómo utilizar la API Convertir gráfico a PDF con SDK?

### Especificación de la API Convertir gráfico a PDF

La [Especificación de la API Convertir gráfico a PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

## Utilizar SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de desarrollar, ya que abstracta detalles de bajo nivel, permitiéndole convertir un gráfico a un archivo PDF con un código mínimo.  
Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}