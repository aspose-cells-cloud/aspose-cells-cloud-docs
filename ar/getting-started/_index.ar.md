---
title: "البدء باستخدام واجهة Aspose.Cells Cloud API – معالجة ملفات إكسل في 3 خطوات بسيطة"
second_title: "وثيقة"
ArticleTitle: "البدء مع Aspose.Cells Cloud"
linktitle: "البدء"
type: docs
url: /ar/getting-started/
description: "تعرّف على كيفية رفع وتحويل وتنزيل ملفات إكسل باستخدام واجهة Aspose.Cells Cloud REST API في ثلاث خطوات بسيطة. يتضمن أمثلة لرموز cURL."
weight: 10
keywords: "Aspose.Cells Cloud, Excel API, spreadsheet conversion, Excel to PDF, cloud spreadsheet, Aspose.Cells Cloud API"
---

- [نظرة عامة](/cells/overview/)
- [البدء السريع](/cells/quickstart/)
- [حزم التطوير المتوفرة (SDKs)](/cells/available-sdks/)
- [المنصات المدعومة](/cells/supported-platforms/)
- [تنسيقات الملفات المدعومة](/cells/supported-file-formats/)
- [تجربة Aspose.Cells Cloud](/cells/evaluate-aspose-cells/)
- [خطة التسعير](/cells/pricing-plan/)
- [الدعم الفني](/cells/technical-support/)
- [كيفية تشغيل حاوية Docker](/cells/how-to-run-docker-container/)

**دليل البدء**

قبل البدء، تأكّد من امتلاك **مفتاح API صالح لـ Aspose Cloud** و**اسم التخزين**. تُعد هذه البيانات الاحترافية مطلوبة لجميع استدعاءات API اللاحقة.

**الخطوة 1: رفع ملف إكسل**  
ارفع ملف المصنف المصدر إلى تخزين Aspose Cloud.

```curl
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/{path}" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/octet-stream" \
     --data-binary @sample.xlsx
```

*جسم الطلب*: يُرسل الملف كدفق ثنائي (`application/octet‑stream`).  
*المعلمات المطلوبة*:

- `path` – مسار التخزين الذي سيتم حفظ الملف فيه (مثال: `folder/sample.xlsx`).

**الخطوة 2: تحويل المصنف إلى PDF**  
أرسل طلب التحويل بعد تخزين الملف.

```curl
curl -X POST "https://api.aspose.cloud/v4.0/cells/{name}/saveas?format=pdf&outPath={outputPath}" \
     -H "Authorization: Bearer {access_token}"
```

*المعلمات المطلوبة*:

- `name` – اسم المصنف المرفوع (مثال: `sample.xlsx`).
- `format` – تنسيق الهدف (`pdf`).
- `outputPath` – مسار التخزين لملف الناتج المحول (مثال: `folder/result.pdf`).

*نموذج استجابة JSON*:

```json
{
  "status": "OK",
  "outputPath": "folder/result.pdf"
}
```

**الخطوة 3: تنزيل ملف PDF المحول**  
احصل على ملف PDF الناتج من التخزين.

```curl
curl -X GET "https://api.aspose.cloud/v4.0/cells/storage/file/{outputPath}" \
     -H "Authorization: Bearer {access_token}" \
     -o result.pdf
```

*المعلمات المطلوبة*:

- `outputPath` – مسار ملف PDF الذي تم إنشاؤه في الخطوة السابقة.

**ملخص أمثلة الطلب والاستجابة**

| العملية | طريقة HTTP | النقطة الطرفية (مثال) | المعلمات | حالة النجاح |
|----------|-------------|------------------------|-------------|----------------|
| الرفع | PUT | /cells/storage/file/{path} | `path` (مكان التخزين) | 200 OK |
| التحويل | POST | /cells/{name}/saveas?format=pdf&outPath={outputPath} | `name`, `format`, `outPath` | 200 OK |
| التنزيل | GET | /cells/storage/file/{outputPath} | `outputPath` | 200 OK |

**أكواد الأخطاء الشائعة**

- **400 Bad Request** – معلمات مفقودة أو غير صالحة.  
- **401 Unauthorized** – رمز وصول غير صالح أو مفقود.  
- **404 Not Found** – الملف أو المسار المحدّد غير موجود.  
- **500 Internal Server Error** – خطأ غير متوقع في الخادم؛ حاول إعادة المحاولة أو اتصل بالدعم.  
---