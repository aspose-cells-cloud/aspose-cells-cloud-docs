---
title: Trabajar con SaveResult Tas
second_title: Documen
type: docs
url: /es/tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: REST API, task, save result, spreadsheets, exce
description: "Cells.Cloud API para Excel operar: tareas de soporte para guardar el resultado en el contenido de respuesta o almacenamiento en la nube"
weight: 50
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Trabajando con la tarea SaveResult
---
## RESTO API

|**API**|**Tipo**|**Descripción**|**Enlace de recursos**|
|:- |:- |:- |:- |
|/células/tarea/ejecutartarea|CORREO|Ejecutar tarea|[Tarea posterior a la ejecución](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 El[Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) define una interfaz de programación de acceso público y le permite realizar interacciones REST directamente desde un navegador web.

 Puedes utilizar**cURL** Herramienta de línea de comandos para acceder fácilmente a los servicios web Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a Cloud API con cURL.


{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{ <Tasks>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>CloudFileSystem</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet1</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>ImportData</TaskType>\t <ImportDataTaskParameter>\t\t<Workbook>\t\t <FileSourceType>InMemoryFiles</FileSourceType>\t\t <FilePath>TaskBook.xlsx</FilePath>\t\t</Workbook>\t\t<ImportBatchDataOption>\t\t <DestinationWorksheet>Sheet2</DestinationWorksheet>\t\t <IsInsert>true</IsInsert>\t\t <Source>\t\t\t<FileSourceType>RequestFiles</FileSourceType>\t\t\t<FilePath>Batch_data_xml_2.txt</FilePath>\t\t </Source>\t\t</ImportBatchDataOption>\t </ImportDataTaskParameter>\t</TaskDescription>\t<TaskDescription>\t <TaskType>SaveResult</TaskType>\t <SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t <DestinationType>CloudFileSystem</DestinationType>\t\t <InputFile>TaskBook.xlsx</InputFile>\t\t <OutputFile>ImpDataBook.xlsx</OutputFile>\t\t</ResultDestination>\t </SaveResultTaskParameter>\t</TaskDescription> </Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="Java" >}}

{{< tab tabNum="1" >}}
```java

var xml = @"

<TaskData>

  <Tasks>

    <TaskDescription>

      <TaskType>Convert</TaskType>

      <ConvertTaskParameter>

        <Workbook>

          <FileSourceType>CloudFileSystem</FileSourceType>

          <FilePath>Source.xlsx</FilePath>

        </Workbook>

        <DestinationFile>Temp.tiff</DestinationFile>

        <ImageSaveOptions>

          <HorizontalResolution>200</HorizontalResolution>

          <OnePagePerSheet>true</OnePagePerSheet>

          <VerticalResolution>100</VerticalResolution>

        </ImageSaveOptions>

      </ConvertTaskParameter>

    </TaskDescription>

    <TaskDescription>

      <TaskType>SaveResult</TaskType>

      <SaveResultTaskParameter>

        <ResultSource>InMemoryFiles</ResultSource>

        <ResultDestination>

          <DestinationType>OutputStream</DestinationType>

          <InputFile>Temp.tiff</InputFile>

          <OutputFile>Output.tiff</OutputFile>

        </ResultDestination>

      </SaveResultTaskParameter>

    </TaskDescription>

  </Tasks>

</TaskData>

";

ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))

{

    if (response.StatusCode == HttpStatusCode.OK)

    {

        System.Console.WriteLine("OK");

        Stream st = response.GetResponseStream();

        FileStream fs = new FileStream("Output.tiff", FileMode.OpenOrCreate);

        st.CopyTo(fs);

    }

}


```
{{< /tab >}}

{{< /tabs >}}
