---
title: كيفية تشغيل دوكر كونتين
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: كيفية تشغيل حاوية Docker Aspose.Cells السحابية. Aspose.Cells تدعم السحابة Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 100
kwords: Excel، Office Cloud، REST API، جدول البيانات، PDF، CSV، Json، Markdwon، كيفية تشغيل حاوية Docker
---
 ال**عامل ميناء**تم تصميم هذه التقنية لأتمتة نشر التطبيقات باستخدام حاويات خفيفة الوزن. يمكن للمطورين استخدام**حاوية عامل الميناء** لاختتام تطبيق بجميع مكتباته وتبعياته ونشر كل شيء كحزمة واحدة.

 Aspose.Cells قام فريق Cloud بنشر حاوية Docker على[مركز عامل الميناء](https://hub.docker.com/r/aspose/cells-cloud) لتسهيل مستخدمي Docker. سترشدك الأقسام التالية إلى كيفية تشغيل أوامر Docker أو كتابة التكوين في ملف Yaml لأداة إنشاء Docker.

## تكوين الحاوية

### الكميات المطلوبة

|مسار التثبيت في الحاوية|وصف|
|:- |:- |
|ج:\الخطوط|مجلد يحتوي على الخطوط، والذي سيتم استخدامه لعرض المستندات|
|ج:\البيانات|مجلد تخزين الملفات|

### حدود

|اسم|وصف|
|:- |:- |
|مفتاح الترخيص العام|المفتاح العام للترخيص|
|مفتاح الترخيص الخاص|المفتاح الخاص للترخيص|


إذا تم حذف معلمات "الترخيص"، فسيعمل التطبيق في الوضع التجريبي.


### قم بتشغيل حاوية Docker باستخدام سطر الأوامر

يمكنك ببساطة تشغيل أمر الإرساء التالي بعد سحب الحاوية منه[مركز عامل الميناء](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### تكوينات أداة Docker-Compose

يمكنك كتابة التكوينات التالية في ملف yaml الخاص بك لأداة Docker-Compose:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
