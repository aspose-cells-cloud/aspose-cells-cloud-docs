---
title: "Aspose.Cells Cloud SDK for Perl – تحويل، دمج، تقسيم، حماية والمزيد"
second_title: "مستند"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – تحويل، دمج، تقسيم، حماية والمزيد"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /ar/available-sdks/aspose-cells-cloud-perl/
description: "استكشف Aspose.Cells Cloud Perl SDK – مكتبة متعددة المنصات لإنشاء وتحويل ودمج وتقسيم وحماية وبحث واستبدال ملفات إكسل دون الحاجة إلى تثبيت أوفيس. يشمل دليل التثبيت وأمثلة الكود ومراجع الواجهة البرمجية."
weight: 30
keywords: "Perl, Aspose.Cells Cloud, Excel SDK, تحويل, PDF, API, معالجة إكسل, Perl SDK, معالجة إكسل في السحابة"
---

_تم التحديث الأخير في 30 يوليو 2026_

تُعتبر المكتبة مفتوحة المصدر ومرخصة بموجب ترخيص MIT. يمكنك الوصول إلى كود مصدَّر مكتبة Aspose.Cells Cloud لـ Perl [هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **كيفية استخدام مكتبة Aspose.Cells Cloud لغة Perl**

يُعد Aspose.Cells Cloud SDK for Perl مكتبة قوية تتيح للمطورين التلاعب ومعالجة ملفات مايكروسوفت إكسل باستخدام لغة البرمجة Perl. وباستخدام هذه المكتبة، يمكنك إنشاء وتعديل وتحويل مستندات إكسل في السحابة، دون الحاجة لتثبيت أي برامج إضافية أو تبعيات على جهازك المحلي.

في هذه المقالة، سنستعرض كيفية استخدام Aspose.Cells Cloud SDK for Perl لإنجاز بعض المهام الشائعة، مثل إنشاء ملف إكسل جديد، وإدخال بيانات في الخلايا، وحفظ الملف المعدّل في السحابة.

## البدء

قبل البدء باستخدام Aspose.Cells Cloud SDK لغة **Perl**، تحتاج إلى إعداد بيئة التطوير وتثبيت التبعيات المطلوبة. راجع **[دليل البدء السريع لـ Aspose.Cells Cloud](https://docs.aspose.cloud/cells/quickstart/)** على موقع Aspose للحصول على معرّف العميل (client ID) ومعرّف سر العميل (client secret) الخاصين بك.

## كيفية تثبيت حزمة Perl الخاصة بـ Aspose.Cells Cloud

**متطلبات مسبقة**  
- Perl الإصدار 5.10 أو أحدث  
- تثبيت CPAN (شبكة أرشيف Perl الشاملة)  
- معرّف عميل (client ID) وسر عميل (client secret) ساري المفعول لـ Aspose.Cells Cloud  

يمكنك تثبيت Aspose.Cells Cloud SDK لغة Perl باستخدام الأمر التالي:

```perl
perl -MCPAN -e shell
install AsposeCellsCloud::CellsApi
```

## كيفية استخدام حزمة Perl لتحويل ملف Xlsx إلى صيغ أخرى

- **استيراد مكتبة Aspose.Cells Cloud**  
  ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud Perl SDK إلى مشروعك.

- **إعداد عميل الواجهة البرمجية بالبيانات الاحصائية المطلوبة**  
  مصادقة عميل الواجهة البرمجية باستخدام معرّف العميل وسر العميل الفريدَين الخاصين بك.

- **إعداد معلمات التحويل**  
  عرّف المعلمات الخاصة بمهمة التحويل، بما في ذلك اسم ملف المصدر، وصيغة الإخراج المطلوبة، ومسار مجلد التخزين.

- **تنفيذ عملية تحويل الملف**  
  نفّذ عملية التحويل باستخدام الطريقة `PostConvertWorkbook` وتعامل مع الاستجابة.

فيما يلي مرجع موجز لعملية `PostConvertWorkbook`:

| طريقة HTTP | نقطة النهاية                           | المعلمات المطلوبة                                 | مثال على الطلب (Perl)                                                                                         | مثال على الاستجابة (JSON)                               | رموز الحالة الممكنة |
|-----------|----------------------------------------|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|---------------------|
| POST      | `/cells/convert`                       | `file` (ملف العمل المصدر)، `outputFormat`، `storage` | ```perl\nmy $result = $api_instance->post_convert_workbook({ file => 'Book1.xlsx', outputFormat => 'pdf', storage => 'MyStorage' });\n``` | `{ "File": "Book1.pdf", "Url": "https://.../Book1.pdf" }` | 200 OK، 400 Bad Request، 401 Unauthorized، 500 Server Error |

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}