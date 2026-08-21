---
title: "حذف الأعمدة الفارغة من ملفات إكسل باستخدام واجهة Aspose.Cells Cloud API – مثال سريع لواجهة REST"
second_title: "وثيقة"
ArticleTitle: "كيف تحذف الأعمدة الفارغة من ملفات إكسل – أتمتة تنظيف الأعمدة"
linktype: "حذف الأعمدة الفارغة"
type: docs
url: /ar/delete-spreadsheet-blank-columns/
keywords: "واجهة حذف الأعمدة الفارغة في إكسل، Aspose.Cells Cloud، واجهة REST، تنظيف ملفات إكسل، أتمتة الجداول المحسوبة"
description: "تعلم كيفية إزالة الأعمدة الفارغة من ملفات إكسل باستخدام واجهة Aspose.Cells Cloud REST API. يتضمن نقطة نهاية API، وتفاصيل المصادقة، وأمثلة على الطلبات والاستجابات، وأكواد SDK بلغات C#، Java، Python، والمزيد."
weight: 100
---

استخدم واجهة Aspose.Cells Cloud API لحذف جميع الأعمدة الفارغة من الجداول المحسوبة في ملفات إكسل تلقائيًا. تكتشف واجهة API الذكية الأعمدة التي لا تحتوي على أي بيانات أو صيغ أو تعليقات أو مخططات أو كائنات، ثم تزيلها. تدعم الواجهة معالجة الدفعات، والأتمتة في السحابة، والتكامل السلس عبر REST لتنفيذ سير عمل تنظيف الجداول المحسوبة بمستوى مؤسسي.

**الخلفية:**  
غالبًا ما تظهر الأعمدة الفارغة بعد عمليات استيراد البيانات، أو توليد القوالب، أو ترحيل الملفات القديمة. يؤدي إزالة هذه الأعمدة الفارغة إلى تحسين حجم الملف، وأداء العرض، ودقة معالجة البيانات في الخطوات اللاحقة. وتوفّر واجهة حذف الأعمدة الفارغة من الجداول المحسوبة وسيلة سريعة وتعمل على الخادم لإزالة الفراغات من الجداول دون الحاجة للتعديل اليدوي.

## **واجهة DeleteSpreadsheetBlankColumns API**

### واجهة الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/delete/blank-columns
```

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات الطلب

| اسم المعامل         | النوع  | الموقع                         | الوصف                                                                                                                                   |
|--------------------|--------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Spreadsheet**    | ملف    | بيانات النموذج (multipart)      | ملف مصنف إكسل الذي سيتم معالجته.                                                                                                        |
| **outPath**        | نص    | الاستعلام (Query)              | اختياري. المجلد الوجهة في التخزين السحابي لحفظ الملف بعد التنظيف. إذا تم تجاهله، فسيُعاد الملف الناتج في جسم الاستجابة.                 |
| **outStorageName** | نص    | الاستعلام (Query)              | اختياري. اسم التخزين السحابي الذي يجب حفظ الناتج فيه.                                                                                 |
| **region**         | نص    | الاستعلام (Query)              | اختياري. معرّف اللغة والمنطقة (مثل `en-US`، `de-DE`).                                                                                  |
| **password**       | نص    | الاستعلام (Query)              | اختياري. كلمة المرور اللازمة لفتح مصنف محمي.                                                                                          |

### الاستجابة

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

### رموز الأخطاء

- **400 Bad Request** – معاملات طلب غير صالحة أو URI غير مهيأ بشكل صحيح.
- **401 Unauthorized** – رمز وصول مفقود أو غير صالح.
- **404 Not Found** – تعذر العثور على الملف المحدد.
- **500 Server Error** – شرط غير متوقع منع واجهة API من معالجة الملف.

## متى تستخدم واجهة Delete Spreadsheet Blank Columns API

- **سير عمل استيراد البيانات والتنظيف** – احذف الأعمدة الفارغة الزائدة أو البنيوية فور تحميل البيانات من ملفات CSV أو قواعد البيانات أو واجهات ويب.
- **توليد التقارير واللوحات التفاعلية** – تأكد من أن التقارير النهائية تمتاز بمظهر نظيف خالٍ من الأعمدة الفارغة غير الضرورية.
- **خطوط أنابيب ETL** – قم بالمعالجة الأولية لملفات إكسل قبل تحميلها في مستودعات البيانات مثل Snowflake أو BigQuery.
- **دمج الأنظمة** – قم بتوحيد ملفات إكسل التي يُوفّرها الشركاء قبل معالجتها لاحقًا.
- **أتمتة المستندات بالدفعات** – احذف الأعمدة الوهمية من القوالب المُولّدة دفعة واحدة.
- **المحتوى المُنشأ من قبل المستخدمين** – نظّف ملفات إكسل المرفوعة من منصات الويب قبل تخزينها أو تحليلها.
- **ترحيل البيانات القديمة** – بسّط أرشيفات الجداول المحسوبة القديمة بإزالة الأعمدة الفارغة تاريخيًا.

## لماذا تستخدم هذه الواجهة؟

- **سهلة الاستخدام للمطورين** – توفر SDKs للغات C#، Java، Python، PHP، Ruby، Node.js، Go، ومزيد من اللغات، ما يقلل جهود التطوير.
- **فعّالة من حيث التكلفة** – نموذج الدفع حسب الاستخدام يلغي تكاليف البنية التحتية المقدمة.
- **خالية من الصيانة** – لا حاجة لإدارة خوادم؛ يتم تحديث الخدمة باستمرار من قِبل Aspose.

## كيفية استخدام واجهة Delete Spreadsheet Blank Columns API مع SDKs

### مواصفات الواجهة

توفر [مواصفات واجهة حذف الأعمدة الفارغة من الجداول المحسوبة](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/RemoveSpreadsheetBlankColumns) تعريف OpenAPI الكامل وأمثلة عليه.

### استخدام SDKs لـ Aspose.Cells Cloud

تُجرّد SDKs من تفاصيل HTTP منخفضة المستوى، مما يسمح لك بحذف الأعمدة الفارغة باستخدام بضعة أسطر فقط من الكود. يمكنك الاطلاع على القائمة الكاملة للغات المدعومة في مستودع GitHub الرسمي: <https://github.com/aspose-cells-cloud>.

تُظهر أمثلة الكود التالية كيفية استدعاء الواجهة باستخدام SDKs مختلفة:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteSpreadsheetBlankColumns.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteSpreadsheetBlankColumns.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteSpreadsheetBlankColumns.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteSpreadsheetBlankColumns.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteSpreadsheetBlankColumns.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteSpreadsheetBlankColumns.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteSpreadsheetBlankColumns.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteSpreadsheetBlankColumns.go" >}}
{{</tab>}}
{{< /tabs >}}
---