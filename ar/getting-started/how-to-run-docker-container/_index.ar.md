---
title: "تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud – سحب، تهيئة وتشغيل"
second_title: "مستند"
ArticleTitle: "كيفية تشغيل حاوية Docker الخاصة بـ Aspose.Cells Cloud"
LinkTitle: "حاوية Docker"
type: docs
url: /getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: "تعرّف على كيفية سحب حاوية Docker الخاصة بـ Aspose.Cells Cloud وتهيئتها وتشغيلها على نظامي التشغيل Windows أو Linux. يتضمن ملف YAML لـ Docker‑Compose، وإعداد الترخيص، وترقية المنافذ (Port mapping)، ونصائح لاستكشاف الأخطاء وإصلاحها."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "حاوية Docker"
  - "Docker Compose"
  - "مفاتيح الترخيص"
  - "Excel"
  - "جدول بيانات"
  - "واجهة برمجة تطبيقات سحابية"
  - "Docker"
  - "Aspose Cells"
  - "واجهة برمجة تطبيقات"
---

تُصمم تقنية Docker لأتمتة نشر التطبيقات باستخدام حاويات خفيفة الوزن. ويمكن للمطورين استخدام حاوية Docker لحزم التطبيق مع جميع مكتباته واعتمادياته ونشرها كحزمة واحدة.

نشر فريق Aspose.Cells Cloud حاوية Docker على <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> لتسهيل استخدامها من قِبل مستخدمي Docker.

**المتطلبات الأساسية** – تأكد من تثبيت محرك Docker بإصدار ≥ 20.x، وأن نظام التشغيل الخاص بك (Windows 10 أو Windows Server 2019/2022 أو إحدى توزيعات Linux المدعومة) يستوفي المتطلبات. ويمكنك تزويد مفتاح ترخيص اختياري لتشغيل التطبيق في الوضع المرخص.

- محرك Docker بإصدار ≥ 20.x مثبت  
- نظام التشغيل المدعوم (Windows 10 أو Windows Server 2019/2022 أو إحدى توزيعات Linux)  
- مفتاح ترخيص اختياري للتشغيل في الوضع المرخص  

## تهيئة الحاوية

### وحدات التخزين المطلوبة

| مسار التحميل في الحاوية | الوصف |
| :--- | :--- |
| C:\fonts | مجلد يحتوي على الخطوط المستخدمة في عرض المستندات |
| C:\data | مجلد لتخزين الملفات |

**البديل لنظامي التشغيل Linux/macOS**: استخدم المسارين `/fonts` و `/data` داخل الحاوية، وقم بربطهما بمجلدين على الجهاز المضيف مثل `/home/user/fonts` و `/home/user/data` عند تشغيل الحاوية.

### المعاملات

| الاسم | الوصف |
| :--- | :--- |
| LicensePublicKey | المفتاح العام للترخيص |
| LicensePrivateKey | المفتاح الخاص للترخيص |

إذا تم حذف معاملات **License**، يعمل التطبيق في الوضع التجريبي.

### 1. سحب صورة Aspose.Cells Cloud

```bash
# سحب إصدار مُحدد من صورة Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# سحب صورة Aspose.Cells Cloud لنظام Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# سحب صورة Aspose.Cells Cloud لنظام Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# سحب صورة Aspose.Cells Cloud لنظام Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **ملاحظة:** للحصول دائمًا على أحدث إصدار، يمكنك أيضًا سحب العلامة `latest`: `docker pull aspose/cells-cloud:latest`.

### 2. التهيئة باستخدام أداة Docker‑Compose

يمكنك كتابة التهيئة التالية في ملف **docker‑compose.yml**:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # منفذ المضيف 5000 ← منفذ الحاوية 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "yourPublicKey"
    LicensePrivateKey: "yourPrivateKey"
```

> **ملاحظة:** يُشير تعيين المنافذ `5000:80` إلى أن واجهة برمجة التطبيقات ستكون متاحة عبر الرابط `http://localhost:5000`.

### 3. تشغيل حاوية Docker باستخدام سطر الأوامر

```bash
docker run \
  -e "LicensePublicKey=yourPublicKey" \
  -e "LicensePrivateKey=yourPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**استكشاف الأخطاء وإصلاحها:**  
- **تعارض في المنافذ:** تأكد من أن منفذ 5000 على الجهاز المضيف غير مستخدم، أو غيّر التعيين إلى منفذ غير مستخدم.  
- **فشل تحميل الترخيص:** تحقق من أن المفتاح العام والمفتاح الخاص تم تمريرهما بشكل صحيح كمتغيرات بيئة أو تم تحميلهما كملفات.  
- **الخطوط مفقودة:** إذا ظهرت المستندات بخطوط غير صحيحة، تأكد من أن مجلد الخطوط مربوط بشكل صحيح ويحتوي على ملفات الخطوط المطلوبة.

**موارد ذات صلة:**  
- <a href="/cells/api/">مرجع واجهة برمجة التطبيقات</a> | <a href="/cells/license/">دليل تفعيل الترخيص</a> | <a href="/cells/getting-started/">نظرة عامة على البدء</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Run Aspose.Cells Cloud Docker Container",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "سحب صورة Docker",
      "text": "شغّل الأمر `docker pull aspose/cells-cloud:<version>` لتنزيل الصورة المطلوبة."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "إنشاء ملف docker‑compose",
      "text": "حدّد الصورة والمنافذ ووحدات التخزين ومتغيرات بيئة الترخيص في ملف `docker‑compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "تشغيل الحاوية",
      "text": "نفّذ الأمر `docker run` مع متغيرات البيئة ووحدات التخزين وتعيين المنافذ المناسبة."
    }
  ]
}
```