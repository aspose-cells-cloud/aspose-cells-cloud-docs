---
title: "العمل مع مهمة SmartMarker في API Aspose.Cells السحابية"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "مهمة SmartMarker، Aspose.Cells Cloud، REST API، Excel، أتمتة الجداول المحسوبة"
description: "تعرّف على كيفية استخدام مهمة SmartMarker في API Aspose.Cells Cloud مع أمثلة باستخدام cURL وSDKs، بما في ذلك مخطط الطلب ومعالجة الأخطاء."
weight: 60
ArticleTitle: "العمل مع مهمة SmartMarker في API Aspose.Cells السحابية"
---

## API REST

**SmartMarker** هي ميزة من ميزات API Aspose.Cells Cloud التي تدمج البيانات من مصادر XML أو JSON داخل العناصر النائبة (placeholders) الموجودة في قالب Excel لإنشاء ملف عمل مُملأ بالكامل. تُستخدم عادةً في إنشاء التقارير، والدمج البريدي (mail-merge)، وإنشاء الجداول المحسوبة المبنية على البيانات.

**المتطلبات المسبقة**

- إصدار API Aspose.Cells Cloud 3.0 أو أحدث.  
- رمز وصول OAuth2/JWT ساري المفعول (يُمرر في رأس الطلب `Authorization: Bearer <token>`).  
- ملفات المصدر (ملف العمل القالبي وملف البيانات) المرفوعة إلى مساحة التخزين السحابية لـ Aspose أو المتوفرة عبر نوع نظام ملفات مدعوم.  
- عنوان HTTPS (يجب أن تستخدم جميع الطلبات بروتوكول TLS).

| **API** | **النوع** | **الوصف** | **رابط المورد** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة **cURL** سطر الأوامر للوصول إلى خدمات Aspose.Cells بسهولة. يوضح المثال التالي كيفية تشغيل مهمة SmartMarker ثم حفظ ملف العمل الناتج.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### مخطط الطلب (مقتطف)

| العنصر | النوع | مطلوب | الوصف |
| ------- | ---- | -------- | ----------- |
| `TaskData` | object | نعم | العنصر الجذري الذي يحتوي على كائن أو أكثر من `TaskDescription`. |
| `Tasks` | مصفوفة من الكائنات | نعم | مجموعة المهام التي سيتم تنفيذها بالترتيب. |
| `TaskDescription.TaskType` | string | نعم | نوع المهمة (`SmartMarker`، `SaveResult`، إلخ). |
| `SmartMarkerTaskParameter.SourceWorkbook` | object | نعم | يحدد موقع ملف العمل القالبي. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | object | نعم | يحدد مكان تخزين ملف العمل المؤقت. |
| `SmartMarkerTaskParameter.xmlFile` | object | نعم | مصدر البيانات (XML/JSON) المستخدم من قبل SmartMarker. |
| `SaveResultTaskParameter.ResultDestination` | object | نعم | يُعرّف كيفية إرجاع ملف العمل النهائي (مثل `OutputStream`). |

### معالجة الأخطاء

قد يُعيد API الرسائل التالية لحالات HTTP:

- **400 Bad Request** – طلب غير صحيح أو نقص في الحقول الإلزامية.  
- **401 Unauthorized** – رمز مصادقة غير صالح أو مفقود.  
- **404 Not Found** – لا يمكن العثور على أحد ملفات المصدر المحددة.  
- **500 Internal Server Error** – حدوث خطأ غير متوقع من جانب الخادم.

تحقق من جسم الاستجابة للعثور على كائن `Error` يحتوي على `Code` ورسالة وصفية `Message`.

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. تُعنى SDK بمعالجة التفاصيل منخفضة المستوى وتتيح لك التركيز على مهام مشروعك. يُرجى زيارة [مستودع GitHub](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

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
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}