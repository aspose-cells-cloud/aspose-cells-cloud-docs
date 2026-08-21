---
title: "واجهة برمجة تطبيقات نقل الملفات في Aspose.Cells Cloud – حل فعّال لإدارة ملفات Excel السحابية"
second_title: "مستند"
ArticleTitle: "حل فعّال لإدارة ملفات Excel سحابيًا – واجهة لنقل الملفات بسرعة في السحابة"
linktype: "move-file"
type: docs
url: /ar/move-file/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات نقل الملفات، التخزين السحابي، واجهة برمجة تطبيقات Excel، إدارة الملفات"
description: "كيفية نقل الملفات بين مجلدات في تخزين Aspose.Cells Cloud باستخدام واجهة برمجة تطبيقات نقل الملفات الإصدار 4.0 – نقاط النهاية، المعاملات، أمثلة، وروابط SDKs."
weight: 100
---

واجهة برمجة التطبيقات **moveFile** تقوم بنقل ملف من موقع إلى آخر داخل تخزين Aspose.Cells Cloud. وتساعدك هذه الواجهة على تنظيم الملفات وإدارة التخزين بكفاءة.

## **واجهة برمجة تطبيقات Excel: نقل الملفات**

### واجهة برمجة التطبيقات عبر الويب

```bash
PUT https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **الأمان والمصادقة**

واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### معاملات طلب واجهة برمجة التطبيقات **moveFile**

| اسم المعامل       | النوع   | المسار / سلسلة الاستعلام / جسم HTTP | الوصف                                              |
| ----------------- | ------- | ---------------------------------- | --------------------------------------------------- |
| srcPath           | String  | Path                               | المسار المصدري للملف المراد نقله.                   |
| destPath          | String  | Query                              | المسار الوجهة الذي سيتم نقل الملف إليه.             |
| srcStorageName    | String  | Query                              | اسم مساحة التخزين المصدري، إن وُجد.                 |
| destStorageName   | String  | Query                              | اسم مساحة التخزين الوجهة، إن وُجد.                   |
| versionId         | String  | Query                              | معرّف الإصدار للملف، إن وُجد.                        |

### **الاستجابة**

تُعيد الطلب الناجح رمز الحالة **HTTP 200 OK** مع جسم JSON فارغ.

```json
{}
```

**رموز حالة HTTP**

| رمز HTTP | حالة HTTP             | الوصف                                                                |
| --------- | --------------------- | -------------------------------------------------------------------- |
| 200       | OK (تم بنجاح)         | تم استدعاء واجهة برمجة التطبيقات بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400       | Bad Request (طلب خاطئ) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).               |
| 401       | Unauthorized (غير مُصرّح) | رمز JWT غير صالح أو مفقود.                                          |
| 413       | Payload Too Large (حجم الحمولة كبير جدًا) | تجاوز حجم الملف المرفوع الحد المسموح به.                             |
| 500       | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم.                                            |

## مواصفات OpenAPI

تُعرّف [مواصفات OpenAPI](https://reference.aspose.cloud/cells/#/FileController/MoveFile) واجهة برمجة تطبيقات متاحة علنًا وتتيح لك إجراء تفاعلات REST مباشرة من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات الويب Aspose.Cells بسهولة. يوضح المثال التالي كيفية إجراء المكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}?destPath={destPath}" \
     -H "Authorization: Bearer {access_token}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{}
```

{{< /tab >}}

{{< /tabs >}}

استخدام SDK هو أفضل طريقة لتسريع عملية التطوير، حيث تهتم SDK بتفاصيل المستوى المنخفض وتتيح لك التركيز على مهام مشروعك. يُرجى الاطلاع على [مستودع GitHub](https://github.com/aspose-cells-cloud) للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية إجراء مكالمات إلى خدمات الويب Aspose.Cells باستخدام مكتبات SDK مختلفة:

---