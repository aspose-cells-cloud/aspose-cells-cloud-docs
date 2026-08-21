---
title: "Aspose.Cells Cloud SDK for Java: تحويل، دمج، تقسيم، حماية، بحث، استبدال، وأكثر من ذلك"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Java: تحويل، دمج، تقسيم، حماية، بحث، استبدال، وأكثر من ذلك"
linktitle: "Aspose.Cells Cloud SDK for Java"
type: docs
url: /ar/available-sdks/aspose-cells-cloud-java/
description: "استخدم Aspose.Cells Cloud Java SDK لإنشاء وتحويل ودمج وتقسيم وحماية وبحث واستبدال ملفات Excel دون الحاجة إلى تثبيت Office."
weight: 30
keywords: "Aspose Cells Java SDK، تحويل Excel بـ Java، واجهة برمجة تطبيقات جداول البيانات في السحابة، مكتبة Java لملفات Excel، Aspose.Cells Cloud Java"
---


يُعد SDK مفتوح المصدر ومرخّص بموجب ترخيص MIT. يمكنك الاطّلاع على كود مكتبة Java لـ Aspose.Cells Cloud [هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **كيفية استخدام مكتبة Aspose.Cells Cloud لـ Java**

تُعد مكتبة Aspose.Cells Cloud SDK for Java مكتبة قوية تتيح للمطورين تنسيق ومعالجة ملفات مايكروسوفت إكسل باستخدام لغة البرمجة جافا. وباستخدام هذا SDK، يمكنك إنشاء وتعديل وتحويل مستندات Excel في السحابة، دون الحاجة إلى تثبيت أي برامج إضافية أو تبعيات على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Java لأداء بعض المهام الشائعة، مثل إنشاء ملف Excel جديد، وإدراج البيانات في الخلايا، وحفظ الملف المعدّل في السحابة.

## البدء

قبل أن تبدأ باستخدام Aspose.Cells Cloud SDK for Java، يجب إعداد بيئة التطوير وتثبيت التبعيات الضرورية. راجع [المقالة](https://docs.aspose.cloud/cells/quickstart/) على موقع Aspose للحصول على معرّف العميل وسر معرّف العميل.

## كيفية استخدام Maven لإضافة التبعيات الخاصة بـ Aspose.Cells Cloud

في مشروع Maven الخاص بك، أضف التبعيات الخاصة بـ Aspose.Cells Cloud SDK. ضع التبعيات التالية في ملف pom.xml:

**مستودع Aspose Maven**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**تبعية Maven**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## كيفية استخدام حزمة Java لتحويل ملف Xlsx إلى PDF

- استيراد مكتبة Aspose.Cells Cloud  
  ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud Java SDK إلى مشروعك.
- تهيئة عميل API باستخدام بيانات الاعتماد  
  قم بمصادقة عميل API الخاص بك باستخدام معرّف العميل وسر معرّف العميل الفريدين الخاصين بك.
- إعداد معاملات عملية التحويل  
  حدد المعاملات اللازمة لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ عملية تحويل Workbook  
  استدعِ عملية التحويل باستخدام الطريقة PostConvertWorkbook، وتعامل مع الاستجابة.

### **كود مثال**

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_AvailableSDKs.java" >}}