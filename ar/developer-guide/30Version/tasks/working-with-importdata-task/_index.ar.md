---
title: "مهمة ImportData – مرجع واجهة برمجة تطبيقات Aspose.Cells Cloud وأمثلة cURL"  
second_title: "مستند"  
type: docs  
url: /ar/tasks/importdata/
aliases: [  /ar/working-with-importdata-task/ ]
keywords: "Aspose.Cells، مهمة ImportData، واجهة برمجة تطبيقات Excel، REST، cURL، SDK"  
description: "تعرّف على كيفية استيراد كميات كبيرة من البيانات إلى أوراق عمل Excel باستخدام مهمة ImportData في Aspose.Cells Cloud. يشمل بناء جملة cURL ومخطط الطلب وأمثلة SDK (C# و PHP و Ruby و Node.js) وتعامل مع الأخطاء."  
weight: 40  
---  

## واجهة برمجة تطبيقات REST  

| **واجهة برمجة التطبيقات** | **النوع** | **الوصف** | **رابط المورد** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) واجهة برمجة تطبيقات متاحة علنًا تسمح بإجراء تفاعلات REST مباشرة من متصفح ويب.  

يمكنك استخدام أداة سطر الأوامر **cURL** لاستدعاء خدمات Aspose.Cells Cloud. يُظهر المثال التالي كيفية تنفيذ مهمة **ImportData** باستخدام حمولة JSON مُنسّقة بشكل صحيح.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
  "Tasks": [
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "CloudFileSystem",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet1",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml.txt"
            }
          }
        }
      }
    },
    {
      "TaskDescription": {
        "TaskType": "ImportData",
        "ImportDataTaskParameter": {
          "Workbook": {
            "FileSourceType": "InMemoryFiles",
            "FilePath": "TaskBook.xlsx"
          },
          "ImportBatchDataOption": {
            "DestinationWorksheet": "Sheet2",
            "IsInsert": true,
            "Source": {
              "FileSourceType": "RequestFiles",
              "FilePath": "Batch_data_xml_2.txt"
            }
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
            "DestinationType": "CloudFileSystem",
            "InputFile": "TaskBook.xlsx",
            "OutputFile": "ImpDataBook.xlsx"
          }
        }
      }
    }
  ]
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "OK",
  "TaskId": "12345678",
  "Result": {
    "FilePath": "ImpDataBook.xlsx",
    "DownloadUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

يُعد استخدام SDK الطريقة الأكثر كفاءة لدمج هذه العمليات في تطبيقك. فتتولى SDKات المصادقة وبناء الطلب وتفسير الاستجابة، ما يسمح لك بالتركيز على المنطق التجاري. للاطّلاع على القائمة الكاملة لـ SDKs الخاصة بـ Aspose.Cells Cloud، راجع [مستودع GitHub](https://github.com/aspose-cells-cloud).  

تُظهر أمثلة الرمز التالية كيفية استدعاء خدمات Aspose.Cells عبر SDKات متنوعة:

{{< tabs tabTotal="5" tabID="8" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Tasks-ImportTaskData-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_run_task-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Tasks-ImportTaskData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-ImportData-postImportDataMultipartContent-1.pl" >}}

{{< /tab >}}

{{< /tabs >}}
---