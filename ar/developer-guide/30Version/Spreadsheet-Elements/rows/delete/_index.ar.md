---
---
title: "العمل مع حذف الصفوف في ورقة عمل Excel"
second_title: "Document"
linktitle: "Delete"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, حذف صف, Excel API, REST, سحابة, جدول بيانات, Excel, SDK"
description: "تعرّف على كيفية حذف صف واحد أو صفوف متعددة في ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API. يشمل أمثلة كود مكتوبة بلغات Android وC# وGo وJava وNode.js وPerl وPHP وPython وRuby وSwift."
weight: 20
ArticleTitle: "العمل مع حذف الصفوف في ورقة عمل Excel – دليل واجهة Aspose.Cells Cloud API"
---

## عمليات الحذف المتاحة

تُظهر الأمثلة التالية كيفية حذف صف فارغ واحد أو عدة صفوف من ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud REST API.

- [كيفية حذف صف فارغ في ورقة عمل Excel](/cells/rows/delete/row/)
- [كيفية حذف صفوف متعددة في ورقة عمل Excel](/cells/rows/delete/rows/)

**مرجع واجهة برمجة التطبيقات**

| العنصر | التفاصيل |
|---------------------|---------------------------------------------------------------|
| **طريقة HTTP** | DELETE |
| **النقطة النهائية (Endpoint)** | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **مُعاملات المسار** | `fileName` – اسم ملف Excel (مطلوب)<br>`sheetName` – اسم ورقة العمل (مطلوب) |
| **مُعاملات الاستعلام** | `startrow` – فهرس الصف الأول المراد حذفه (مطلوب)<br>`totalRows` – عدد الصفوف المراد حذفها (مطلوب)<br>`storage` – اسم وحدة التخزين السحابية (اختياري)<br>`folder` – مسار المجلد داخل وحدة التخزين (اختياري) |
| **جسم الطلب** | *لا يوجد* |
| **مثال على الاستجابة** | ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **رموز الحالة الممكنة** | 200 OK – تم حذف الصفوف بنجاح<br>400 Bad Request – مُعلمات غير صالحة<br>401 Unauthorized – فشل المصادقة<br>404 Not Found – الملف أو ورقة العمل غير موجودة<br>500 Internal Server Error – مشكلة من جانب الخادم |

**انظر أيضًا**

- [إضافة صف](/cells/rows/add/)
- [الحصول على صف](/cells/rows/get/)
- [نسخ صف](/cells/rows/copy/)
- [إخفاء صف](/cells/rows/hide/)
- [نظرة عامة على الصفوف](/cells/rows/)
---