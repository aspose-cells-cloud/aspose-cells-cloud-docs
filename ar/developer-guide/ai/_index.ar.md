---
---
title: "Aspose.Cells Cloud AI – تحليل المهام، ترجمة الجداول وملفات النصوص"
second title: "الوثيقة"
ArticleTitle: "طور مهاراتك في الذكاء الاصطناعي: تعلّم ترجمة إكسل، تجزئة المهام، وأكثر من ذلك"
linktitle: "الذكاء الاصطناعي"
type: docs
url: /ai/
keywords: "Aspose.Cells، Cloud AI، ترجمة إكسل، تحليل المهام، REST API"
description: "استكشف Aspose.Cells Cloud AI لتحليل المهام، وترجمة كتب عمل إكسل وملفات النصوص. تتضمن نقاط نهاية REST، وأكواد مثال، وأفضل الممارسات."
weight: 20
---

يوفر Aspose.Cells Cloud AI ثلاث خدمات قوية مدعومة بالذكاء الاصطناعي لتبسيط العمل مع بيانات إكسل وملفات النصوص: **تحليل المهمة المستخدم**، **ترجمة الجدول المُحسَّن**، و**ترجمة ملف النص**. تتيح هذه واجهات برمجة التطبيقات للمطورين تحليل أهداف المستخدمين المعقدة إلى خطوات قابلة للتنفيذ برمجيًا، وترجمة كتب العمل بأكملها أو ملفات النصوص العادية، ودمج النتائج في تطبيقاتهم المخصصة. ابدأ باستخدام النقاط النهائية أدناه بسرعة، وراجع المواصفات التفصيلية لطلبات واستجابات كل خدمة المقدمة في الوثائق.

- **[تحليل المهمة المستخدم](https://docs.aspose.cloud/cells/decompose-user-task/)** – حوّل أهداف المستخدمين إلى خطط عمل متتالية باستخدام Aspose.Cells Cloud AI.  
  - **طريقة الطلب:** `POST`  
  - **عنوان URL للنقطة النهائية:** `https://api.aspose.cloud/v4.0/cells/ai/decompose-task`  
  - **الرؤوس:** `Authorization: Bearer <access_token>`, `Content-Type: application/json`  
  - **جسم الطلب (JSON):**  
    ```json
    {
      "task": "توليد تقرير مبيعات ربع سنوي مع رسوم بيانية وجداول محورية"
    }
    ```  
  - **الاستجابة:** تُعيد ملف الجدول المحتوي على قائمة المهام كملف قابل للتنزيل.  
  - **رموز الحالة:** `200 OK`، `400 Bad Request`، `401 Unauthorized`، `500 Internal Server Error`  
  - **المتطلبات المسبقة:** رمز وصول صالح مع نطاق **CellsAI**.  
  - **مثال على استجابة (مقتطف JSON):**  
    ```json
    {
      "fileId": "12345abcde",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/12345abcde"
    }
    ```  
  - **ملاحظات:** يتضمن كتاب العمل الذي تم إنشاؤه ورقة عمل باسم **TaskList** تحتوي على خطوات مرتبة. حد الاستخدام: 100 طلب في الدقيقة.

- **[ترجمة الجدول المُحسَّن](https://docs.aspose.cloud/cells/translate-spreadsheet/)** – ترجمة جدول كامل باستخدام Aspose.Cells Cloud AI.  
  - **طريقة الطلب:** `POST`  
  - **عنوان URL للنقطة النهائية:** `https://api.aspose.cloud/v4.0/cells/ai/translate-spreadsheet`  
  - **الرؤوس:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **معلمات الطلب:**  
    - `file` – ملف إكسل المراد ترجمته (ثنائي).  
    - `targetLanguage` – رمز اللغة حسب المعيار الدولي (مثل `fr`, `de`).  
  - **الاستجابة:** تُعيد كتاب العمل المُترجَم كملف قابل للتنزيل.  
  - **رموز الحالة:** `200 OK`، `400 Bad Request`، `401 Unauthorized`، `415 Unsupported Media Type`، `500 Internal Server Error`  
  - **المتطلبات المسبقة:** رمز وصول مع نطاق **CellsAI** ومساحة تخزين كافية.  
  - **مثال على استجابة (مقتطف JSON):**  
    ```json
    {
      "translatedFileId": "f9d8c7b6",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/f9d8c7b6"
    }
    ```  
  - **ملاحظات:** تُترجم جميع قيم الخلايا والتعليقات وأسماء الأوراق. حد الاستخدام: 100 طلب في الدقيقة.

- **[ترجمة ملف النص](https://docs.aspose.cloud/cells/translate-text-file/)** – ترجمة ملف نصي كامل باستخدام Aspose.Cells Cloud AI.  
  - **طريقة الطلب:** `POST`  
  - **عنوان URL للنقطة النهائية:** `https://api.aspose.cloud/v4.0/cells/ai/translate-text`  
  - **الرؤوس:** `Authorization: Bearer <access_token>`, `Content-Type: multipart/form-data`  
  - **معلمات الطلب:**  
    - `file` – ملف النص المراد ترجمته (ثنائي).  
    - `targetLanguage` – رمز اللغة حسب المعيار الدولي (مثل `es`, `ja`).  
  - **الاستجابة:** تُعيد ملف النص المُترجَم.  
  - **رموز الحالة:** `200 OK`، `400 Bad Request`، `401 Unauthorized`، `415 Unsupported Media Type`، `500 Internal Server Error`  
  - **المتطلبات المسبقة:** رمز وصول صالح مع نطاق **CellsAI**.  
  - **مثال على استجابة (مقتطف JSON):**  
    ```json
    {
      "translatedFileId": "a1b2c3d4",
      "downloadUrl": "https://api.aspose.cloud/v4.0/cells/ai/files/a1b2c3d4"
    }
    ```  
  - **ملاحظات:** يدعم ملفات النصوص العادية المشفرة بـ UTF‑8 يصل حجمها إلى 5 ميغا بايت. حد الاستخدام: 100 طلب في الدقيقة.