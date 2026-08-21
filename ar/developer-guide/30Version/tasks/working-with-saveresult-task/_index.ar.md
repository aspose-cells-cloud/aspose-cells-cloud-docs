---
title: "العمل مع مهمة SaveResult"
second_title: "مستند"
type: docs
url: /tasks/save-result/
aliases: [/working-with-saveresult-task/]
keywords: "مهمة SaveResult، واجهة برمجة تطبيقات Aspose.Cells Cloud، تصدير النتيجة، تنزيل ملف الحساب، التخزين السحابي، واجهة REST API، الجداول الحسابية، إكسل"
description: "تعرّف على كيفية استخدام مهمة SaveResult في واجهة برمجة تطبيقات Aspose.Cells Cloud لتصدير بيانات ملف الحساب المعالَجة إلى التخزين السحابي أو تنزيلها مباشرةً. يشمل أمثلة cURL وJava و.NET، ومرجعًا كاملاً للمعاملات."
weight: 50
---

## واجهة برمجة التطبيقات REST

| **الواجهة** | **النوع** | **الوصف** | **رابط المورد** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) واجهة برمجة تطبيقات متاحة علنًا، ويتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يُظهر المثال التالي كيفية استدعاء واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/xml" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d "<?xml version=\"1.0\" encoding=\"UTF-8\"?>
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet1</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>TaskBook.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <Source>
            <FileSourceType>RequestFiles</FileSourceType>
            <FilePath>Batch_data_xml_2.txt</FilePath>
          </Source>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>CloudFileSystem</DestinationType>
          <InputFile>TaskBook.xlsx</InputFile>
          <OutputFile>ImpDataBook.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HttpResponseMessage تحتوي على نتيجة العملية.
```

{{< /tab >}}

{{< /tabs >}}

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالمكتبة (SDK) تعتني بالتفاصيل منخفضة المستوى وتجعلك تركّز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية إجراء مكالمات إلى خدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات (SDKs) مختلفة:

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
---