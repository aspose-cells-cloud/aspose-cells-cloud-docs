---
title: "واجهة برمجة تطبيقات نسخ المجلد في Aspose.Cells Cloud – نسخ سريع للمجلدات في السحابة"
second_title: "مستند"
ArticleTitle: "حل إدارة ملفات إكسل عبر السحابة – شرح مفصّل لوظيفة النسخ الدفعي في واجهة برمجة تطبيقات نسخ المجلد في Aspose.Cells Cloud"
linktype: "docs"
url: /ar/copy-folder/
keywords: "نسخ المجلد، Aspose.Cells Cloud، واجهة برمجة تطبيقات REST، تخزين سحابي، إدارة جداول البيانات"
description: "تعرّف على كيفية نسخ مجلدات داخل تخزين Aspose.Cells Cloud باستخدام استدعاء REST واحد فقط. يشمل الرابط endpoint، المعلَمات، طلبات مثال، رموز الأخطاء، وأمثلة لواجهات برمجة تطبيقات (SDKs)."
weight: 100
---

تُكرّر واجهة برمجة تطبيقات **CopyFolder** مجلدًا موجودًا داخل تخزين Aspose.Cells Cloud. وتُستخدم هذه الوظيفة عادةً لإنشاء نسخ احتياطية، أو إعادة تنظيم البيانات، أو إعداد هيكل المجلدات لمعالجة لاحقة دون الحاجة لنقل الملفات يدويًا.

## **واجهة برمجة تطبيقات إكسل: نسخ المجلد**

### واجهة برمجة التطبيقات عبر الويب

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **الأمان والمصادقة**

تتّسم واجهات برمجة تطبيقات Aspose.Cells Cloud بالأمان، وتشترط <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة مبنية على رمز JWT</a>.

### تقبل واجهة برمجة تطبيقات CopyFolder المعلَمات التالية:

| اسم المعلَمة       | مطلوبة | النوع   | الموقع (مسار/استعلام) | الوصف                                                                 |
| ------------------ | ------ | ------- | --------------------- | --------------------------------------------------------------------- |
| `srcPath`          | نعم     | سلسلة  | المسار                | مسار المجلد المصدر الذي سيتم نسخه.                                   |
| `destPath`         | نعم     | سلسلة  | الاستعلام            | المسار الذي سيتم إنشاء المجلد الجديد فيه.                            |
| `srcStorageName`   | لا      | سلسلة  | الاستعلام            | اسم التخزين الذي يحتوي على المجلد المصدر.                             |
| `destStorageName`  | لا      | سلسلة  | الاستعلام            | اسم التخزين الوجهة الذي يجب نسخ المجلد إليه.                          |

### استجابة مثال

يعيد الاستدعاء الناجح رمز الحالة **HTTP 200** مع جسم JSON فارغ:

```json
{}
```

**طلب مثال باستخدام cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**رموز حالات HTTP**

| الرمز | المعنى                  | الوصف                                                        |
| ----- | ------------------------ | ------------------------------------------------------------- |
| 200   | ناجح (OK)               | تم تطبيق الفلتر بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.   |
| 400   | طلب غير صحيح (Bad Request) | معلَمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).         |
| 401   | غير مصادق عليه (Unauthorized) | رمز JWT غير صالح أو مفقود.                                   |
| 413   | حجم الحمولة كبير جدًا (Payload Too Large) | تجاوز حجم الملف المرفوع الحد المسموح به.                      |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقع في الخادم.                                     |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) واجهة برمجة تطبيقات عامة قابلة للوصول، وتتيح لك تنفيذ تفاعلات REST مباشرةً من خلال متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول بسهولة إلى خدمات الويب الخاصة بـ Aspose.Cells. يوضح المثال التالي كيفية إجراء استدعاءات لواجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

استخدام واجهة برمجة التطبيقات (SDK) هو أفضل طريقة لتسريع عملية التطوير، إذ تعتني واجهة برمجة التطبيقات بتفاصيل المستوى المنخفض، مما يسمح لك بالتركيز على مهام مشروعك. يُرجى الاطّلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بواجهات برمجة تطبيقات (SDKs) الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية إجراء استدعاءات لخدمات الويب الخاصة بـ Aspose.Cells باستخدام مختلف واجهات برمجة التطبيقات (SDKs):

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}