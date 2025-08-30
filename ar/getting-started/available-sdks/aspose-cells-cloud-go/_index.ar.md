---
title: Aspose.Cells مجموعة تطوير البرامج السحابية لنظام G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-go/
description: توفر مجموعة تطوير البرامج السحابية Aspose.Cells للغة Go دعمًا قويًا متعدد المنصات لمطوري Go، مما يسهل دمجها واستخدامها مع أنظمة Windows وLinux وmacOS. كما تدعم Excel إنشاء الكائنات وتحويلها ودمجها وتقسيمها وحمايتها وتشغيل الكائنات الداخلية، وما إلى ذلك.
weight: 30
kwords: Go، Excel، Office Cloud، REST API، مخطط، جدول محوري، جدول، جدول بيانات، PDF، CSV، Json، Markdown
---
 مجموعة تطوير البرامج (SDK) مفتوحة المصدر ومرخصة بموجب ترخيص معهد ماساتشوستس للتكنولوجيا (MIT). يمكنك الوصول إلى الكود المصدري لمكتبة Go لـ Aspose.Cells Cloud.[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **كيفية استخدام مكتبة Go من Aspose.Cells Cloud**

مجموعة تطوير البرامج السحابية Aspose.Cells للغة Go هي مكتبة فعّالة تُمكّن المطورين من التعامل مع ملفات Microsoft Excel ومعالجتها باستخدام لغة برمجة Go. باستخدام هذه المجموعة، يُمكنك إنشاء مستندات Excel وتحريرها وتحويلها في السحابة، دون الحاجة إلى تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Go لأداء بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## **ابدء**

 قبل أن تتمكن من استخدام حزمة تطوير البرامج السحابية Aspose.Cells للغة Go، عليك إعداد بيئة التطوير وتثبيت التبعيات اللازمة. راجع[المقال](https://docs.aspose.cloud/cells/quickstart/) على موقع الويب Aspose للحصول على معرف العميل والسر الخاص بالعميل.

## كيفية تثبيت حزمة Go لـ Aspose.Cells Cloud

يمكنك تثبيت حزمة تطوير البرامج السحابية Aspose.Cells لنظام Go باستخدام الأمر `go get`. افتح الطرفية أو موجه الأوامر وشغّل الأمر التالي:

```bash
go install github.com/aspose-cells-cloud/aspose-cells-cloud-go@latest
```

سيؤدي هذا إلى تنزيل أحدث إصدار من SDK وتثبيته على مساحة عمل Go الخاصة بك.

## كيفية استيراد مكتبة Go إلى مشروعك

```golang
package main

import (
 . "github.com/aspose-cells-cloud/aspose-cells-cloud-go/v25"
)
```

## كيفية البدء باستخدام Aspose.Cells Cloud for Go، اتبع الخطوات التالية

- قم بإنشاء حساب على الرقم Aspose للسحابة واحصل على معرف عميل التطبيق والسر الخاص بك.
- أنشئ دليلًا لمشروعك وملفًا رئيسيًا.go داخله. أضف الكود التالي إلى ملف main.go.

### **رمز العينة**

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_AvailableSDKs.go" >}}

- قم بتشغيل المشروع go.mod، ثم قم بجلب التبعيات الخاصة بمشروعك، ثم قم بتشغيل التطبيق الذي قمت بإنشائه.

```bash
go mod init main
go mod tidy
go run main.go

```
