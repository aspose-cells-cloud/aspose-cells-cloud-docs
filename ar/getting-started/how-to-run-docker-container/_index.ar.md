---
title: "كيفية تشغيل حاوية Aspose.Cells Cloud Docker: قم بتشغيل حاوية Aspose.Cells Cloud الرسمية في 3 خطوات: السحب والتكوين والبدء"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /ar/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: كيفية تشغيل حاوية Docker Aspose.Cells السحابية. تدعم Aspose.Cells السحابية Excel إنشاء الكائنات الداخلية وتحويلها ودمجها وتقسيمها وحمايتها وتشغيلها وما إلى ذلك.
weight: 100
kwords: Excel، Office السحابة، REST API، جدول بيانات، PDF، CSV، Json، Markdown، كيفية تشغيل حاوية Docker
---
 ال**عامل ميناء** صُممت هذه التقنية لأتمتة نشر التطبيقات باستخدام حاويات خفيفة الوزن. يمكن للمطورين استخدام**حاوية Docker** لتغليف التطبيق بكل مكتباته وتبعياته ونشر كل شيء كحزمة واحدة.

 Aspose.Cells نشر فريق Cloud حاوية Docker على[مركز دوكر](https://hub.docker.com/r/aspose/cells-cloud) لتسهيل الأمر على مستخدمي Docker. سترشدك الأقسام التالية إلى كيفية تشغيل أوامر Docker أو كتابة الإعدادات في ملف Yaml لأداة Docker Compose.

## تكوين الحاوية

### الأحجام المطلوبة

|مسار التركيب في الحاوية|وصف|
|:- |:- |
|ج:\الخطوط|مجلد يحتوي على الخطوط التي سيتم استخدامها لعرض المستندات|
|ج:\البيانات|مجلد تخزين الملفات|

### حدود

|اسم|وصف|
|:- |:- |
|ترخيص المفتاح العام|المفتاح العام للترخيص|
|مفتاح الترخيص الخاص|المفتاح الخاص للترخيص|

إذا تم حذف معلمات "الترخيص"، فسيعمل التطبيق في الوضع التجريبي.

### 1. اسحب صورة السحابة Aspose.Cells

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. تكوينات أداة Docker-Compose

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

### 3. قم بتشغيل حاوية Docker باستخدام سطر الأوامر

 يمكنك ببساطة تشغيل أمر docker التالي بعد سحب الحاوية من[مركز دوكر](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
