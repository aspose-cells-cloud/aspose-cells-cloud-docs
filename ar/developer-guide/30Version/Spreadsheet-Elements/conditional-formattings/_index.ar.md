---
title: "العمل مع التنسيق الشرطي في Excel"
second_title: "مستند"
linktype: "التنسيق الشرطي"
type: docs
url: /ar/conditional-formattings/
aliases: [/ar/working-with-conditional-formatting/]
keywords: "Excel, التنسيق الشرطي, Aspose.Cells Cloud, API"
description: "توفر واجهة برمجة تطبيقات Aspose.Cells Cloud لـ Excel نقاط نهاية لاسترداد قواعد التنسيق الشرطي وإضافتها وتعديلها ومسحها، مما يمكّن من التحليل البصري الديناميكي لبيانات ورقة العمل."
weight: 100
ArticleTitle: "العمل مع التنسيق الشرطي في Excel – دليل واجهة برمجة التطبيقات"
---

التنسيق الشرطي في Excel يمكّنك من تلوين الخلايا بلون معيّن بناءً على قيمة الخلية.

استخدم التنسيق الشرطي لمساعدتك في استكشاف البيانات وتحليلها بصريًا، واكتشاف القضايا الحرجة، وتحديد الأنماط والاتجاهات.

يجعل التنسيق الشرطي من السهل تسليط الضوء على خلايا أو نطاقات خلايا مثيرة للاهتمام، والتلميح إلى القيم غير المعتادة، وتصور البيانات باستخدام أشرطة البيانات وم масحات الألوان ومجموعات الأيقونات التي تتوافق مع تباينات محددة في البيانات.

يغيّر التنسيق الشرطي مظهر الخلايا استنادًا إلى الشروط التي تحدّدها. إذا كانت الشروط صحيحة، يتم تنسيق نطاق الخلايا؛ وإذا كانت الشروط خاطئة، يبقى نطاق الخلايا دون تغيير. توجد العديد من الشروط المدمجة، ويمكنك أيضًا إنشاء شروطك الخاصة (بما في ذلك باستخدام صيغة تُقيّم إلى **TRUE** أو **FALSE**).

توفر واجهة برمجة تطبيقات Aspose.Cells Cloud مجموعة من نقاط النهاية لإدارة قواعد التنسيق الشرطي برمجيًا. العمليات المتاحة هي كالتالي:

- **استرداد التنسيقات الشرطية لورقة العمل** – يسترِدّ جميع قواعد التنسيق الشرطي المطبّقة على ورقة العمل.  
  - **الطريقة:** `GET`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **المعلمات:** `fileName` (سلسلة نصية، مطلوبة)، `sheetName` (سلسلة نصية، مطلوبة)، ومعلمات استعلام اختيارية مثل `folder` و`storageName`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings?folder=Docs&storageName=MyStorage" -H "Authorization: Bearer {access_token}"
    ```
- **استرداد التنسيق الشرطي** – يُعيد تنسيقًا شرطيًّا معيّنًا باستخدام مُعرّفه.  
  - **الطريقة:** `GET`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **المعلمات:** `index` (عدد صحيح، مطلوب) يحدّد موضع القاعدة.  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X GET "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```
- **إضافة منطقة خلية لشرط التنسيق** – تضيف نطاق خلايا سيتأثر بالتنسيق الشرطي المحدّد.  
  - **الطريقة:** `POST`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **جسم الطلب (JSON):** `{ "FirstRow": 1, "FirstColumn": 1, "RowCount": 5, "ColumnCount": 3 }`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"FirstRow":1,"FirstColumn":1,"RowCount":5,"ColumnCount":3}'
    ```
- **إضافة شرط لشرط التنسيق** – يُعرّف شرطًا جديدًا (مثل القيمة أو الصيغة) لقاعدة التنسيق الموجودة.  
  - **الطريقة:** `POST`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/condition`  
  - **جسم الطلب (JSON):** `{ "Type": "CellValue", "Operator": "GreaterThan", "Formula1": "100" }`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/condition" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d '{"Type":"CellValue","Operator":"GreaterThan","Formula1":"100"}'
    ```
- **إضافة شرط تنسيق** – يُنشئ قاعدة تنسيق شرطي كاملة، بما في ذلك النوع والنمط.  
  - **الطريقة:** `POST`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **جسم الطلب (JSON):**  
    ```json
    {
      "Priority": 0,
      "Type": "HighlightCells",
      "Style": { "ForegroundColor": "FFFF0000" },
      "Condition": { "Operator": "LessThan", "Formula1": "50" },
      "CellArea": { "FirstRow": 0, "FirstColumn": 0, "RowCount": 10, "ColumnCount": 5 }
    }
    ```  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X POST "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" \
         -H "Authorization: Bearer {access_token}" \
         -H "Content-Type: application/json" \
         -d @condition.json
    ```
- **مسح جميع قواعد التنسيق الشرطي** – يزيل كل قواعد التنسيق الشرطي من ورقة العمل المستهدفة.  
  - **الطريقة:** `DELETE`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings" -H "Authorization: Bearer {access_token}"
    ```
- **إزالة منطقة الخلايا من التنسيق الشرطي** – تحذف منطقة خلايا مُعرّفة مسبقًا من قاعدة تنسيق شرطي.  
  - **الطريقة:** `DELETE`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}/cellarea`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0/cellarea" -H "Authorization: Bearer {access_token}"
    ```
- **إزالة التنسيق الشرطي** – يحذف قاعدة تنسيق شرطي كاملة من ورقة العمل.  
  - **الطريقة:** `DELETE`  
  - **نقطة النهاية:** `/cells/{fileName}/worksheets/{sheetName}/conditionalFormattings/{index}`  
  - **مثال باستخدام cURL:**  
    ```bash
    curl -X DELETE "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet1/conditionalFormattings/0" -H "Authorization: Bearer {access_token}"
    ```

تُوضّح الأمثلة أعلاه الطريقة المطلوبة لطلب HTTP، ونمط عنوان URL، والمعلمات الأساسية، وحمولات الطلبات النموذجية لكل عملية. إذا رغبت، يمكنك استخدام SDK المناسب (C# أو Java أو Python وما إلى ذلك) للحصول على مقاطع كود مُخصّصة للغات برمجة معيّنة.