---
title: "تجميع الأعمدة – وثائق واجهة Aspise.Cells Cloud API"
description: "تجميع أعمدة ورقة عمل في ملف Excel باستخدام واجهة Aspose.Cells Cloud REST API (الإصدار 3.0). يشمل بناء الجملة للطلب، المعلمات، أمثلة cURL و SDK، وتفاصيل الاستجابة."
keywords: "Aspose.Cells، تجميع الأعمدة، واجهة Excel API، REST، SDK سحابي"
weight: 60
type: docs
aliases:
  - /group-columns-in-an-excel-worksheet/
  - /group-columns-in-excel-worksheet/
---

# تجميع الأعمدة في ورقة عمل Excel

**إصدار API:** v3.0  
**العملية:** `PostGroupWorksheetColumns` – تجميع أعمدة ورقة العمل داخل ورقة العمل.

---

## نظرة عامة

تتيح لك هذه الواجهة البرمجية تجميع نطاق من الأعمدة داخل ورقة عمل. يمكن إظهار الأعمدة المجمّعة أو إخفاؤها، مما يمكّنك من إنشاء أقسام قابلة للطيّ تشبه تلك الموجودة في Microsoft Excel.

---

## المتطلبات الأساسية

- **رمز وصول JWT** صالح تم الحصول عليه من خدمة مصادقة Aspose Cloud.  
- يجب أن يكون ملف المصنف مخزنًا في مكان يمكن لـ Aspose.Cells Cloud الوصول إليه (التخزين الافتراضي أو اسم تخزين مخصص).  
- إصدار SDK المطلوب (إذا كنت تستخدم SDK): أحدث إصدار يدعم إصدار API **v3.0**.  

---

## المصادقة

تتطلب جميع الطلبات مصادقة باستخدام **رمزBearer**.

```http
Authorization: Bearer <access_token>
```

للحصول على تفاصيل حول كيفية الحصول على رمز، راجع [دليل مصادقة JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

---

## طلب HTTP

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/columns/group
```

| المعلمة | الموقع | الإجباري | الوصف |
|----------|---------|----------|-------------|
| `name` | المسار | نعم | اسم ملف المصنف (مثل `test.xlsx`). |
| `sheetName` | المسار | نعم | اسم ورقة العمل التي تحتوي على الأعمدة المراد تجميعها. |
| `firstIndex` | الاستعلام | نعم | المؤشر البادئ من الصفر (zero-based index) للعمود الأول المُراد تضمينه في المجموعة. |
| `lastIndex` | الاستعلام | نعم | المؤشر البادئ من الصفر (zero-based index) للعمود الأخير المُراد تضمينه في المجموعة. |
| `hide` | الاستعلام | لا | إذا كانت القيمة `true`، فستُخفى الأعمدة المجمّعة؛ وإلا ستظل ظاهرة. |
| `folder` | الاستعلام | لا | المسار إلى المجلد الذي يحتوي على المصنف. |
| `storageName` | الاستعلام | لا | اسم خدمة التخزين التي يوجد فيها الملف. |

---

## مثال على الطلب (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/columns/group?firstIndex=1&lastIndex=2&hide=true" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>"
```

> **ملاحظة:** يستخدم الطلب **HTTPS** لضمان تشفير الاتصال.

---

## الاستجابة

### نجاح (200)

| الحقل | النوع | الوصف |
|--------|--------|-------------|
| `Code` | عدد صحيح | رمز حالة HTTP (`200`). |
| `Status` | نص | الحالة النصية للعملية (`OK`). |

**مثال**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### خطأ (مثل 400 Bad Request)

| الحقل | النوع | الوصف |
|--------|--------|-------------|
| `Code` | عدد صحيح | رمز حالة HTTP (`400`، `401`، `404`، `500`، …). |
| `Status` | نص | الحالة النصية (`Error`). |
| `ErrorMessage` | نص | وصف قابل للقراءة للخطأ. |
| `ErrorCode` | نص | مُعرّف برمجي للخطأ. |

**مثال – طلب غير صالح**

```json
{
  "Code": 400,
  "Status": "Error",
  "ErrorMessage": "مؤشر عمود غير صالح.",
  "ErrorCode": "InvalidParameter"
}
```

---

## أمثلة باستخدام SDK

تُظهر المقاطع التالية كيفية استدعاء عملية **تجميع أعمدة ورقة العمل** باستخدام SDKs المدعومة.

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetColumns.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetColumns.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetColumns.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetColumns.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetColumns.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetColumns.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetColumns.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetColumns.go" >}}

{{< /tab >}}

{{< /tabs >}}

---

## ملاحظات

- **سلوك التجميع:** تُنشئ الواجهة مجموعة أعمدة يمكن توسيعها أو طيّها داخل Excel. وعند تعيين `hide=true`، تُطيّ المجموعة فورًا.  
- **العدّ من الصفر (Zero-based indexing):** يبدأ كل من `firstIndex` و `lastIndex` من **0**؛ أول عمود في ورقة العمل يحمل المؤشر 0.  
- **اعتبارات التخزين:** إذا كان المصنف موجودًا في تخزين غير افتراضي، فقم بتوفير معلمتَي الاستعلام `folder` و `storageName`.  

---

## انظر أيضًا

- [المصادقة – باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- [مواصفات OpenAPI لتجميع أعمدة ورقة العمل](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetColumns)  
- [SDKs لـ Aspose.Cells Cloud (GitHub)](https://github.com/aspose-cells-cloud)  
- [تجميع الصفوف في ورقة عمل Excel](/rows/group/)  

---

> *الرسم التوضيحي:* ![لقطة شاشة تُظهر أعمدة مجمّعة في ورقة عمل Excel](./images/group-columns.png){: .img-fluid alt="لقطة شاشة تُظهر أعمدة مجمّعة في ورقة عمل Excel" }

*يجب استبدال صورة النموذج أعلاه بلقطة شاشة فعلية تُظهر النتيجة البصرية لتجميع الأعمدة.*
---