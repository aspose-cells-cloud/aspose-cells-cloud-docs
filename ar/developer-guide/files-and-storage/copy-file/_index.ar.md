---
title: "واجهة برمجة تطبيقات نسخ الملفات في Aspose.Cells Cloud – واجهة لنسخ الملفات بسرعة وتنفيذ عمليات دفعّة لملفات إكسل في السحابة"
second_title: "مستند"
ArticleTitle: "حل إدارة ملفات إكسل القائم على السحابة – شرح مفصّل لوظيفة النسخ الدفعّي في واجهة برمجة تطبيقات نسخ الملفات Aspose.Cells"
linktype: "docs"
url: /ar/copy-file/
keywords: "Aspose.Cells، واجهة برمجة تطبيقات CopyFile، نسخ ملف إكسل، التخزين السحابي، واجهة برمجة تطبيقات REST"
description: "تعرّف على كيفية استخدام واجهة برمجة تطبيقات Aspose.Cells Cloud CopyFile لنسخ ملفات إكسل بكفاءة وإدارتها عبر مواقع تخزين مختلفة."
weight: 100
---

تتيح واجهة برمجة تطبيقات **copyFile** للمستخدمين نسخ ملف إكسل من مسار مصدر محدّد إلى مسار وجهة، وتدعم خيارات تخزين متعددة.

## **واجهة برمجة تطبيقات إكسل: نسخ ملف**

### واجهة برمجة التطبيقات عبر الويب

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **الأمان والمصادقة**

تُعدّ واجهات برمجة تطبيقات Aspose.Cells Cloud آمنة وتحتاج إلى <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معاملات الطلب لواجهة برمجة تطبيقات **copyFile** هي:

| اسم المعامل        | النوع   | المسار/سلسلة الاستعلام/جسم HTTP | الوصف                                                |
| ------------------ | ------- | ------------------------------- | ----------------------------------------------------- |
| srcPath            | String  | Path                            | مسار الملف المصدر الذي سيُنسَخ.                        |
| destPath           | String  | Query                           | مسار الوجهة حيث سيتم حفظ الملف.                        |
| srcStorageName     | String  | Query                           | اسم وحدة التخزين المصدر.                              |
| destStorageName    | String  | Query                           | اسم وحدة التخزين الوجهة.                              |
| versionId          | String  | Query                           | معرّف الإصدار الاختياري للملف المراد نسخه.            |

### **الاستجابة**

لا تُعيد العملية أي محتوى في حال النجاح. رموز حالة HTTP الشائعة هي:

**رموز حالة HTTP**

| الرمز | المعنى                 | الوصف                                                              |
| ----- | ----------------------- | ------------------------------------------------------------------- |
| 200   | ناجح (OK)               | تطبيق المرشّح بنجاح؛ تحتوي الاستجابة على تفاصيل العملية.          |
| 400   | طلب غير صالح (Bad Request) | معاملات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم).              |
| 401   | غير مفوّض (Unauthorized) | رمز JWT غير صالح أو مفقود.                                         |
| 413   | حملة البيانات كبيرة جدًا (Payload Too Large) | يتجاوز حجم الملف المرفوع الحدّ المسموح به.                        |
| 500   | خطأ داخلي في الخادم (Internal Server Error) | خطأ غير متوقّع في الخادم.                                          |

## كيفية استخدام واجهة برمجة تطبيقات نسخ الملف باستخدام مكتبات SDK؟

###仕様 واجهة برمجة تطبيقات نسخ الملف

يوفر <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile" rel="noopener noreferrer">仕様 واجهة برمجة تطبيقات نسخ الملف</a> واجهة برمجة تطبيقات مفتوحة للوصول عبر واجهة REST مباشرةً من متصفح ويب.

يمكنك استخدام أداة سطر الأوامر cURL للوصول إلى خدمات Aspose.Cells عبر الويب بسهولة. يوضح المثال التالي كيفية إجراء مكالمات إلى واجهة برمجة التطبيقات السحابية باستخدام cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="الطلب" tabName12="الاستجابة" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### استخدام مكتبات SDK الخاصة بـ Aspose.Cells Cloud

استخدام مكتبات SDK هو أسرع طريقة لتطوير التطبيقات، حيث تُجرّدك من التفاصيل منخفضة المستوى، مما يسمح لك بتحويل بيانات جداول البيانات إلى صور برمجيات قليلة جدًا من الكود. يُرجى مراجعة <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بمكتبات SDK الخاصة بـ Aspose.Cells Cloud.

توضّح أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر الويب باستخدام مكتبات SDK مختلفة:

---