---
title: "واجهة برمجة تطبيقات Aspose.Cells Cloud - تحويل بيانات جدول إكسل محلي إلى ملف PDF - أداة مجانية عبر الإنترنت"
second_title: "مستند"
ArticleTitle: "كيفية تحويل بيانات جدول جداول البيانات المحلية إلى ملف PDF: دليل خطوة بخطوة"
linktype: "تحويل الجدول إلى PDF"
type: docs
url: /ar/convert-table-to-pdf/
keywords: "Aspose.Cells, تحويل إكسل إلى PDF, تحويل الجداول, واجهة برمجة تطبيقات السحابة"
description: "قم بتحويل جدول إكسل محلي إلى ملف PDF بسرعة باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud REST."
weight: 100
---

تصدير بيانات الجدول من ملف إكسل محلي إلى ملف PDF باستخدام واجهة برمجة تطبيقات السحابة.

## **واجهة برمجة تطبيقات تحويل الجدول إلى PDF**

### واجهة برمجة تطبيقات الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/table/pdf
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معامِلات الطلب:**

| اسم المعامل | النوع | المسار / سلسلة الاستعلام / جسم HTTP | الوصف |
| :----------- | :----- | :------------------------- | :-------------------------------------------------------------------------------------- |
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات المراد تحويله. |
| worksheet | سلسلة نصية | استعلام | اسم ورقة العمل الخاصة بجدول البيانات. |
| tableName | سلسلة نصية | استعلام | اسم الجدول المراد تحويله. |
| outPath | سلسلة نصية | استعلام | (اختياري) مسار المجلد الذي سيتم حفظ ملف PDF المحول فيه. القيمة الافتراضية هي null. |
| outStorageName | سلسلة نصية | استعلام | تحديد اسم مخزن الملفات الناتجة. |
| fontsLocation | سلسلة نصية | استعلام | استخدام خطوط مخصصة لملف PDF. |
| region | سلسلة نصية | استعلام | تحديد إعداد المنطقة لجدول البيانات. |
| password | سلسلة نصية | استعلام | كلمة المرور للوصول إلى ملف جدول البيانات. |

### **الاستجابة**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**عناوين استجابة نموذجية**

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="ConvertedTable.pdf"
Content-Length: 124578
```

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200 | ناجح | تمت تطبيق المرشح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مصرّح به | رمز JWT غير صالح أو مفقود. |
| 413 | حجم الحمولة كبير جدًا | تجاوز حجم الملف المرفوع الحد المسموح به. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## **أين يجب استخدام واجهة برمجة تطبيقات تحويل الجدول إلى PDF؟**

- **البيانات المالية**: تحويل ميزانيات العمليات، البيانات المالية (جداول محددة) إلى PDF لتوثيق جاهز للمراجعة.
- **تقارير المبيعات**: تحويل لوحات معلومات المبيعات أو حسابات العمولات إلى ملفات PDF قابلة للتوزيع.
- **مقاييس العمليات**: تصدير جداول مؤشرات الأداء الرئيسية (KPI) ومقاييس الأداء كتقارير رسمية بصيغة PDF.
- **البيانات التعاقدية**: تصدير جداول الأسعار واتفاقيات مستوى الخدمة من جداول البيانات إلى ملفات مُلحَقة بصيغة PDF.
- **سجلات التدقيق**: الاحتفاظ بجداول البيانات المالية كأدلة PDF غير قابلة للتعديل.
- **ملخّصات المحافظ**: تصدير جداول أداء الاستثمارات كبيانات PDF جاهزة للعملاء.
- **تقارير ضبط الجودة**: تصدير جداول بيانات الفحص إلى PDF لسجلات الامتثال.
- **ملخّصات المخزون**: تحويل جداول مستويات المخزون إلى PDF لمراجعة الإدارة.

## **لماذا يجب استخدام واجهة برمجة تطبيقات تحويل الجدول إلى PDF؟**

- **سهلة للمطورين**: تقدّم Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يمكّن من تطوير سريع، وتأتي مع وثائق شاملة. مقارنةً بإنشاء حلول مخصصة لعرض الرسوم البيانية، فإنها تقلل بشكل كبير من حجم العمل المطلوب في التطوير.
- **موفرة من حيث التكلفة**: يمكنك تحويل بيانات الجدول دون الحاجة مسبقًا لرفع الملف المحتوي على ورقة العمل، ما يوفر مساحة التخزين ويقلل التكاليف.
- **يحافظ على تنسيقات إكسل المعقدة** في تنسيق PDF قابل للوصول عالميًا.

## **كيفية استخدام واجهة برمجة تطبيقات تحويل الجدول إلى PDF باستخدام مكتبات SDK؟**

### مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى PDF

توفر [مواصفات واجهة برمجة تطبيقات تحويل الجدول إلى PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertTableToPDF) واجهة برمجة تطبيقات برمجية متاحة عمومًا لتنفيذ تفاعلات REST مباشرة من متصفح ويب.
يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء مكالمات لواجهة برمجة تطبيقات السحابة باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/table/pdf?worksheet=Sheet1&tableName=Table1" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@myWorkbook.xlsx" \
  -o converted.pdf
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (مشفرة بـ Base64)",
  "contentType": "نوع MIME",
  "fileDownloadName": "اسم ملف اختياري"
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبة SDK هو أسرع طريقة للتطوير، لأنها تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جدول جداول البيانات إلى ملف PDF باستخدام كود محدود. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertTableToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertTableToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertTableToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertTableToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertTableToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertTableToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertTableToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertTableToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}