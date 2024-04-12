---
title: Travailler avec les tâches SmartMarker
type: docs
url: /fr/tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: REST API, task, save result, spreadsheets, exce
description: "Cells.Cloud API pour Excel fonctionne : prise en charge des tâches par le marqueur intelligent"
weight: 60
---
## REPOS API

|**API**|**Taper**|**Description**|**Lien vers la ressource**|
|:- |:- |:- |:- |
|/cellules/tâche/tâche d'exécution|POSTE|Exécuter la tâche|[PostExécutionTâche](https://apireference.aspose.cloud/cells/#/Task/PostRunTask)|


 Le[Spécification OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) définit une interface de programmation accessible au public et vous permet d'effectuer des interactions REST directement depuis un navigateur Web.

 Vous pouvez utiliser**cURL** outil de ligne de commande pour accéder facilement aux services Web Aspose.Cells. L'exemple suivant montre comment passer des appels vers Cloud API avec cURL.


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

 Utiliser un SDK est le meilleur moyen d’accélérer le développement. Un SDK prend en charge les détails de bas niveau et vous permet de vous concentrer sur les tâches de votre projet. Veuillez consulter le[Dépôt GitHub](https://github.com/aspose-cells-cloud) pour une liste complète des SDK Cloud Aspose.Cells.

Les exemples de code suivants montrent comment effectuer des appels vers les services Web Aspose.Cells à l'aide de divers SDK :

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
