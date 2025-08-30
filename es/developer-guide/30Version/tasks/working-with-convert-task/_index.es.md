---
title: Trabajar con Convert Tas
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/tasks/convert/
aliases: [/working-with-convert-task/]
keywords: REST API, task, convert, spreadsheets, exce
description: "Cells.Cloud API para Excel opera: tareas de soporte para convertir archivos de Excel"
weight: 30
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Trabajando con la tarea Convertir
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

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData>\t<Tasks>\t<TaskDescription>\t\t<TaskType>SmartMarker</TaskType>\t\t<SmartMarkerTaskParameter>\t\t<SourceWorkbook>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>Book1.xlsx</FilePath>\t\t</SourceWorkbook>\t\t<DestinationWorkbook>\t\t\t<FileSourceType>InMemoryFiles</FileSourceType>\t\t\t<FilePath>ReportTask.xlsx</FilePath>\t\t</DestinationWorkbook>\t\t<xmlFile>\t\t\t<FileSourceType>CloudFileSystem</FileSourceType>\t\t\t<FilePath>ReportData.xml</FilePath>\t\t</xmlFile>\t\t</SmartMarkerTaskParameter>\t</TaskDescription>\t<TaskDescription>\t\t<TaskType>SaveResult</TaskType>\t\t<SaveResultTaskParameter>\t\t<ResultSource>InMemoryFiles</ResultSource>\t\t<ResultDestination>\t\t\t<DestinationType>OutputStream</DestinationType>\t\t\t<InputFile>ReportTask.xlsx</InputFile>\t\t\t<OutputFile>Output.xlsx</OutputFile>\t\t</ResultDestination>\t\t</SaveResultTaskParameter>\t</TaskDescription>\t</Tasks></TaskData>}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the operation result.

```

{{< /tab >}}

{{< /tabs >}}

 Usar un SDK es la mejor manera de acelerar el desarrollo. Un SDK se encarga de los detalles básicos y te permite concentrarte en las tareas de tu proyecto. Consulta el[repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web Aspose.Cells utilizando varios SDK:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}

```csharp

var xml = @"<TaskData>

                <Tasks>

                <TaskDescription>

                    <TaskType>SmartMarker</TaskType>

                    <SmartMarkerTaskParameter>

                    <SourceWorkbook>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>Book1.xlsx</FilePath>

                    </SourceWorkbook>

                    <DestinationWorkbook>

                        <FileSourceType>InMemoryFiles</FileSourceType>

                        <FilePath>ReportTask.xlsx</FilePath>

                    </DestinationWorkbook>

                    <xmlFile>

                        <FileSourceType>CloudFileSystem</FileSourceType>

                        <FilePath>ReportData.xml</FilePath>

                    </xmlFile>

                    </SmartMarkerTaskParameter>

                </TaskDescription>

                <TaskDescription>

                    <TaskType>SaveResult</TaskType>

                    <SaveResultTaskParameter>

                    <ResultSource>InMemoryFiles</ResultSource>

                    <ResultDestination>

                        <DestinationType>OutputStream</DestinationType>

                        <InputFile>ReportTask.xlsx</InputFile>

                        <OutputFile>Output.xlsx</OutputFile>

                    </ResultDestination>

                    </SaveResultTaskParameter>

                </TaskDescription>

                </Tasks>

            </TaskData>";


ServiceHelper helper = new ServiceHelper(sid, key);

using (HttpWebResponse response = helper.CallPost("http://api.aspose.com/v3.0/cells/task/runtask", xml, "application/xml"))

{

    if (response.StatusCode == HttpStatusCode.OK)

    {

        System.Console.WriteLine("OK");

        Stream st = response.GetResponseStream();

        FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate);

        st.CopyTo(fs);

    }

}//using


```

{{< /tab >}}

{{< /tabs >}}
