---
title: "كيفية التعامل مع إمكانية الرؤية في ورقة عمل إكسل"
second_title: "مستند"
linktitle: "إمكانية الرؤية"
type: docs
url: /ar/worksheets/panes/
keywords: "Aspose.Cells Cloud، API إخفاء ورقة عمل، API إظهار ورقة عمل، إمكانية رؤية ورقة عمل إكسل، REST API لـ إكسل، Aspose.Cells v3.0"
description: "تعرّف على كيفية إخفاء أو إظهار ورقات عمل إكسل برمجيًا باستخدام واجهة Aspose.Cells Cloud REST API. يشمل العناوين URL للطلبات، وأمثلة لـ cURL و .NET SDK، ومعالجة الأخطاء، وملاحظات محددة بالإصدار."
weight: 20
---

## التعامل مع إمكانية الرؤية في ورقة عمل إكسل

تُعرّف *إمكانية الرؤية للورقة* ما إذا كانت الورقة معروضة للمستخدم النهائي. باستخدام Aspose.Cells Cloud، يمكنك إخفاء أو إظهار ورقة عمل عبر طلب REST بسيط. عناوين نقاط نهاية الواجهة المستخدمة هي:

* **إخفاء ورقة عمل** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **إظهار ورقة عمل** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **إصدار الواجهة المدعوم:** **v3.0** (حتى مارس 2026)

### المتطلبات المسبقة
1. حساب نشط لـ **Aspose.Cells Cloud**.  
2. **معرف عميل** و**سر عميل** ساري المفعول (أو رمز وصول OAuth 2.0).  
3. يجب أن يكون المصنف (`{fileName}`) قد تم رفعه مسبقًا إلى مساحة التخزين السحابية لـ Aspose.  

---

## إخفاء ورقة عمل

### الطلب
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### الاستجابة
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### مثال على cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### مثال على .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"تم إخفاء الورقة: {response.Worksheet.Visible}");
```

### الأخطاء الشائعة
| رمز HTTP | الوصف                                      | التخفيف                                                |
|----------|--------------------------------------------|---------------------------------------------------------|
| 400      | جسم JSON غير صالح أو مفتاح `Visible` مفقود | تأكد من أن جسم الطلب عبارة عن JSON صالح يحتوي على المفتاح. |
| 401      | غير مُخوَّل – رمز منتهٍ أو مفقود            | قم بتحديث رمز OAuth وأدرجها في الرأس.                  |
| 404      | ورقة العمل أو الملف غير موجود              | تأكد من صحة `{fileName}` و`{sheetName}`.                |
| 409      | ورقة العمل مخفية بالفعل                     | تحقق من حالة الرؤية الحالية قبل إرسال الطلب.           |

---

## إظهار ورقة عمل

### الطلب
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### الاستجابة
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### مثال على cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### مثال على .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"الورقة مرئية: {response.Worksheet.Visible}");
```

### الأخطاء الشائعة
| رمز HTTP | الوصف                                      | التخفيف                                                |
|----------|--------------------------------------------|---------------------------------------------------------|
| 400      | جسم JSON غير صالح أو مفتاح `Visible` مفقود | قدّم حمولة JSON صحيحة تحتوي على `"Visible": true`.    |
| 401      | غير مُخوَّل – رمز منتهٍ أو مفقود            | أعد إنشاء رمز الوصول وحاول مرة أخرى.                   |
| 404      | ورقة العمل أو الملف غير موجود              | تأكد من وجود أسماء الملف والورقة في التخزين.            |
| 409      | الورقة مرئية بالفعل                         | لا حاجة لاتخاذ إجراء؛ الورقة معروضة بالفعل.            |

---

## العمليات ذات الصلة
> *تجميد المقاطع* | *تقسيم المقاطع* | *التكبير* – راجع الصفحات المقابلة لمزيد من عناصر التحكم في تخطيط ورقة العمل.

---

## الأسئلة الشائعة

<dl>
  <dt>كيف أُخفي ورقة عمل باستخدام واجهة Aspose.Cells Cloud API؟</dt>
  <dd>أرسل طلب `PUT` إلى `/cells/{fileName}/worksheets/{sheetName}/visibility` مع جسم JSON `{ "Visible": false }`. تأكد من تضمين رمز وصول OAuth 2.0 ساري المفعول. ستستلم استجابة `200 OK` تحتوي على كائن الورقة المُحدَّث.</dd>

  <dt>ما هي الاستجابة التي أحصل عليها بعد إظهار ورقة عمل؟</dt>
  <dd>تُعيد الواجهة `200 OK` مع حمولة تحتوي على كائن الورقة حيث `"Visible": true`. تحتوي الاستجابة على خصائص الورقة `Name` و`Index` و`Visible`.</dd>

  <dt>هل يمكنني إخفاء عدة ورقات عمل في طلب واحد؟</dt>
  <dd>لا. تعمل نقطة نهاية إمكانية الرؤية على ورقة عمل واحدة فقط مُعرَّفة باسم `{sheetName}`. لإخفاء عدة أوراق، كرّر العملية على كل اسم في كود العميل.</dd>
</dl>

---

*كتبه فريق Aspose Docs – أكثر من 15 عامًا من الخبرة في أتمتة سير عمل إكسل.*