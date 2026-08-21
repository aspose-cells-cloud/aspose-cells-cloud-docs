---
title: "إظهار الصفوف المخفية في ورقة عمل إكسل"
second_title: "وثيقة"
linktitle: "إظهار"
type: docs
url: /rows/unhide/
aliases: [/unhide-rows-in-excel-worksheet/]
keywords: "Aspose.Cells Cloud, إكسل, إظهار الصفوف, واجهة REST API, جدول بيانات, .NET, Java, Python, Node.js, Ruby, Go, PHP, Perl, Swift, Aspose.Cells Cloud REST API"
description: "استخدم واجهة Aspose.Cells Cloud REST API لإظهار الصفوف المخفية في ورقة عمل إكسل. تتوفر الواجهة عبر العديد من حزم التطوير (SDKs) مثل .NET و Java و Python و Node.js و Ruby و Go و PHP و Perl و Swift."
weight: 50
ArticleTitle: "إظهار الصفوف المخفية في ورقة عمل إكسل باستخدام واجهة Aspose.Cells Cloud API"
---

تقوم هذه الواجهة (REST API) بإظهار الصفوف المخفية في ورقة عمل إكسل.

**المتطلبات المسبقة:** احصل على رمز وصول JWT صالح من خدمة مصادقة Aspose Cloud، وتأكد من رفع ملف المصنف المستهدف إلى مساحة تخزين مدعومة قبل استدعاء هذه النقطة النهائية (endpoint).

## واجهة PostUnhideWorksheetRows

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/unhide
```

### **الأمان والمصادقة**

تُعد واجهات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة | النوع     | الموقع | الوصف                                                |
|-------------|-----------|--------|------------------------------------------------------|
| name        | string    | path   | اسم المصنف.                                          |
| sheetName   | string    | path   | اسم ورقة العمل.                                      |
| startrow    | integer   | query  | المؤشر الصفري (zero-based) للصف الأول المراد إظهاره. |
| totalRows   | integer   | query  | عدد الصفوف المراد إظهارها.                           |
| height      | number    | query  | ارتفاع الصف (القيمة المبدئية: 15.0).                |
| folder      | string    | query  | مجلد المستند.                                        |
| storageName | string    | query  | اسم مساحة التخزين.                                   |

<a href="https://apireference.aspose.cloud/cells/#/Cells/PostUnhideWorksheetRows" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات عامة قابلة للوصول وتتيح لك تنفيذ تفاعلات REST مباشرة من متصفح الويب.

**المصادقة**  
يجب مصادقة جميع الطلبات باستخدام رمز وصول JWT مُستحصل من خدمة مصادقة Aspose Cloud. تضمين الرمز في الرأس `Authorization: Bearer <jwt token>`.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات إلى واجهة Cloud API باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/unhide?startrow=1&totalRows=1&height=15" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
# ملاحظة: جسم الـ POST فارغ لهذه النقطة النهائية
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

**رموز حالة HTTP**

| الكود | المعنى                     | الوصف                                               |
|-------|----------------------------|-----------------------------------------------------|
| 200   | ناجح (OK)                  | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح (Bad Request)| معلمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مُصادَق (Unauthorized) | رمز JWT غير صالح أو مفقود.                         |
| 413   | حجم البيانات كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح.             |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                          |

للحصول على تفاصيل مُعمّقة حول استكشاف الأخطاء وإصلاحها، راجع دليل [معالجة الأخطاء](/error-handling/).

## عائلة حزم SDK السحابية

استخدام حزمة SDK (SDK) هي أفضل طريقة لتسريع عملية التطوير. فحزم SDK تتعامل مع التفاصيل منخفضة المستوى، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للاطلاع على قائمة كاملة بحزم Aspose.Cells Cloud SDK.

تُظهر أمثلة الرمز التالية كيفية إجراء استدعاءات إلى خدمات ويب Aspose.Cells باستخدام حزم SDK المختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}