---
title: "إضافة صفوف متعددة إلى ورقة عمل Excel"
ArticleTitle: "إضافة صفوف متعددة إلى ورقة عمل Excel باستخدام واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktype: "صفحات"
type: docs
url: /rows/add/rows/
keywords: "Aspose.Cells Cloud، إدخال صفوف، ورقة عمل Excel، واجهة REST API، مكتبة SDK، إضافة صفوف متعددة"
description: "تعرّف على كيفية استخدام واجهة Aspose.Cells Cloud REST API لإدخال صفوف متعددة في ورقة عمل Excel. يغطي هذا الدليل نقطة النهاية ومعلمات الطلب وأوامر cURL النموذجية وأمثلة استخدام مكتبات SDK."
weight: 20
---

تقوم هذه الواجهة البرمجية REST بإضافة عدة صفوف جديدة إلى ورقة عمل Excel.

## PutInsertWorksheetRows API

```http
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">المصادقة باستخدام رمز مميز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة     | النوع    | الموقع | الوصف                                                                 |
|------------------|----------|--------|------------------------------------------------------------------------|
| name             | نص (string) | المسار (path) | اسم المصنف (الملف).                                                    |
| sheetName        | نص (string) | المسار (path) | اسم ورقة العمل.                                                        |
| startrow         | عدد صحيح (integer) | الاستعلام (query) | فهرس أول صف سيتم إدراجه (**يبدأ من الصفر**).                          |
| totalRows        | عدد صحيح (integer) | الاستعلام (query) | عدد الصفوف المراد إدراجه.                                              |
| updateReference  | منطقي (boolean) | الاستعلام (query) | ما إذا كان سيتم تحديث مراجع الخلايا بعد الإدراج (`true` أو `false`). |
| folder           | نص (string) | الاستعلام (query) | المجلد الذي يحتوي على المستند.                                         |
| storageName      | نص (string) | الاستعلام (query) | اسم وحدة التخزين.                                                       |

**المتطلبات المسبقة**  
يجب أن يكون المصنف موجودًا مسبقًا في وحدة التخزين (أو المجلد) المحددة قبل تنفيذ هذه العملية.

**المصادقة**  
تتطلب الواجهة البرمجية وجود رمز مميز JWT صالح. يُدرج في رأس الطلب `Authorization` كما هو موضح في مثال cURL أدناه.

يُعرّف [مواصفة OpenAPI](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRows) واجهة برمجة تطبيقات عامة قابلة للاستخدام، وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية استدعاء واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=11&updateReference=true" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **ملاحظة:** لا تتطلب هذه العملية `PUT` وجود جسم طلب؛ يمكن إرسال كائن JSON فارغ (`{}`) إذا اشترطت مكتبة العميل وجود حمل بيانات.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*رموز الاستجابة الممكنة*  

- **200 OK** – أُدخلت الصفوف بنجاح.  
- **400 Bad Request** – معلمات غير صالحة (مثل: فهرس صف سالب).  
- **401 Unauthorized** – رمز JWT مفقود أو غير صالح.  
- **404 Not Found** – المصنف أو ورقة العمل المحددة غير موجودة.  
- **500 Internal Server Error** – خطأ في الخادم غير متوقع.

{{< /tab >}}

{{< /tabs >}}

للمزيد من العمليات على الصفوف، راجع الصفحات ذات الصلة: **حذف الصفوف**، **الحصول على بيانات الصفوف**، و **نسخ الصفوف**.

## مجموعة أدوات Cloud SDK

استخدام مكتبة SDK هو أسرع طريقة لتطوير التطبيقات، إذ تُدارة التفاصيل منخفضة المستوى تلقائيًا مما يسمح لك بالتركيز على مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية استدعاء خدمات ويب Aspose.Cells باستخدام مكتبات SDK متنوعة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}