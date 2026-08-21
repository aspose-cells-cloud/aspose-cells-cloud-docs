---
title: "كيفية ضبط موقع التخزين لحاوية Aspose.Cells Cloud Docker"
second_title: "وثيقة"
ArticleTitle: "إعدادات تخزين حاوية Aspose.Cells Cloud Docker"
linktitle: "تخزين الحاوية"
type: docs
url: /docker/storage/
description: "اضبط موقع التخزين لحاويات Aspose.Cells Cloud Docker باستخدام ملفات تكوين JSON أو PowerShell أو Bash."
weight: 30
keywords: "Aspose.Cells, Docker, تخزين الحاوية, تكوين JSON, PowerShell, Bash"
---

**ملخص**: توضح هذه الدليل كيفية ضبط موقع التخزين لحاويات Aspose.Cells Cloud Docker على نظامي التشغيل Windows وLinux باستخدام ملفات تكوين JSON وأوامر Docker run.

## إعداد التخزين الافتراضي ##

**متطلبات مسبقة**: تأكد من تثبيت محرك Docker الإصدار 20.10 أو أحدث، وامتلاك مفاتيح ترخيص Aspose.Cells Cloud الصالحة (`LicensePublicKey` و`LicensePrivateKey`)، ووجود مجلد المضيف الذي تنوِّي استخدامه للتخزين (مثل `c:/data` على Windows أو `/data` على Linux) مُعدًّا مسبقًا مع الأذونات المناسبة.

{{< tabs tabTotal="2" tabID="1" tabName1="windows" tabName2="linux" >}}

{{< tab tabNum="1" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "c:/data"
    }
  ]
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Local": [
    {
      "Name": "First Storage",
      "RootFolder": "/data"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## الموقع الافتراضي ##

- **Windows**

```powershell
c:\app\storageResource.json
```

- **Linux**

```bash
/app/storageResource.json
```

## إعداد التخزين المخصّص ##

حدّد ملف تعريف تخزين مخصّص عندما تحتاج إلى استخدام مجلد مختلف لبيانات Aspose.Cells Cloud.

```bash
docker run -d \
  -v c:/data:c:/data \   # ربط مجلد المضيف كمساحة تخزين للحاوية
  -p 47900:5000 \        # تعيين منفذ واجهة برمجة التطبيقات
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=c:/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

*مثال لنظام Linux*:

```bash
docker run -d \
  -v /data:/data \   # ربط مجلد المضيف كمساحة تخزين للحاوية
  -p 47900:5000 \    # تعيين منفذ واجهة برمجة التطبيقات
  -e LicensePublicKey=yourLicensePublicKey \
  -e LicensePrivateKey=yourLicensePrivateKey \
  -e storagesCredentialsFilePath=/data/storageResource.json \
  --name asposecellscloud \
  aspose/cells-cloud:ltsc2019.22.9.0
```

**وثيقة المرجع**:

- [كيفية تشغيل حاوية Aspose.Cells Cloud Docker.](https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/)
- [ميزات حاوية Docker](https://docs.aspose.cloud/cells/docker/container-features/)
- [تنزيل صورة Aspose.Cells Cloud Docker](https://docs.aspose.cloud/cells/docker/download-image/)
- [إدارة علامات الحاوية](https://docs.aspose.cloud/cells/docker/manage-tags/)
---