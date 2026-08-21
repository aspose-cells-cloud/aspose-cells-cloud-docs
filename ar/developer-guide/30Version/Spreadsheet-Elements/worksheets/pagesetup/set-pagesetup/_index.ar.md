---
title: "ضبط إعدادات الصفحة لورقة عمل"
second_title: "مستند"
linktype: "ضبط إعدادات الصفحة"
type: docs
url: /ar/set-page-setup/
keywords: "Aspose.Cells, Excel, إعدادات الصفحة, REST API, ورقة عمل, SDK سحابي"
description: "تعرّف على كيفية ضبط إعدادات الصفحة لورقة عمل Excel باستخدام Aspose.Cells Cloud REST API. يشمل تفاصيل الطلب، مثال آمن لاستخدام cURL عبر HTTPS، رموز حالات الاستجابة، ومقتطفات من كود SDK تدعم لغات برمجة متعددة."
weight: 20
ArticleTitle: "ضبط إعدادات الصفحة لورقة عمل – دليل API السحابي Aspose.Cells"
---

متطلبات مسبقة: لاستدعاء هذه الواجهة البرمجية، يجب أن تمتلك رمز JWT (OAuth) صالحًا، كما يجب أن يكون الملف المصنف موجودًا في مساحة تخزين Aspose Cloud التي تمتلك صلاحيات القراءة والكتابة فيها. تأكد من تضمين الرمز في رأس **Authorization**، وأن حسابك يتمتع بحد كافٍ من الطلب المسموح به لواجهة API.

تقوم هذه الواجهة البرمجية REST بضبط إعدادات الصفحة لورقة عمل Excel.

## واجهة برمجة تطبيقات REST (REST API)

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagesetup
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### **معلمات الطلب**

| اسم المعلمة | النوع | الموقع | الوصف |
|------------|-------|--------|--------|
| name | string | path | اسم المستند. |
| sheetName | string | path | اسم ورقة العمل. |
| pageSetup | object | body | وصف إعدادات الصفحة. |
| folder | string | query | مجلد المستند. |
| storageName | string | query | اسم مساحة التخزين. |

**مثال على حمولة JSON لموضوع `pageSetup`**

```json
{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}
```

يُعرّف <a href="https://reference.aspose.cloud/cells/#/PageSetup/PostPageSetup" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> واجهة برمجة تطبيقات متاحة عمومًا، ويتيح لك تنفيذ تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب الخاصة بـ Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة API السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Tasks/pagesetup" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{
  "pageSetup": {
    "orientation": "Portrait",
    "paperSize": "A4",
    "fitToPagesTall": 1,
    "fitToPagesWide": 1,
    "centerHorizontally": true,
    "centerVertically": false
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

تعيد واجهة API كائن JSON يُظهر نتيجة العملية:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**رموز حالات الاستجابة المحتملة**

| الكود | المعنى | الحالة |
|-------|---------|--------|
| 200 | OK (تم بنجاح) | تم تحديث إعدادات الصفحة بنجاح |
| 400 | Bad Request (طلب غير صالح) | حمولة JSON غير صالحة أو حقول مطلوبة مفقودة |
| 401 | Unauthorized (غير مصرّح) | رمز JWT مفقود أو غير صالح |
| 404 | Not Found (غير موجود) | اسم الملف المصنف أو ورقة العمل غير موجود |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | فشل غير متوقع في الخادم |

## عائلة SDK السحابية

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير. يتعامل SDK مع التفاصيل منخفضة المستوى ويسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

توضح أمثلة الكود التالية كيفية إجراء مكالمات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مكتبات SDK مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostPageSetup.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostPageSetup.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostPageSetup.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostPageSetup.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostPageSetup.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostPageSetup.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostPageSetup.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostPageSetup.go" >}}

{{< /tab >}}

{{< /tabs >}}