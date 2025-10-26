---
title: Trabajar con SmartMarker Tas
type: docs
url: /es/tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: REST API, task, save result, spreadsheets, exce
description: "Cells.Cloud API para Excel opera: soporte de tareas para marcador inteligente"
weight: 60
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Trabajando con SmartMarker Task
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

curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" -H "accept: application/json" -H "Content-Type: application/json" -H "x-aspose-client: Containerize.Swagger" -d "{<TaskData> <Tasks> <TaskDescription> <TaskType>SmartMarker</TaskType> <SmartMarkerTaskParameter> <SourceWorkbook> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>Designer.xlsx</FilePath> </SourceWorkbook> <DestinationWorkbook> <FileSourceType>InMemoryFiles</FileSourceType> <FilePath>Temp.xlsx</FilePath> </DestinationWorkbook> <xmlFile> <FileSourceType>CloudFileSystem</FileSourceType> <FilePath>DataSet.xml</FilePath> </xmlFile> </SmartMarkerTaskParameter> </TaskDescription> <TaskDescription> <TaskType>SaveResult</TaskType> <SaveResultTaskParameter> <ResultSource>InMemoryFiles</ResultSource> <ResultDestination> <DestinationType>OutputStream</DestinationType> <InputFile>Temp.xlsx</InputFile> <OutputFile>Output.xlsx</OutputFile> </ResultDestination> </SaveResultTaskParameter> </TaskDescription> </Tasks></TaskData>}"

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

            <FilePath>Designer.xlsx</FilePath>

        </SourceWorkbook>

        <DestinationWorkbook>

            <FileSourceType>InMemoryFiles</FileSourceType>

            <FilePath>Temp.xlsx</FilePath>

        </DestinationWorkbook>

        <xmlFile>

            <FileSourceType>CloudFileSystem</FileSourceType>

            <FilePath>DataSet.xml</FilePath>

        </xmlFile>

        </SmartMarkerTaskParameter>

    </TaskDescription>

    <TaskDescription>

        <TaskType>SaveResult</TaskType>

        <SaveResultTaskParameter>

        <ResultSource>InMemoryFiles</ResultSource>

        <ResultDestination>

            <DestinationType>OutputStream</DestinationType>

            <InputFile>Temp.xlsx</InputFile>

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

}

```
{{< /tab >}}

{{< /tabs >}}
