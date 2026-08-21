---
title: "فتح ملفات إكسل"
second_title: "مستند"
linktitle: "فتح ملفات إكسل"
type: docs
url: /ar/unlock-excel-files/
aliases: [  /ar/unlock/without-storage/ , /ar/unlock/ , /ar/unlock/without-using-storage/ ]
keywords: "فتح إكسل، Aspose.Cells Cloud، REST API، فتح ملفات إكسل، مصنف محمي بكلمة مرور، SDK، C#، Java، Python، Node.js، Go، PHP، Ruby، Swift"
description: "توفر واجهة Aspose.Cells Cloud REST نقطة نهاية لفتح ملفات إكسل المحمية بكلمة مرور. تتوفر وحدات التطوير البرمجي (SDKs) لعدة لغات برمجة، تشمل Android، C#، Go، Java، Node.js، Perl، PHP، Python، Ruby، و Swift."
ArticleTitle: "فتح ملفات إكسل باستخدام واجهة Aspose.Cells Cloud REST API"
weight: 70
---

تقوم هذه الواجهة (REST API) بفتح ملفات إكسل.

## واجهة REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### الأمان والمصادقة

تُعتبر واجهات Aspose.Cells Cloud آمنة وتتطلب [المصادقة باستخدام رمز JWT](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### معاملات الطلب

| اسم المعامل | النوع | الموقع | الوصف |
|------------|--------|---------|--------|
| file | ملف | formData (جسم HTTP) | الملف المراد رفعه |
| password | نص | سلسلة الاستعلام | كلمة المرور لفتح الملف (إن وُجدت) |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**كُودات حالة HTTP**

| الكود | المعنى | الوصف |
|-------|---------|--------|
| 200 | نجاح (OK) | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401 | غير مُعتمد (Unauthorized) | رمز JWT غير صالح أو مفقود. |
| 413 | حمل البيانات كبير جدًا (Payload Too Large) | حجم الملف المرفوع يتجاوز الحد المسموح. |
| 500 | خطأ داخلي في الخادم (Internal Server Error) | حدث خطأ غير متوقع في الخادم. |

## كيفية استخدام PostUnlock API باستخدام وحدات التطوير البرمجي (SDKs)

### مواصفات PostUnlock API

تُعرّف [مواصفات OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) واجهة برمجة قابلة للوصول العام وتتيح لك إجراء تفاعلات REST مباشرة من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر `cURL` للوصول بسهولة إلى خدمات ويب Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة Cloud API باستخدام `cURL`.

{{< tabs tabTotal="2" tabID="1" tabName1="الطلب" tabName2="الاستجابة" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام وحدات التطوير البرمجي (SDKs) لـ Aspose.Cells Cloud

يعتبر استخدام وحدات التطوير البرمجي (SDKs) أفضل طريقة لتسريع عملية التطوير، فهي تتعامل مع التفاصيل منخفضة المستوى وتركز أنت على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بوحدات Aspose.Cells Cloud SDK.

**ملاحظات:**  
- يمكن للواجهة فتح عدة ملفات إكسل في طلب واحد؛ ويُعاد كل ملف في مصفوفة `Files` ضمن الاستجابة.  
- تأكد من أن إصدار وحدة SDK يتوافق مع إصدار الواجهة (`v3.0`) لتجنب مشاكل التوافق.

تُظهر أمثلة الشيفرة التالية كيفية إجراء استدعاءات لخدمات ويب Aspose.Cells باستخدام SDKs مختلفة:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}