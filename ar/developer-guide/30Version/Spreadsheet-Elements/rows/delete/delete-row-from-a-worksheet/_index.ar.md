---
title: "حذف صف في ورقة عمل إكسل"
second_title: "مستند"
linktitle: "صف"
type: docs
url: /rows/delete/row/
aliases: [/delete-row-from-a-worksheet/]
description: "استخدم نقطة النهاية DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} لإزالة صف محدد من ورقة عمل إكسل عبر واجهة برمجة تطبيقات Aspose.Cells Cloud REST API. يشمل أمر cURL وأمثلة SDK ومراجع كاملة للمعلمات."
keywords: "Aspose.Cells, حذف صف, إكسل, API, REST, سحابة, SDK"
weight: 80
ArticleTitle: "حذف صف في ورقة عمل إكسل – دليل واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

تقوم هذه الواجهة البرمجية REST بحذف صف من ورقة عمل إكسل.

**المتطلبات الأساسية**  
- رمز مميز JWT صالح لـ **Authorization** (المصادقة).  
- يجب أن يكون ملف المصنف مخزنًا في مساحة تخزين مدعومة من Aspose Cloud (الافتراضية أو المخصصة).  
- يجب أن تكون المجلد الهدف (إن وُجد) موجودًا في مساحة التخزين المختارة.

## واجهة برمجة تطبيقات REST

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **معلمات الطلب**

| اسم المعلمة         | النوع   | المسار / الاستعلام | مطلوب | الوصف                                                                                       |
|---------------------|---------|-------------------|--------|----------------------------------------------------------------------------------------------|
| **name**            | نص (string) | المسار            | نعم    | اسم ملف المصنف.                                                                             |
| **sheetName**       | نص (string) | المسار            | نعم    | اسم ورقة العمل.                                                                             |
| **rowIndex**        | عدد صحيح | المسار            | نعم    | الفهرس الصفري (zero-based) للصف المراد حذفه.                                                |
| **startrow**        | عدد صحيح | الاستعلام         | لا     | فهرس أول صف ليتم حذفه (عادةً يساوي `rowIndex`).                                             |
| **totalRows**       | عدد صحيح | الاستعلام         | لا     | عدد الصفوف المتتالية المراد حذفها.                                                          |
| **updateReference** | منطقي (boolean) | الاستعلام         | لا     | عند تعيينها إلى `true` (القيمة الافتراضية)، يتم تحديث الصيغ وال نطاقات المسماة والمرجعيات الأخرى بعد الحذف. |
| **folder**          | نص (string) | الاستعلام         | لا     | المجلد الذي يحتوي على ملف المصنف.                                                          |
| **storageName**     | نص (string) | الاستعلام         | لا     | اسم خدمة التخزين.                                                                           |

يُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow) واجهة برمجة تطبيقات عامة قابلة للوصول، وتمكنك من إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي طلبًا كاملاً قابلًا للتنفيذ.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**رموز استجابة HTTP الممكنة**

| الرمز | المعنى                             | الوصف                                                                 |
|-------|-------------------------------------|------------------------------------------------------------------------|
| 200   | OK (تم بنجاح)                      | تمت عملية حذف الصف بنجاح.                                              |
| 400   | Bad Request (طلب غير صالح)         | معلمات مفقودة أو غير صالحة (مثل `rowIndex` غير العددي).              |
| 401   | Unauthorized (غير مخوّل)            | رمز JWT غير صالح أو مفقود.                                            |
| 404   | Not Found (غير موجود)              | ملف المصنف أو ورقة العمل أو الصف المحدد غير موجود.                    |
| 500   | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم؛ راجع استجابة الخطأ للحصول على التفاصيل.    |

**مثال على استجابة خطأ**

```json
{
  "Code": 400,
  "Message": "تم تقديم فهرس صف غير صالح."
}
```

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. فالـ SDK يُجرّد التفاصيل من المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**العمليات ذات الصلة**  
- [إضافة صف](/cells/rows/add/row/)  
- [حذف صفوف متعددة](/cells/rows/delete/rows/)  
- [الحصول على تفاصيل الصف](/cells/rows/get/row/)  
---