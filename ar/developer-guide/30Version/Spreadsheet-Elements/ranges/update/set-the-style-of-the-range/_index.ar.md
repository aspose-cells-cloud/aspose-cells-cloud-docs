---
title: "ضبط نمط النطاق – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "التوثيق"
linktitle: "ضبط نمط النطاق"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells، نمط النطاق، واجهة برمجة التطبيقات، إكسل، السحابة"
description: "تعرّف على كيفية ضبط نمط نطاق خلايا في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يتضمن خطوات المصادقة، وتنسيق الطلب، وتفاصيل الاستجابة، وأمثلة لـ SDKs لغات البرمجة مثل .NET وJava وPython وGo وغيرها."
weight: 70
---

## **مقدمة**
يُظهر هذا المثال كيفية ضبط نمط نطاق باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud. ويمكنك استدعاء واجهة برمجة التطبيقات من العديد من لغات البرمجة، مثل .NET وJava وPHP وRuby وPython وJavaScript (jQuery) وغيرها.

## **معلومات واجهة برمجة التطبيقات**

| واجهة برمجة التطبيقات                                               | النوع | الوصف                              | رابط المورد                                                                                                                                 |
| -------------------------------------------------------------------- | ----- | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style                  | POST  | ضبط نمط خلية لنطاق مُسمّى              | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **مثال باستخدام cURL**  

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

** المتطلبات الأساسية **  
1. احصل على رمز وصول (access token) عبر تدفق بيانات اعتماد العميل OAuth2 (`POST https://api.aspose.cloud/connect/token`).  
2. أضف الرأس `Authorization: Bearer <access_token>` في كل طلب.  

**الطلب**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*يُحدّد الكائن `Range` الخلية العلوية اليسرى وحجم النطاق. ويحتوي الكائن `Style` على خيارات التنسيق المطلوب تطبيقها.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**الاستجابة**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**معالجة الأخطاء** – في حالة فشل الاستدعاء، تُعيد واجهة برمجة التطبيقات رمز الحالة HTTP المناسب (مثل 400 أو 401 أو 500) مصحوبًا بمحتوى JSON يحتوي على حقلَي `Error` و`Message`. تحقّق من قيمة الحقل `Code`؛ وأي نتيجة لا تساوي 200 يجب تسجيلها والتعامل معها وفقًا لسياسة معالجة الأخطاء الخاصة بك.

{{< /tab >}}

{{< /tabs >}}

## **مصدر SDK**
يمكن تنزيل حزم SDK الخاصة بـ Aspose.Cells Cloud من الصفحة التالية: [المكتبات المتاحة (Available SDKs)](/cells/available-sdks/)

### **أمثلة على SDKs**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}