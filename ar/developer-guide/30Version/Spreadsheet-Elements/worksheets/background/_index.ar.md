---
title: "إضافة صورة خلفية أو حذفها في ورقة العمل – واجهة برمجة تطبيقات Aspose.Cells Cloud"
second_title: "وثيقة"
linktitle: "الخلفية"
type: docs
url: /worksheets/background/
keywords: "Aspose.Cells Cloud، خلفية ورقة العمل، واجهة برمجة تطبيقات إكسل، إضافة صورة خلفية، حذف خلفية ورقة العمل، أمثلة لوحدات التطوير البرمجي SDK"
description: "تعرّف على كيفية إضافة أو إزالة صورة خلفية في ورقة عمل إكسل باستخدام واجهة برمجة تطبيقات REST لـ Aspose.Cells Cloud. يشمل بناء جملة طلبات الإدخال وأمثلة لوحدات التطوير البرمجي SDK لغات جافا و.NET وبايثون وPHP، بالإضافة إلى معالجة الأخطاء."
weight: 20
ArticleTitle: "إضافة صورة خلفية أو حذفها في ورقة العمل باستخدام واجهة برمجة تطبيقات Aspose.Cells Cloud"
---

## العمل مع الخلفية في ورقة عمل إكسل

**نظرة عامة:** الخلفية عبارة عن صورة تظهر خلف خلايا ورقة العمل، وهي مفيدة في تعزيز العلامة التجارية أو تقديم إشارات بصرية. وتتيح لك واجهة برمجة تطبيقات Aspose.Cells Cloud إضافة أو حذف هذه الصورة الخلفية برمجيًا.

**المتطلبات المسبقة:**  
- رمز وصول صحيح لـ Aspose.Cells Cloud (OAuth 2.0).  
- ملف مصنف إكسل محفوظ في السحابة.  
- ملف صورة (PNG أو JPEG أو BMP) لاستخدامه كخلفية.

- **إضافة خلفية** – ضبط صورة خلفية لورقة عمل. راجع الدليل التفصيلي [كيفية ضبط الخلفية في ورقة عمل إكسل](/cells/worksheets/background/add/).  
- **حذف الخلفية** – إزالة صورة خلفية موجودة من ورقة عمل. راجع الدليل التفصيلي [كيفية حذف الخلفية في ورقة عمل إكسل](/cells/worksheets/background/delete/).

يمكن أن تُحسّن الخلفية في ورقة العمل من العلامة التجارية، أو تُبرز الأقسام المهمة، أو توفر إشارات بصرية للمستخدمين النهائيين. وتجعل واجهة برمجة تطبيقات Aspose.Cells Cloud من السهل ضبط أو مسح صورة الخلفية هذه مباشرةً من تطبيقك.

### مرجع واجهة برمجة التطبيقات

| العملية | طريقة HTTP | نقطة النهاية | معاملات المسار | جسم الطلب | استجابة ناجحة |
|----------|-------------|--------------|----------------|--------------|------------------|
| إضافة خلفية | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – اسم ملف المصنف<br>`sheetName` – اسم ورقة العمل الهدف | ملف الصورة (PNG أو JPEG أو BMP) بصيغة multipart/form‑data | `200 OK` – تم تطبيق الخلفية |
| حذف الخلفية | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – اسم ملف المصنف<br>`sheetName` – اسم ورقة العمل الهدف | *لا يوجد* | `200 OK` – تم إزالة الخلفية |

#### مثال (وحدة التطوير البرمجي SDK للغة جافا)

```java
// إضافة صورة خلفية
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// حذف صورة الخلفية
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### مثال (وحدة التطوير البرمجي SDK للغة بايثون)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# إضافة خلفية
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# حذف الخلفية
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

للحصول على أمثلة إضافية بلغات أخرى (C# وPHP وRuby)، راجع وثائق وحدات التطوير البرمجي SDK.

**مواضيع ذات صلة**  
- اعرف المزيد عن إدارة ورقات العمل بشكل عام: [نظرة عامة على ورقات العمل](/cells/worksheets/).  
- تعرّف على كيفية المصادقة مع Aspose.Cells Cloud: [دليل مصادقة واجهة برمجة التطبيقات](/cells/authentication/).  
- استكشف عناصر أخرى لجدول البيانات مثل المخططات والجداول والصيغ: [مؤشر عناصر جدول البيانات](/cells/elements/).
---