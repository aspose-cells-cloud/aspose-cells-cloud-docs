---
title: "تنزيل صورة Aspose.Cells Cloud Docker"
second_title: "الوثيقة"
ArticleTitle: "تنزيل صورة Aspose.Cells Cloud Docker"
linktitle: "تنزيل الصورة"
type: docs
url: /ar/docker/downloads/
description: "احصل على أحدث صور Aspose.Cells Cloud Docker لخوادم Windows Server 2016/2019 وLinux. اتبع الإرشادات خطوة بخطوة، والمتطلبات الأساسية، ونصائح الأمان لتشغيل الحاوية محليًا."
weight: 30
keywords: "Aspose.Cells, Cloud, Docker, حاوية, صورة, تنزيل, Windows Server, Linux, REST API"
---  

## نظرة عامة  

`aspose/cells-cloud` – الصورة الرسمية لـ Docker التي تستضيف **واجهة برمجة تطبيقات Aspose.Cells Cloud** REST API. تتيح لك هذه الصورة تشغيل محرك معالجة جداول البيانات الكامل داخل حاوية، مما يمكّن من عمليات النشر دون اتصال بالإنترنت أو في بيئة سحابية خاصة دون الاعتماد على خدمات Aspose السحابية العامة.  

**آخر تحديث:** 2026-06-30  

**قائمة التحقق السريع للبدء**

- تأكد من أن إصدار محرك Docker هو 20.10 أو أحدث.  
- اسحب الصورة المناسبة لنظام التشغيل الخاص بك (انظر الأقسام أدناه).  
- عيّن متغيري البيئة `ASPOSE_CLIENT_ID` و`ASPOSE_CLIENT_SECRET`.  
- شغّل الحاوية مع تعيين منفذ 8080 ليربط بالمنفذ الداخلي 80.  

---  

## المتطلبات الأساسية  

| المتطلب | التفاصيل |
|---------|---------|
| **محرك Docker** | Docker 20.10 أو أحدث مثبت على نظام التشغيل المضيف. |
| **نظام التشغيل** | Windows Server 2016 أو Windows Server 2019 أو أي توزيعة حديثة من Linux. |
| **الوصول إلى Docker Hub** | حساب نشط على Docker Hub (اختياري لكن يُوصى به للصور الخاصة). شغّل الأمر `docker login` إذا احتجت لسحب الصور من مستودع خاص. |
| **بيانات اعتماد Aspose Cloud** | `ASPOSE_CLIENT_ID` و`ASPOSE_CLIENT_SECRET` – احصل عليهما من لوحة تحكم Aspose Cloud. |

> **نصيحة:** تحقق من تثبيت Docker باستخدام الأمر `docker --version`.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## تشغيل الحاوية  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **متغيرات البيئة** – `ASPOSE_CLIENT_ID` و`ASPOSE_CLIENT_SECRET` توفران بيانات الاعتماد المطلوبة من قبل واجهة برمجة التطبيقات.  
* **تعيين المنافذ (Port Mapping)** – تُعرِّف الحاوية المنفذ 80؛ قم بربطه بمنفذ على المضيف (مثل 8080) للوصول إلى الخدمة.  
* **الوضع المنفصل (`-d`)** – يشغّل الحاوية في الخلفية.  

---  

## الإصدارات والتحديثات  

| نظام التشغيل | العلامة (Tag) | تاريخ الإصدار | كيفية الحصول على أحدث إصدار |
|-------------|---------------|--------------|----------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:linux.latest` |

> **ملاحظة:** العلامة `21.9` هي الإصدار المستقر الحالي. استخدم العلامة `latest` أو راجع [ملاحظات إصدار Aspose.Cells Cloud](/cells/release-notes/) للحصول على إصدارات أحدث.  

---  

## التحقق والأمان  

* **التحقق من بصمة الصورة (Image Digest)**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **فحص الثغرات (يُوصى به)**  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **أفضل الممارسات** – حدّث Docker باستمرار، وشغّل الحاويات بأقل صلاحيات مطلوبة، وافحص الصور بانتظام عن الثغرات المعروفة (CVEs).  

* **مثال لبيانات منظمة (JSON-LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Image",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## المشاكل الشائعة وحلها  

| العرض | السبب المحتمل | الحل |
|--------|---------------|------|
| `docker: command not found` | لم يتم تثبيت Docker أو لم تُضبط متغيرات PATH | ثبّت Docker وأعد تشغيل الطرفية. |
| فشل المصادقة عند السحب | نقص بيانات `docker login` أو خطأ فيها | شغّل الأمر `docker login` باستخدام بيانات اعتماد Docker Hub صحيحة. |
| خروج الحاوية فورًا | نقص متغيرات البيئة المطلوبة | قدم `ASPOSE_CLIENT_ID` و`ASPOSE_CLIENT_SECRET` كما هو موضح في قسم **تشغيل الحاوية**. |
| تعارض في منفذ المضيف | المنفذ على المضيف مستخدم مسبقًا | اختر منفذ مضيف مختلف (مثل `-p 8081:80`). |

---  

## انظر أيضًا  

* [مستندات واجهة برمجة تطبيقات Aspose.Cells Cloud](/cells/cloud/api/)  
* [ملاحظات إصدار Aspose.Cells Cloud](/cells/release-notes/) – سجل تغييرات مفصّل لإصدار 21.9 والإصدارات الأحدث.  
* [ميزات حاوية Aspose.Cells Docker](/cells/docker/features/)  
* [علامات صورة Aspose.Cells Docker](/cells/docker/tag-list/)  

---  

*أعدّه فريق هندسة Aspose Cloud.*