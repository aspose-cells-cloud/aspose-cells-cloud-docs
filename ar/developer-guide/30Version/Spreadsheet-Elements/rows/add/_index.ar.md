---
---
title: "كيفية إضافة صفوف إلى ورقة عمل في إكسل"
second_title: "مستند"
linktitle: "إضافة"
type: docs
url: /ar/rows/add/
keywords: "Aspose.Cells, إضافة صفوف, واجهة برمجة تطبيقات إكسل, REST, C#, Java, Python, Node.js"
description: "دليل خطوة بخطوة لإضافة صف واحد أو عدة صفوف إلى ورقة عمل في إكسل باستخدام واجهة Aspose.Cells Cloud REST API، مع أمثلة كود مكتوبة بلغات C# و Java و Python و Node.js."
weight: 20
ArticleTitle: "إضافة صفوف إلى ورقة عمل في إكسل باستخدام واجهة Aspose.Cells Cloud API – دليل خطوة بخطوة"
---

## كيفية إضافة صفوف إلى ورقة عمل في إكسل

يشرح هذا المقال كيفية إدراج صف فارغ واحد أو عدة صفوف في ورقة عمل موجودة باستخدام واجهة Aspose.Cells Cloud REST API. تأكد من امتلاك مفتاح API صالح وتنصيب وتهيئة مكتبة SDK المناسبة قبل البدء.

**المتطلبات الأساسية**  
- [ ] حساب Aspose.Cells Cloud مع اشتراك نشط.  
- [ ] مفتاح API / رمز وصول تم إنشاؤه من لوحة تحكم Aspose Cloud.  
- [ ] إحدى مكتبات SDK المدعومة (C# أو Java أو Python أو Node.js) مثبَّتة ومُعدَّة.  

**مرجع واجهة برمجة التطبيقات**  
- **طريقة HTTP:** `POST`  
- **النهاية (Endpoint):** `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/rows`  
- **المعلمات المسار المطلوبة:**  
  - `fileName` – اسم ملف إكسل المخزن في السحابة.  
  - `sheetName` – اسم ورقة العمل التي سيتم إضافة الصفوف إليها.  
- **المعلمات الاستعلامية (Query Parameters):**  
  - `startrow` – الفهرس الصفري للصف الذي يبدأ منه الإدراج.  
  - `totalRows` – عدد الصفوف المراد إضافتها.  
  - `folder` – (اختياري) مسار المجلد السحابي للملف.  
  - `storage` – (اختياري) اسم وحدة التخزين إذا كنت تستخدم وحدة تخزين غير افتراضية.  
- **جسم الطلب (مثال بصيغة JSON):**  

  ```json
  {
    "startrow": 5,
    "totalRows": 3
  }
  ```

  **مثال باستخدام cURL**

  ```bash
  curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/rows?startrow=5&totalRows=3&folder=MyFolder&storage=MyStorage" \
      -H "Authorization: Bearer {access_token}" \
      -H "Content-Type: application/json" \
      -d '{"startrow":5,"totalRows":3}'
  ```

- **استجابة ناجحة (HTTP 200):** تُعيد معلومات ورقة العمل المُحدَّثة، بما في ذلك عدد الصفوف الجديد.  

  ```json
  {
    "Code": 200,
    "Status": "OK",
    "Worksheet": {
      "Name": "Sheet1",
      "RowsCount": 30
    }
  }
  ```

- **مثال على استجابة خطأ (HTTP 400):**  

  ```json
  {
    "Code": 400,
    "Status": "Bad Request",
    "Message": "معلمة startrow غير صالحة. يجب أن تكون عددًا صحيحًا غير سالب."
  }
  ```

- **رموز الحالة (Status Codes):**  

  | الرمز | المعنى                                |
  |------|----------------------------------------|
  | 200  | تمت إضافة الصفوف بنجاح                 |
  | 400  | معلمات غير صالحة أو JSON معطّل         |
  | 401  | فشلت عملية المصادقة                    |
  | 404  | الملف أو ورقة العمل غير موجودة         |
  | 500  | خطأ في الخادم                           |

فيما يلي روابط سريعة لعرض الأمثلة التفصيلية لإضافة الصفوف:

- [كيفية إضافة صف فارغ إلى ورقة عمل في إكسل](/ar/cells/rows/add/row/)
- [كيفية إضافة عدة صفوف إلى ورقة عمل في إكسل](/ar/cells/rows/add/rows/)
---