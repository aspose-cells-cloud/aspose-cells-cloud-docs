---
title: "ملف طلب الدعم في واجهة برمجة تطبيقات المهام"
second_title: "وثيقة"
type: docs
url: /ar/tasks/support-request-file/
aliases: [/ar/support-request-file-in-task-api/]
keywords: "Aspose.Cells, واجهة برمجة تطبيقات REST, Excel, السحابة"
description: "تتيح واجهة برمجة تطبيقات Aspose.Cells Cloud معالجة ملفات الطلبات القائمة على المهام لملفات عمل Excel."
weight: 10
ArticleTitle: "ملف طلب الدعم في واجهة برمجة تطبيقات المهام في Aspose.Cells"
---

## واجهة برمجة تطبيقات REST

| **واجهة برمجة التطبيقات** | **النوع** | **الوصف** | **رابط المورد** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | تشغيل المهمة | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) واجهة برمجة تطبيقات متاحة للعامة، وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

**معلَمات الطلب**

| المعلَمة | النوع | مطلوبة | الوصف |
|-----------|------|----------|-------------|
| TaskDescription | كائن | نعم | حاوية لتعريف مهمة واحدة. |
| TaskType | سلسلة نصية | نعم | نوع المهمة، مثل `ImportData` أو `SaveResult`. |
| Workbook.FileSourceType | سلسلة نصية | نعم | مصدر ملف ملف العمل (`CloudFileSystem` أو `InMemoryFiles`). |
| Workbook.FilePath | سلسلة نصية | نعم | مسار ملف ملف العمل في المصدر المُحدَّد. |
| ImportBatchDataOption.DestinationWorksheet | سلسلة نصية | نعم | اسم ورقة العمل الهدف لاستيراد البيانات. |
| ImportBatchDataOption.IsInsert | منطقي | نعم | ما إذا كانت الصفوف ستُدرج (`true`) أم تُستبدَل (`false`). |
| ImportBatchDataOption.Source.FileSourceType | سلسلة نصية | نعم | مصدر ملف الطلب (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | سلسلة نصية | نعم | مسار ملف الطلب الذي يحتوي على البيانات المجمعة. |
| SaveResultTaskParameter.ResultSource | سلسلة نصية | نعم | مصدر ملف النتيجة (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | سلسلة نصية | نعم | نوع الوجهة لملف النتيجة (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | سلسلة نصية | نعم | اسم ملف ملف العمل المدخل. |
| SaveResultTaskParameter.ResultDestination.OutputFile | سلسلة نصية | نعم | اسم ملف الإخراج المطلوب. |

**الاستجابة**

| الحقل | النوع | الوصف |
|-------|------|-------------|
| Code | عدد صحيح | رمز حالة HTTP (مثل 200 للنجاح). |
| Status | سلسلة نصية | حالة العملية (`OK` أو رسالة خطأ). |
| Result | كائن | تفاصيل تنفيذ المهمة، بما في ذلك أي ملفات تم إنشاؤها. |

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول إلى خدمات ويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
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
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

لمزيد من المعلومات حول المهام ذات الصلة، راجع صفحات [مهمة ImportData](/ar/cells/tasks/importdata/) و [مهمة SaveResult](/ar/cells/tasks/save-result/).

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع التطوير. يعتني SDK بالتفاصيل منخفضة المستوى ويتيح لك التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}