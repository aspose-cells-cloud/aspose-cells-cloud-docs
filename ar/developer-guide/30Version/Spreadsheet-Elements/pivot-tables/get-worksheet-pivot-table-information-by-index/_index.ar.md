---
title: "الحصول على جدول محوري في ورقة عمل إكسل"
second_title: "مستند"
linktitle: الحصول
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells، الجدول المحوري، إكسل، واجهة برمجة تطبيقات REST، الحصول على الجدول المحوري في ورقة العمل"
description: "استرجاع جدول محوري من ورقة عمل إكسل عبر واجهة برمجة تطبيقات Aspose.Cells Cloud REST. يتضمن بناء الجملة المطلوبة، المعلمات، المصادقة، مخطط الاستجابة، معالجة الأخطاء، وأمثلة لحزم تطوير البرمجيات (SDK)."
weight: 10
ArticleTitle: "الحصول على جدول محوري في ورقة عمل إكسل"
---

تُعيد هذه الواجهة البرمجية معلومات **الجدول المحوري** في ورقة العمل بناءً على مؤشره.

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

## واجهة برمجة تطبيقات REST

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### معلمات الطلب

| اسم المعلمة        | النوع   | الموقع | الوصف                                                    |
| ------------------- | ------- | ------ | --------------------------------------------------------- |
| **name**            | نص (string) | مسار   | اسم ملف إكسل.                                            |
| **sheetName**       | نص (string) | مسار   | اسم ورقة العمل التي تحتوي على الجدول المحوري.            |
| **pivottableIndex** | عدد صحيح (integer) | مسار   | المؤشر الصفري (zero-based) للجدول المحوري في ورقة العمل. |
| **folder**          | نص (string) | استعلام | المجلد الذي يُخزَّن فيه المستند.                         |
| **storageName**     | نص (string) | استعلام | اسم تخزين Aspose Cloud.                                  |

يمكنك استخدام أداة سطر الأوامر **cURL** للوصول بسهولة إلى خدمات Aspose.Cells عبر الويب. يُظهر المثال التالي كيفية استدعاء الواجهة البرمجية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**مخطط الاستجابة**

| الحقل          | النوع   | الوصف                                            |
|----------------|---------|--------------------------------------------------|
| Status         | نص (string) | حالة العملية كنص (مثال: "OK").                   |
| PivotFilters   | مصفوفة (array) | مجموعة تعريفات مرشّحات الجدول المحوري.         |
| └─ AutoFilter  | كائن (object) | تفاصيل التصفية التلقائية المطبّقة على الجدول المحوري. |
|    └─ link     | كائن (object) | معلومات الارتباط التشعبي (hyperlink) الخاص بالمرشّح. |
|    └─ FilterColumns | مصفوفة (array) | إعدادات المرشّح لكل عمود على حدة.          |
|    └─ Range    | نص (string) | مدى الخلايا الذي يطبّق عليه المرشّح.                |
|    └─ Sorter   | كائن (object) | إعدادات الترتيب للبيانات المُرشّحة.                 |
| (تتّبع الحقول المتداخلة الإضافية نفس البنية الموضّحة في مثال JSON أعلاه) |

{{< /tab >}}

{{< /tabs >}}

### معالجة الأخطاء

تتّبع الواجهة البرمجية رموز حالة HTTP القياسية. تشمل الاستجابات الشائعة ما يلي:

| رمز الحالة | المعنى                                                          | مثال JSON (خطأ)                                   |
| ----------- | ---------------------------------------------------------------- | ------------------------------------------------- |
| 200         | نجاح – تم إرجاع الجدول المحوري                                  | —                                                 |
| 401         | غير مصادَق – رمز غير صالح أو مفقود                             | `{"code":401,"message":"Invalid access token."}`  |
| 404         | غير موجود – الملف أو ورقة العمل أو مؤشر الجدول المحوري غير موجود | `{"code":404,"message":"Pivot table not found."}` |
| 500         | خطأ في الخادم – حالة غير متوقّعة                               | `{"code":500,"message":"Internal server error."}` |

**ملاحظات:** تدعم الواجهة البرمجية ملفات إكسل حتى 150 ميغابايت، وتعمل مع صيغ إكسل من 2007 إلى 2021. تأكّد من أن اسم ورقة العمل حسّاس لحالة الأحرف.

## عائلة حزم تطوير البرمجيات (SDK) السحابية

استخدام حزمة تطوير برمجيات (SDK) هو أفضل طريقة لتسريع عملية التطوير. فحزمة SDK تُدار بالتفاصيل منخفضة المستوى، مما يمكّنك من التركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بحزم تطوير البرمجيات لـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام حزم تطوير برمجيات مختلفة:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}
---