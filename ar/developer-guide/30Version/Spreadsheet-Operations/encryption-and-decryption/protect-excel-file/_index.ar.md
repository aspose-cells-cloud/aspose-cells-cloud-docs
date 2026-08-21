---
title: "حماية ملف Excel باستخدام واجهة Aspose.Cells Cloud API"
second_title: "مستند"
linktitle: "حماية ملف Excel"
type: docs
url: /protect-excel-file/
aliases: [/protect-excel-workbooks/, /workbook/protect/]
keywords: "Aspose.Cells, حماية Excel, واجهة برمجة التطبيقات, REST, SDK"
description: "تعرّف على كيفية حماية ملف Excel عبر واجهة Aspose.Cells Cloud REST API. يتضمّن خطوات المصادقة، ومعلّمات الاستعلام ومحتوى الطلب، وطلب cURL، وأكواد أمثلة لـ SDK بلغات C# وJava وPHP وRuby وNode.js وPython وPerl وGo."
weight: 30
ArticleTitle: "حماية ملف Excel باستخدام واجهة Aspose.Cells Cloud API"
---

تقوم هذه **واجهة برمجة التطبيقات REST** بـ**حماية** ملف Excel، مما يتيح لك حماية ملف Excel بشكل آمن باستخدام كلمة مرور وخيارات الحماية عبر Aspose.Cells Cloud.

## واجهة PostProtectDocument API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/protection
```

### **الأمان والمصادقة**

تُعدّ واجهات Aspose.Cells Cloud API آمنة وتتطلب <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">مصادقة تعتمد على رمز JWT</a>.

### معلّمات الاستعلام

| اسم المعلّمة | النوع | الوصف |
|--------------|-------|--------|
| folder | string | المجلد الذي يحتوي على الملف المطلوب حمايته. _(اختياري)_ |
| storageName | string | اسم موقع التخزين. _(اختياري؛ الافتراضي = "Default")_ |

### معلّمات جسم الطلب

| اسم المعلّمة | النوع | الوصف |
|--------------|-------|--------|
| protection | WorkbookProtectionRequest | كائن يُعرّف إعدادات الحماية لملف العمل. |

#### WorkbookProtectionRequest

| اسم المعلّمة | النوع | الوصف |
|--------------|-------|--------|
| ProtectionType | string | نوع الحماية المطلوب تطبيقه. القيم المسموحة (بدون تمييز بين الأحرف الكبيرة والصغيرة): **ALL**، **CONTENTS**، **NONE**، **OBJECTS**، **SCENARIOS**، **STRUCTURE**، **WINDOWS**. |
| Password | string | كلمة مرور اختيارية لضبطها للحماية. |

### الاستجابة

```json
{
  "Status":"OK",
  "Code":200
}
```

**كود حالات HTTP**

| الكود | المعنى | الوصف |
|------|--------|--------|
| 200 | OK (تمت العملية بنجاح) | تمت عملية تطبيق الحماية بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400 | Bad Request (طلب خاطئ) | معلّمات مفقودة أو غير صالحة (مثل نوع ملف غير مدعوم). |
| 401 | Unauthorized (غير مصادق عليه) | رمز JWT غير صالح أو مفقود. |
| 413 | Payload Too Large (حمولة كبيرة جدًا) | حجم الملف المرفوع يتجاوز الحد المسموح به. |
| 500 | Internal Server Error (خطأ داخلي في الخادم) | خطأ غير متوقع في الخادم. |

## كيفية استخدام واجهة PostProtectDocument API باستخدام SDKs

### المتطلبات المسبقة

قبل استدعاء واجهة برمجة التطبيقات، تأكّد من تنفيذ الخطوات التالية:

- **الحصول على رمز وصول JWT** باستخدام سير المصادقة الموضّح في قسم الأمان.  
- **رفع ملف العمل** إلى مساحة التخزين الخاصة بك في Aspose Cloud أو التأكّد من وجوده بالفعل في المجلد المستهدف.  
- **معرفة اسم مساحة التخزين** (الافتراضي هو `"Default"` إن لم يُحدّد) واسم الملف الدقيق الذي ترغب في حمايته.

### مواصفات واجهة PostProtectDocument API

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument" target="_blank" rel="noopener noreferrer">مواصفات OpenAPI</a> تُعرّف واجهة برمجة تطبيقات متاحة للعامة وتتيح لك إجراء تفاعلات REST مباشرة من متصفح الويب.

### مثال: حماية ملف Excel باستخدام cURL

1. احصل على رمز وصول كما هو موضّح في **المتطلبات المسبقة / المصادقة**.  
2. نفّذ الطلب:

   ```bash
   curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection?folder=MyFolder&storageName=MyStorage" \
        -H "accept: application/json" \
        -H "Content-Type: application/json" \
        -H "Authorization: Bearer <access_token>" \
        -d '{ "ProtectionType": "ALL", "Password": "aspose" }'
   ```

   ستتضمن الاستجابة كائن حالة يؤكد نجاح الحماية.

### استخدام Aspose.Cells Cloud SDKs

استخدام SDK هو أسرع طريقة لتطوير تطبيقات تتفاعل مع Aspose.Cells Cloud. فالمكتبة SDK تقوم بإخفاء التفاصيل منخفضة المستوى، مما يتيح لك التركيز على منطق تطبيقك. راجع <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">مستودع GitHub</a> للحصول على قائمة كاملة بـ SDKs الخاصة بـ Aspose.Cells Cloud.

تُظهر أمثلة الكود التالية كيفية استدعاء خدمات Aspose.Cells عبر لغات برمجة مختلفة باستخدام SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostProtectWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostProtectWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostProtectWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostProtectWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostProtectWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostProtectWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostProtectWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostProtectWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

### استجابة كاملة نموذجية

```json
{
  "Status": "OK",
  "Code": 200,
  "Workbook": {
    "Name": "test.xlsx",
    "Path": "/MyFolder/test.xlsx",
    "Protection": {
      "ProtectionType": "ALL",
      "Password": true
    }
  }
}
```