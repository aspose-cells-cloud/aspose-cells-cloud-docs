---
title: كيفية تشغيل Docker Containe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: كيفية تشغيل حاوية Docker Aspose.Cells Cloud. Aspose.Cells Cloud يدعم Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 100
---
 ال**عامل ميناء** تم تصميم التكنولوجيا لأتمتة نشر التطبيقات باستخدام حاويات خفيفة الوزن. يمكن للمطورين استخدام ملف**حاوية عامل الميناء** لإنهاء تطبيق بكل مكتباته وتبعياته ونشر كل شيء كحزمة واحدة.

 نشر فريق السحابة Aspose.Cells حاوية Docker على[Docker Hub](https://hub.docker.com/r/aspose/cells-cloud) لتسهيل مستخدمي Docker. ستوجهك الأقسام التالية إلى كيفية تشغيل أوامر Docker أو كتابة التكوين في ملف Yaml لأداة إنشاء Docker.

## تكوين الحاوية

### الأحجام المطلوبة

|مسار التركيب في الحاوية|وصف|
|:- |:- |
|ج: \ الخطوط|مجلد مع الخطوط ، والذي سيتم استخدامه لتقديم المستندات|
|ج: \ البيانات|مجلد تخزين الملفات|

### حدود

|اسم|وصف|
|:- |:- |
|LicensePublicKey|المفتاح العام للترخيص|
|مفتاح الترخيص الخاص|المفتاح الخاص للترخيص|


إذا تم حذف معلمات "الترخيص" ، فسيعمل التطبيق في الوضع التجريبي.


### قم بتشغيل حاوية Docker باستخدام سطر الأوامر

 يمكنك ببساطة تشغيل أمر docker التالي بعد سحب الحاوية من[Docker Hub](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

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
