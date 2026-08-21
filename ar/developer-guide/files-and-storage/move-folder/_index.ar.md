---
title: "واجهة برمجة تطبيقات نقل المجلدات في Aspose.Cells Cloud – نقل المجلدات بسرعة في السحابة"
second_title: "مستند"
ArticleTitle: "إدارة ملفات إكسل عبر السحابة – نقل المجلدات بسرعة في السحابة"
linktype: "move-folder"
type: docs
url: /ar/move-folder/
keywords: "Aspose.Cells, نقل المجلد, التخزين السحابي, واجهة برمجة تطبيقات إكسل"
description: "تعرّف على كيفية نقل المجلدات في تخزين Aspose.Cells Cloud باستخدام واجهة برمجة تطبيقات نقل المجلدات عبر REST. يشمل ذلك عنوان URL للنقطة الطرفية، المعاملات، مثال على cURL، رموز الأخطاء، وأمثلة لـ SDK بلغات C#، Java، Python، وأكثر من ذلك."
weight: 100
---

تقوم هذه الواجهة بتحريك مجلد من موقع إلى آخر داخل تخزين Aspose.Cells Cloud. وهي تساعد في تنظيم الملفات وإدارة التخزين السحابي بكفاءة.

## **واجهة برمجة تطبيقات إكسل: نقل المجلد**

### واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

**مثال على طلب cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/FolderA?destPath=FolderB" \
     -H "Authorization: Bearer {access_token}"
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات طلب واجهة برمجة التطبيقات **moveFolder**

| اسم المعامل      | النوع   | الموقع | الوصف                                                             |
| ---------------- | ------- | ------ | ------------------------------------------------------------------ |
| srcPath          | string  | Path   | المسار الكامل للمجلد المراد نقله، مثال: `FolderA/`.               |
| destPath         | string  | Query  | المسار الوجهة الذي سيتم نقل المجلد إليه، مثال: `FolderB/`.        |
| srcStorageName   | string  | Query  | (اختياري) اسم وحدة التخزين المصدر.                                 |
| destStorageName  | string  | Query  | (اختياري) اسم وحدة التخزين الوجهة.                                 |

**تفاصيل المعاملات**

- **srcPath** – إلزامي. مسار المجلد المصدر.
- **destPath** – إلزامي. مسار المجلد الوجهة.
- **srcStorageName** – اختياري. مُعرّف وحدة التخزين المصدر.
- **destStorageName** – اختياري. مُعرّف وحدة التخزين الوجهة.

### **الاستجابة**

في حال النجاح، تُعيد الواجهة جسم استجابة فارغ مع رمز الحالة HTTP **200 OK**. أما في حالة حدوث أخطاء، فتُعاد ككائنات JSON تحتوي على حقل `error`.

**رموز حالة HTTP**

| رمز HTTP | حالة HTTP                | الوصف                                                              |
| --------- | ------------------------ | ------------------------------------------------------------------- |
| 200       | OK (نجاح)               | تم استدعاء واجهة برمجة التطبيقات بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400       | Bad Request (طلب خاطئ)  | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).              |
| 401       | Unauthorized (غير مخوّل) | رمز JWT غير صالح أو مفقود.                                         |
| 413       | Payload Too Large (حمولة كبيرة جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.                         |
| 500       | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                          |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يُظهر المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="طلب" tabName12="استجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

يُعد استخدام SDK أفضل طريقة لتسريع عملية التطوير، حيث تُهتم SDK بمعالجة التفاصيل منخفضة المستوى وتسمح لك بالتركيز على مهام مشروعك. يُرجى مراجعة [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الرمز التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مكتبات SDK المختلفة: