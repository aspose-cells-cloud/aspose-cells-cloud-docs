---
title: "SDKs de Aspose.Cells Cloud disponibles"
second_title: "Documento"
ArticleTitle: "SDKs de Aspose.Cells Cloud disponibles: C#, Java, PHP, Python, Ruby, Node.js, Go y Perl"
LinkTitle: "SDKs disponibles"
type: docs
url: /es/available-sdks/
description: "Explore los SDKs de Aspose.Cells Cloud para C#, Java, PHP, Python, Ruby, Node.js, Go y Perl. Desarrolle, convierta y analice archivos de Excel en la nube mediante APIs de bajo coste y multiplataforma."
weight: 30
keywords: "SDKs de Aspose.Cells Cloud, C#, Java, PHP, Python, Ruby, Node.js, Go, Perl, Excel, API en la nube"
---

# **¿Por qué utilizar los SDKs de Aspose.Cells Cloud?**

## **Compatibilidad multiplataforma**

Los SDKs de Aspose.Cells Cloud ofrecen una biblioteca fiable y estable para múltiples lenguajes de desarrollo. Proporcionan un sólido soporte multiplataforma, facilitando la integración en Windows, Linux o macOS.

## **Procesamiento eficiente de archivos de Excel y conjunto de funciones amplio**

Los SDKs de Aspose.Cells Cloud permiten a los desarrolladores trabajar eficientemente con archivos de Excel en la nube, incluyendo lectura, escritura, modificación y conversión, sin necesidad de instalar ningún software local de Office. El SDK ofrece una amplia gama de APIs y funciones para soportar operaciones complejas en Excel, como cálculo de fórmulas, creación de gráficos, formato condicional y mucho más, satisfaciendo necesidades diversas de los desarrolladores.

## **Fácil de integrar**

El SDK proporciona una API concisa y clara que permite a los desarrolladores integrarlo rápidamente en sus proyectos existentes, reduciendo así el tiempo y el coste de desarrollo.

## **Reducción de costes**

El uso de los SDKs de Aspose.Cells Cloud puede reducir los costes operativos de su negocio al evitar la necesidad de adquirir y mantener costosos software o servidores locales de Office.

### Resumen de los SDKs

<table>
<thead>
<tr>
<th>Lenguaje</th>
<th>Versión más reciente</th>
<th>Instalación</th>
<th>Ejemplo de inicio rápido</th>
</tr>
</thead>
<tbody>
<tr>
<td>C#</td>
<td>23.12</td>
<td><code>dotnet add package Aspose.Cells-Cloud</code></td>
<td>
<pre><code class="language-csharp">var api = new CellsApi("clientId", "clientSecret");
var result = api.ConvertSpreadsheet(new ConvertSpreadsheetRequest("sample.xlsx", "pdf"));</code></pre>
</td>
</tr>
<tr>
<td>Java</td>
<td>23.12</td>
<td><code>mvn dependency:copy -Dartifact=aspose:aspose-cells-cloud:23.12</code></td>
<td>
<pre><code class="language-java">CellsApi api = new CellsApi("clientId", "clientSecret");
ConvertSpreadsheetRequest request = new ConvertSpreadsheetRequest();
request.setSpreadsheet("Book1.xlsx");
request.setFormat("pdf");
File result = api.ConvertSpreadsheetRequest(request);</code></pre>
</td>
</tr>
<tr>
<td>PHP</td>
<td>23.12</td>
<td><code>composer require aspose/cells-cloud-sdk</code></td>
<td>
<pre><code class="language-php">$instance = new CellsApi(getenv("CellsCloudClientId"), getenv("CellsCloudClientSecret"));
$convertSpreadsheetRequest = new ConvertSpreadsheetRequest();
$convertSpreadsheetRequest->setSpreadsheet($EmployeeSalesSummaryXlsx);
$convertSpreadsheetRequest->setFormat("pdf");
$instance->convertSpreadsheet($convertSpreadsheetRequest, "export-out1.pdf");</code></pre>
</td>
</tr>
<tr>
<td>Python</td>
<td>23.12</td>
<td><code>pip install aspose-cells-cloud</code></td>
<td>
<pre><code class="language-python">instance = CellsApi(os.getenv('CellsCloudClientId'), os.getenv('CellsCloudClientSecret'))
instance.convert_spreadsheet(ConvertSpreadsheetRequest('EmployeeSalesSummary.xlsx', 'pdf'), local_outpath="EmployeeSalesSummary.pdf")</code></pre>
</td>
</tr>
<tr>
<td>Ruby</td>
<td>23.12</td>
<td><code>gem install aspose_cells_cloud</code></td>
<td>
<pre><code class="language-ruby">@instance = AsposeCellsCloud::CellsApi.new(ENV['CellsCloudClientId'], ENV['CellsCloudClientSecret'])
request = AsposeCellsCloud::ConvertSpreadsheetRequest.new(:Spreadsheet=>'EmployeeSalesSummary.xlsx', :format=>'pdf')
response = @instance.convert_spreadsheet(request)</code></pre>
</td>
</tr>
<tr>
<td>Node.js</td>
<td>23.12</td>
<td><code>npm install asposecellscloud</code></td>
<td>
<pre><code class="language-javascript">const cellsApi = new CellsApi(process.env.CellsCloudClientId, process.env.CellsCloudClientSecret, "v4.0", process.env.CellsCloudApiBaseUrl);
var request = new model.ConvertSpreadsheetRequest();
request.spreadsheet = "Book1.xlsx";
request.format = "pdf";
return cellsApi.convertSpreadsheet(request).then((result) => {
    expect(result.response.statusCode).to.equal(200);
});</code></pre>
</td>
</tr>
<tr>
<td>Go</td>
<td>23.12</td>
<td><code>go get github.com/aspose/cells-cloud-go/v2</code></td>
<td>
<pre><code class="language-go">instance := NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"))
convertedData, httpResponse, err := instance.ConvertSpreadsheet(&amp;ConvertSpreadsheetRequest{Spreadsheet: employeeSalesSummaryXlsx, Format: "pdf"})</code></pre>
</td>
</tr>
</tbody>
</table>

**Requisitos previos** – .NET 6+ / Java 8+ / PHP 7.4+ / Python 3.7+ / Ruby 2.6+ / Node 12+ / Go 1.16+ / Perl 5.30+. También necesita un ID de cliente y un secreto de cliente válidos de Aspose Cloud.

**Ejemplo de solicitud y respuesta de API** – conversión de un libro de Excel a PDF:

```json
{
  "Input": "EmployeeSalesSummary.xlsx",
  "OutputFormat": "pdf"
}
```

Los SDKs son de código abierto y están alojados en GitHub; puede clonarlos o contribuir a ellos:

- C#: https://github.com/aspose-cells-cloud/aspose-cells-cloud-csharp  
- Java: https://github.com/aspose-cells-cloud/aspose-cells-cloud-java  
- PHP: https://github.com/aspose-cells-cloud/aspose-cells-cloud-php  
- Python: https://github.com/aspose-cells-cloud/aspose-cells-cloud-python  
- Ruby: https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby  
- Node.js: https://github.com/aspose-cells-cloud/aspose-cells-cloud-node  
- Go: https://github.com/aspose-cells-cloud/aspose-cells-cloud-go  
- Perl: https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl  

En resumen, el uso de los SDKs de Aspose.Cells Cloud aporta múltiples beneficios: compatibilidad multiplataforma, manejo eficiente de archivos de Excel, conjunto de funciones amplio, protección de seguridad y privacidad, alta escalabilidad, fácil integración, soporte y documentación comunitaria, y reducción de costes. Estas ventajas convierten a los SDKs en una opción ideal para desarrolladores que trabajan con archivos de Excel.

# **Escenarios de aplicación**

## **Automatización del procesamiento de hojas de cálculo**

- Mediante los SDKs de Aspose.Cells Cloud, los desarrolladores pueden escribir scripts de automatización para procesar por lotes archivos de hojas de cálculo como Excel.  
- Las tareas automatizadas pueden incluir importación/exportación de datos, formateo, cálculos de fórmulas, generación de gráficos y más.

## **Procesamiento y análisis de datos en la nube**

- Con el servicio Aspose.Cells en la nube, se pueden procesar grandes volúmenes de datos en hojas de cálculo sin consumir recursos informáticos locales.  
- Es ideal para escenarios que requieren análisis complejos de datos, minería de datos o generación de informes.

## **Compatibilidad multiplataforma**

- Debido a su naturaleza multiplataforma, los SDKs de Aspose.Cells Cloud facilitan la implementación del procesamiento de hojas de cálculo en distintos sistemas operativos y arquitecturas.  
- Es especialmente adecuado para escenarios que requieren soporte en múltiples entornos, como back‑ends de aplicaciones web, aplicaciones de escritorio y back‑ends de aplicaciones móviles.

## **Integraciones y extensiones de APIs**

- Los SDKs de Aspose.Cells Cloud pueden integrarse en APIs existentes, proporcionando capacidades de procesamiento de hojas de cálculo como parte del servicio.  
- Es adecuado para construir aplicaciones empresariales, plataformas SaaS o prestar servicios mediante APIs.

## **Colaboración y compartir documentos**

- Con los SDKs de Aspose.Cells Cloud, se puede habilitar la edición colaborativa en línea de hojas de cálculo por múltiples usuarios.  
- Los usuarios pueden editar, comentar y compartir archivos de hojas de cálculo en tiempo real en la nube, mejorando así la colaboración en equipo.

## **Migración y transformación de datos**

- Cuando se necesita migrar datos desde otros formatos o sistemas, los SDKs de Aspose.Cells Cloud pueden actuar como puente para la transformación de datos.  
- Los datos de otros formatos pueden convertirse a formato Excel para su análisis y procesamiento posteriores.

## **Generación automática de informes**

- Mediante la ejecución periódica de scripts, se pueden generar automáticamente informes o paneles de control periódicos con los SDKs de Aspose.Cells Cloud.  
- Esto resulta útil para organizaciones que necesitan monitorear métricas empresariales, datos de ventas o datos financieros de forma regular.

## **Integración en procesos CI/CD**

- Integre los SDKs de Aspose.Cells Cloud en sus procesos de integración y despliegue continuos (CI/CD) para automatizar la verificación de la corrección de los datos en hojas de cálculo.  
- Esto ayuda a garantizar que los cambios de código no comprometan la integridad ni el formateo de los datos en la hoja de cálculo.

## **Aplicaciones personalizadas de hojas de cálculo**

- Con los SDKs de Aspose.Cells Cloud, puede desarrollar aplicaciones personalizadas de hojas de cálculo para satisfacer necesidades empresariales específicas.  
- Por ejemplo, crear aplicaciones personalizadas para procesamiento de formularios, herramientas de gestión de datos financieros, etc.

# **Ventajas de los SDKs**

Nuestros SDKs están 100 % probados y listos para ejecutarse fuera de la caja. Son de código abierto y se distribuyen bajo la licencia MIT, por lo que puede utilizarlos y personalizarlos completamente de forma gratuita.
---