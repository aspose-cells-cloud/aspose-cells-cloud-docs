---
title: Aspose.Cells Cloud SDK لـ G
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ar/available-sdks/aspose-cells-cloud-go/
description: يوفر Aspose.Cells Cloud SDK for Go دعمًا قويًا عبر الأنظمة الأساسية لمطوري Go، مما يجعل من السهل التكامل والاستخدام مع Windows أو Linux أو macOS. وهو يدعم Excel لإنشاء وتحويل ودمج وتقسيم وحماية وتشغيل الكائن الداخلي وما إلى ذلك
weight: 30
kwords: Go, Excel, Office Cloud, REST API, Chart, Pivot Table, Table, Spreadsheet, PDF, CSV, Json, Markdown
---
 SDK مفتوح المصدر ومرخص بموجب ترخيص MIT. يمكنك الوصول إلى الكود المصدري لمكتبة Go لـ Aspose.Cells Cloud[هنا](https://github.com/aspose-cells-cloud/aspose-cells-cloud-go).

# **كيفية استخدام مكتبة Go الخاصة بـ Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Go هي مكتبة قوية تسمح للمطورين بمعالجة ومعالجة ملفات Microsoft Excel باستخدام لغة برمجة Go. باستخدام SDK هذا، يمكنك إنشاء وتحرير وتحويل Excel مستندًا في السحابة، دون تثبيت برامج أو تبعيات إضافية على جهازك المحلي.

في هذه المقالة، سنستكشف كيفية استخدام Aspose.Cells Cloud SDK for Go لتنفيذ بعض المهام الشائعة، مثل إنشاء مصنف Excel جديد، وإدراج البيانات في الخلايا، وحفظ المصنف المعدل في السحابة.

## **ابدء**

 قبل أن تتمكن من البدء في استخدام Aspose.Cells Cloud SDK for Go، تحتاج إلى إعداد بيئة التطوير الخاصة بك وتثبيت التبعيات اللازمة. تشير إلى[المقالة](https://docs.aspose.cloud/cells/quickstart/) على الموقع الإلكتروني Aspose للحصول على معرف العميل وسر العميل.

## كيفية تثبيت حزمة Go لـ Aspose.Cells Cloud

يمكنك تثبيت Aspose.Cells Cloud SDK for Go باستخدام الأمر `go get`. افتح المحطة الطرفية أو موجه الأوامر وقم بتشغيل الأمر التالي:

```bash
go get -u github.com/aspose-cells-cloud/aspose-cells-cloud-go
```

سيؤدي هذا إلى تنزيل أحدث إصدار من SDK وتثبيته على مساحة عمل Go الخاصة بك.


## كيفية استيراد مكتبة Go إلى مشروعك


```golang
package main

import (
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
```

## كيفية استخدام حزمة Go لتحويل XLsx إلى PDF

- استيراد Aspose.Cells المكتبة السحابية
ابدأ باستيراد الحزمة الضرورية من Aspose.Cells Cloud Go SDK إلى مشروعك.
- قم بتكوين API عميل ببيانات الاعتماد
 قم بتوثيق عميلك API بمعرف العميل الفريد وسر العميل.
- إعداد معلمات التحويل
 حدد المعلمات لمهمة التحويل، بما في ذلك اسم الملف المصدر، وتنسيق الإخراج المطلوب، ومسار مجلد التخزين.
- تنفيذ تحويل المصنف
 استدعاء عملية التحويل باستخدام أسلوب PostConvertWorkbook والتعامل مع الاستجابة.

### **عينة من الرموز**

```golang
package main

import (
	"os"
	asposecellscloud "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)
func main() {
	instance := asposecellscloud.NewCellsApiService(os.Getenv("ProductClientId"), os.Getenv("ProductClientSecret"), "https://api.aspose.cloud", "v3.0")
    remoteFolder := "TestData/In"

    localName := "Book1.xlsx"
    remoteName := "Book1.xlsx"

    format := "pdf"

    var mapFiles map[string]string       
    mapFiles = make(map[string]string)
    mapFiles[localName]=  localName 

    request := new (asposecellscloud.PutConvertWorkbookRequest)
    request.File =         mapFiles    
    request.Format =         format    
    _, httpResponse, err := instance.PutConvertWorkbook(request)
    if err != nil {
      print(err)
    } else if httpResponse.StatusCode < 200 || httpResponse.StatusCode > 299 {
      print("Test fail")
    }
}

```
