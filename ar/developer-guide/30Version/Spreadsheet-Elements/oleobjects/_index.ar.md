---
title: "العمل مع كائنات OLE في Excel"
second_title: "مستند"
linktitle: "OleObjects"
type: docs
url: /ar/oleobjects/
aliases: [/ar/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, سحابة"
description: "استخدم واجهة Aspose.Cells Cloud REST API لاسترجاع كائنات OLE وإضافتها وتحديثها وحذفها وتحويلها في أوراق عمل Excel. تتوفر حزم تطوير برمجيات (SDKs) للغات Java و .NET و Python و PHP و Ruby و Go و Node.js و Perl و Swift و Android."
weight: 100
ArticleTitle: "العمل مع كائنات OLE في Excel – دليل لاسترجاع وإضافة وتحديث وحذف وتحويل كائنات OLE"
---

**كيفية العمل مع كائنات OLE في ورقة عمل Excel**

توفر واجهة Aspose.Cells Cloud REST API مجموعة كاملة من العمليات لإدارة كائنات OLE برمجيًا. فيما يلي مرجع موجز لكل عملية، بما في ذلك طريقة HTTP ونمط نقطة النهاية والمعاملات المطلوبة ومثال مبسّط على الاستجابة.

- [كيفية استرجاع كائن OLE من ورقة عمل Excel](/ar/cells/oleobjects/get/)
  - **الطريقة:** `GET`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **المعاملات:** `fileName` (نص)، `sheetName` (نص)، `oleObjectIndex` (عدد صحيح)  
  - **مثال على الاستجابة:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [كيفية إضافة كائن OLE إلى ورقة عمل Excel](/ar/cells/oleobjects/add/)
  - **الطريقة:** `POST`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **المعاملات:** `fileName`، `sheetName`، `oleObject` (ثنائي أو مشفر بـ base‑64)، `imageFormat` (اختياري)  
  - **مثال على جسم الطلب:** multipart/form‑data مع تيار الملف.  
  - **مثال على الاستجابة:** `201 Created` مع رأس موقع للكائن OLE الجديد.

- [كيفية تحديث كائن OLE معيّن في ورقة عمل Excel](/ar/cells/oleobjects/update/)
  - **الطريقة:** `PUT`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **المعاملات:** `fileName`، `sheetName`، `oleObjectIndex`، `oleObject` (المحتوى المُحدَّث)  
  - **مثال على الاستجابة:** `200 OK` مع بيانات تعريف الكائن المحدَّثة.

- [كيفية تحويل كائن OLE إلى صورة في ورقة عمل Excel](/ar/cells/oleobjects/convert/)
  - **الطريقة:** `GET`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **المعاملات:** `fileName`، `sheetName`، `oleObjectIndex`، `format` (مثل `png` أو `jpeg`)  
  - **مثال على الاستجابة:** تيار صورة ثنائي للكائن OLE بعد التحويل.

- [كيفية حذف جميع كائنات OLE في ورقة عمل Excel](/ar/cells/oleobjects/clear/)
  - **الطريقة:** `DELETE`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **المعاملات:** `fileName`، `sheetName`  
  - **مثال على الاستجابة:** `204 No Content` يشير إلى إزالة جميع كائنات OLE.

- [كيفية حذف كائن OLE معيّن في ورقة عمل Excel](/ar/cells/oleobjects/delete/)
  - **الطريقة:** `DELETE`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **المعاملات:** `fileName`، `sheetName`، `oleObjectIndex`  
  - **مثال على الاستجابة:** `204 No Content` يؤكد حذف الكائن.