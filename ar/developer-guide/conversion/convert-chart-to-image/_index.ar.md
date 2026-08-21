---
title: "واجهة Aspose.Cells Cloud Web API - تحويل مخطط Excel إلى صورة - أداة مجانية عبر الإنترنت"
second_title: "وثيقة"
ArticleTitle: "كيفية تحويل مخطط جدول البيانات إلى صورة: دليل خطوة بخطوة"
linktitle: "تحويل المخطط إلى صورة"
type: docs
url: /ar/convert-chart-to-image/
keywords: "تحويل المخطط إلى صورة، Aspose.Cells، تصدير مخطط Excel، PNG، SVG، JPEG، BMP، TIFF"
description: "استخدم واجهة Aspose.Cells Cloud Web API لتحويل مخطط Excel إلى صور PNG أو SVG أو TIFF أو JPEG أو BMP مباشرةً من ملف جدول البيانات."
weight: 100
---

مخططات Excel هي تمثيلات مرئية للبيانات يمكن تضمينها داخل أوراق العمل. يُمكّن تحويل هذه المخططات إلى تنسيقات الصور من إعادة استخدامها بسهولة عبر المستندات وصفحات الويب والتقارير دون الحاجة إلى Excel.

قم بتحويل مخطط من ملف جدول بيانات محلي أو ملف Excel إلى ملف صورة. **تنسيقات الصور المدعومة:** <a href="https://docs.fileformat.com/image/png/" rel="noopener noreferrer">PNG</a>، <a href="https://docs.fileformat.com/page-description-language/svg/" rel="noopener noreferrer">SVG</a>، <a href="https://docs.fileformat.com/image/tiff/" rel="noopener noreferrer">TIFF</a>، <a href="https://docs.fileformat.com/image/jpeg/" rel="noopener noreferrer">JPEG</a>، <a href="https://docs.fileformat.com/image/bmp/" rel="noopener noreferrer">BMP</a>

## **واجهة API لتحويل المخطط إلى صورة**

### واجهة API عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/image
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/chart/image?format=png&chartIndex=0" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@MyWorkbook.xlsx" \
     -o chart.png
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب:**

| اسم المعلمة | النوع | المسار/سلسلة الاستعلام/جسم HTTP | الوصف | الإلزام |
| :------------- | :------ | :------------------------- | :--------------------------------------------------------------------------------- | :------- |
| Spreadsheet | ملف | FormData | تحميل ملف جدول البيانات الذي يحتوي على المخطط. | نعم |
| worksheet | سلسلة نصية | استعلام | تحديد اسم ورقة العمل إن وُجد. | لا |
| chartIndex | عدد صحيح | استعلام | فهرس المخطط المراد تحويله. | نعم |
| format | سلسلة نصية | استعلام | (إلزامي) نوع الصورة المطلوب (مثل: svg، png، jpg). | نعم |
| outPath | سلسلة نصية | استعلام | (اختياري) مسار المجلد الذي سيتم تخزين ملف الإخراج فيه؛ الافتراضي هو null. | لا |
| outStorageName | سلسلة نصية | استعلام | اسم وحدة التخزين الخاصة بملف الإخراج. | لا |
| fontsLocation | سلسلة نصية | استعلام | تحديد الخطوط المخصصة عند الحاجة. | لا |
| region | سلسلة نصية | استعلام | ضبط منطقة جدول البيانات. | لا |
| password | سلسلة نصية | استعلام | كلمة المرور لفتح ملف جدول البيانات. | لا |

## **الاستجابة**

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

**رموز حالة HTTP**

| الرمز | المعنى | الوصف |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200 | ناجح | تم تطبيق التصفية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح | معلمات مفقودة أو غير صحيحة (مثل: نوع ملف غير مدعوم). |
| 401 | غير مصادق عليه | رمز JWT غير صالح أو مفقود. |
| 413 | حملة البيانات كبيرة جدًا | تجاوز حجم الملف المرفوع الحد المسموح. |
| 500 | خطأ داخلي في الخادم | خطأ غير متوقع في الخادم. |

## أين يجب استخدام واجهة API لتحويل المخطط إلى صورة؟

- **توليد التقارير واللوحات التفاعلية (Dashboards)**: تحويل المخططات تلقائيًا من بيانات Excel إلى صور (PNG وJPEG وما إلى ذلك) لتضمينها في تقارير PDF أو لوحات تفاعلية على الويب أو عروض PowerPoint.
- **تطبيقات الويب/البريد الإلكتروني**: عرض صور المخططات مباشرةً في صفحات الويب أو رسائل البريد الإلكتروني دون الحاجة إلى تنزيل أو فتح ملفات Excel. مفيد في أدوات التقارير الديناميكية أو النشرات الإخبارية أو الإشعارات الآلية.
- **سير عمل معالجة المستندات**: دمجها في خطوط أنابيب آلية (مثل: الفوترة أو التحليلات) حيث تكون الحاجة إلى إدراج مخططات من Excel في تنسيقات أخرى (Word أو PDF أو HTML) ضرورية.
- **تطبيقات الجوال/سطح المكتب**: عرض مخططات Excel في التطبيقات التي لا تتطلب عرض جدول البيانات بالكامل أو يكون ذلك غير عملي.
- **الأرشفة والتصور**: حفظ المخططات كصور منفصلة لتخزينها على المدى الطويل أو كصور مصغرة أو معاينات سريعة دون اعتماد على Excel.

## لماذا يجب استخدام واجهة API لتحويل المخطط إلى صورة؟

- **الحفاظ على الدقة البصرية**: تحافظ على تنسيق المخطط بالضبط (الألوان والتصنيفات والم масحات) كما تظهر في Excel، مما يضمن إخراجًا بجودة احترافية.
- **مستقلة عن المنصة**: لا حاجة لتثبيت Excel. تعمل عبر أنظمة التشغيل (Windows وLinux وmacOS) عبر واجهة API REST، مما يجعلها مناسبة للتطبيقات السحابية أو الخوادم.
- **الأتمتة والقابلية للتوسع**: تحويل جماعي لمخططات أو ملفات متعددة برمجيًا، مما يوفر الوقت مقارنةً بالتصدير اليدوي. معالجة كميات كبيرة بكفاءة في السحابة.
- **تنسيقات إخراج مرنة**: تدعم تنسيقات الصور الشائعة (PNG وJPG وBMP وSVG وما إلى ذلك)، مما يسمح بالتكامل مع أنظمة ووسائط متنوعة.
- **آمنة وموثوقة**: معالجة الملفات في بيئة سحابية تابعة لـ Aspose دون تعريض البيانات الحساسة لاستخدام أدوات من جانب العميل. توفر متانة عالية وأداءً ثابتًا.
- **سهلة للمطورين**: توفر Aspose.Cells Cloud مكتبات SDK بلغات برمجة متعددة، ما يُسهّل التطوير بسرعة، وتُرفق بتوثيق شامل. مقارنةً ببناء حلول تصور مخصصة للمخططات، فإن هذا يقلل بشكل كبير من جهد التطوير.
- **موفرة من حيث التكلفة**: يمكنك تحويل المخططات دون رفع كتاب العمل أولاً، مما يوفر مساحة التخزين ويقلل التكاليف.

## كيفية استخدام واجهة API لتحويل المخطط إلى صورة مع مكتبات SDK؟

### مواصفات واجهة API لتحويل المخطط إلى صورة

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToImage" rel="noopener noreferrer">مواصفات واجهة API لتحويل المخطط إلى صورة</a> تُعرّف واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### استخدام مكتبات SDK لـ Aspose.Cells Cloud

استخدام SDK هو أسرع طريقة للتطوير، حيث تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل المخطط إلى صورة باستخدام كود قصير.  
يرجى الاطلاع على <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للاطلاع على قائمة كاملة بمكتبات SDK لـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToImage.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToImage.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToImage.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToImage.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToImage.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToImage.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToImage.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToImage.go" >}}
{{</tab>}}
{{< /tabs >}}