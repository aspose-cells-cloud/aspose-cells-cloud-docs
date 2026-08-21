---
title: "حذف مجلد – واجهة برمجة تطبيقات Aspose.Cells السحابية | إزالة المجلدات عبر REST"
description: "تعرّف على كيفية حذف مجلد (اختياريًا بشكل متكرر) من مساحة التخزين السحابية لـ Aspose.Cells باستخدام نقطة نهاية DELETE /v4.0/cells/storage/folder/{path}. يتضمن بناء الجملة المطلوبة للمُطلب، والمعاملات، والمصادقة، ونموذج من الكود، ومعالجة الأخطاء."
keywords: "Aspose.Cells, حذف مجلد, مساحة تخزين سحابية, واجهة برمجة تطبيقات, REST, Excel, إدارة الملفات"
slug: delete-folder
date: 2026-07-30
---

# حذف مجلد – واجهة برمجة تطبيقات Aspose.Cells السحابية

قم بإزالة مجلد (وبشكل اختياري محتوياته بالكامل) من مساحة التخزين السحابية لـ Aspose.Cells.

---

## نظرة عامة

يؤدي تشغيل **حذف المجلد** إلى إزالة المجلد بشكل دائم من حساب التخزين المستخدم من قِبل Aspose.Cells Cloud.  
يمكنك حذف مجلد فارغ، أو، بضبط علامة `recursive` على `true`، حذف المجلد مع جميع الملفات والمجلدات الفرعية الموجودة بداخله. تُستخدم هذه النقطة النهائية عادةً في سكريبتات التنظيف، أو سير العمل الآلية، أو عند عدم الحاجة بعدُ إلى المجلدات المؤقتة.

---

## طلب HTTP

```
DELETE https://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

*`{path}`* – المسار الكامل للمجلد المراد حذفه (مشفر حسب URL).

### رؤوس HTTP المطلوبة

| الرأس               | القيمة                              | الوصف                              |
|---------------------|-------------------------------------|------------------------------------|
| `Authorization`     | `Bearer {access_token}`             | رمز JWT المُستخلص من خدمة المصادقة. |
| `Accept`            | `application/json`                  | تنسيق الاستجابة المتوقع.           |
| `Content-Type`      | `application/json` *(اختياري)*      | غير مطلوب لطلب DELETE، لكن يمكن إرساله. |

---

## المصادقة

تستخدم Aspose.Cells Cloud **المصادقة القائمة على رموز JWT**.  
احصل على رمز وصول عبر [نقطة نهاية المصادقة](/authentication/) وأدرجها في الرأس `Authorization` كما هو موضح أعلاه.

```bash
-H "Authorization: Bearer {access_token}"
```

---

## المعاملات

| الاسم             | النوع     | الموقع       | الإجبارية | الوصف                                                               |
|-------------------|-----------|--------------|-----------|----------------------------------------------------------------------|
| `path`            | سلسلة نصية | المسار      | نعم       | مسار المجلد المراد حذفه (مشفر حسب URL).                               |
| `storageName`     | سلسلة نصية | الاستعلام  | لا         | اسم مساحة التخزين التي يحتوي المجلد عليها. إذا تم حذفها، تُستخدم مساحة التخزين الافتراضية. |
| `recursive`       | منطقي     | الاستعلام  | لا         | `true` → حذف المجلد **ومحتوياته بالكامل**. القيمة الافتراضية هي `false`. |

**مثال على سلسلة استعلام**

```
?storageName=MyStorage&recursive=true
```

---

## مثال على الطلب (cURL)

```bash
curl -X DELETE "https://api.aspose.cloud/v4.0/cells/storage/folder/MyFolder?storageName=MyStorage&recursive=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

---

## الاستجابة

يُعيد الطلب الناجح **HTTP 200 OK** مع كائن JSON فارغ:

```json
{}
```

لا تُقدَّم أي حمولة إضافية لأن نتيجة العملية ثنائية – إما أن يُحذف المجلد أو يُعاد خطأ.

---

**رموز حالة HTTP**

| الرمز | المعنى                     | الوصف                                      |
|-------|----------------------------|--------------------------------------------|
| 200   | OK                         | تطبيق العامل بنجاح؛ تحتوي الاستجابة على تفاصيل العملية. |
| 400   | طلب غير صالح              | معاملات مفقودة أو غير صحيحة (مثل نوع ملف غير مدعوم). |
| 401   | غير مصرّح به              | رمز JWT غير صالح أو مفقود. |
| 413   | حملة البيانات كبيرة جدًا   | ملف مُرفَع يتجاوز الحد الأقصى للحجم. |
| 500   | خطأ داخلي في الخادم        | خطأ غير متوقع في الخادم. |

عند حدوث خطأ، تحتوي الحمولة على كائن JSON يحتوي على حقلَي `code` و `message` لوصف المشكلة.

---

## أمثلة للكود باستخدام SDKs

توضح الأمثلة التالية كيفية استدعاء **حذف المجلد** باستخدام SDKs المدعومة رسميًا. استبدل `{access_token}` وقيم المعاملات بقيمك الخاصة.

<details><summary>🟦 C# (dotnet)</summary>

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// تهيئة عميل واجهة برمجة التطبيقات
var config = new Configuration
{
    AccessToken = "{access_token}",
    BasePath = "https://api.aspose.cloud"
};

var folderApi = new FolderApi(config);

// حذف المجلد (بشكل متكرر)
var request = new DeleteFolderRequest
{
    Path = "MyFolder",
    StorageName = "MyStorage",
    Recursive = true
};

folderApi.DeleteFolder(request);
```
</details>

<details><summary>🟨 Java</summary>

```java
import com.aspose.cloud.cells.api.FolderApi;
import com.aspose.cloud.cells.model.*;
import com.aspose.cloud.cells.model.requests.DeleteFolderRequest;

// تهيئة عميل واجهة برمجة التطبيقات
FolderApi folderApi = new FolderApi("{access_token}");

DeleteFolderRequest request = new DeleteFolderRequest()
        .path("MyFolder")
        .storageName("MyStorage")
        .recursive(true);

folderApi.deleteFolder(request);
```
</details>

<details><summary>🟪 PHP</summary>

```php
<?php
require_once 'vendor/autoload.php';

use Aspose\Cells\Cloud\Api\FolderApi;
use Aspose\Cells\Cloud\Configuration;

// التكوين
$config = new Configuration();
$config->setAccessToken('{access_token}');
$config->setHost('https://api.aspose.cloud');

$apiInstance = new FolderApi($config);

// حذف المجلد بشكل متكرر
try {
    $apiInstance->deleteFolder('MyFolder', 'MyStorage', true);
    echo "Folder deleted.";
} catch (Exception $e) {
    echo 'Exception when calling FolderApi->deleteFolder: ', $e->getMessage(), PHP_EOL;
}
?>
```
</details>

<details><summary>🟧 Ruby</summary>

```ruby
require 'aspose_cells_cloud'

config = AsposeCellsCloud::Configuration.new
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

api = AsposeCellsCloud::FolderApi.new

begin
  api.delete_folder('MyFolder', storage_name: 'MyStorage', recursive: true)
  puts 'Folder deleted.'
rescue AsposeCellsCloud::ApiError => e
  puts "Error: #{e.message}"
end
```
</details>

<details><summary>🟢 Node.js (TypeScript)</summary>

```ts
import { FolderApi, DeleteFolderRequest } from '@asposecloud/cells-sdk';

const config = {
    accessToken: '{access_token}',
    basePath: 'https://api.aspose.cloud'
};

const folderApi = new FolderApi(config);

const request: DeleteFolderRequest = {
    path: 'MyFolder',
    storageName: 'MyStorage',
    recursive: true
};

folderApi.deleteFolder(request)
    .then(() => console.log('Folder deleted'))
    .catch(err => console.error('Error:', err));
```
</details>

<details><summary>🐍 Python</summary>

```python
from asposecellscloud import FolderApi, DeleteFolderRequest, Configuration

config = Configuration()
config.access_token = '{access_token}'
config.host = 'https://api.aspose.cloud'

folder_api = FolderApi(config)

request = DeleteFolderRequest(
    path='MyFolder',
    storage_name='MyStorage',
    recursive=True
)

folder_api.delete_folder(request)
print("Folder deleted")
```
</details>

<details><summary>🦪 Perl</summary>

```perl
use AsposeCellsCloud::FolderApi;
use AsposeCellsCloud::Configuration;

my $config = AsposeCellsCloud::Configuration->new(
    access_token => '{access_token}',
    host => 'https://api.aspose.cloud'
);

my $api = AsposeCellsCloud::FolderApi->new($config);

eval {
    $api->delete_folder(
        path => 'MyFolder',
        storage_name => 'MyStorage',
        recursive => 1
    );
    print "Folder deleted.\n";
};
if ($@) {
    warn "Error deleting folder: $@";
}
```
</details>

<details><summary>🦑 Go</summary>

```go
package main

import (
    "context"
    "fmt"
    cells "github.com/asposecellscloud/aspose-cells-cloud-go/v4"
)

func main() {
    cfg := cells.NewConfiguration()
    cfg.AccessToken = "{access_token}"
    cfg.Host = "https://api.aspose.cloud"

    api := cells.NewFolderApi(cfg)

    req := cells.DeleteFolderRequest{
        Path:        "MyFolder",
        StorageName: "MyStorage",
        Recursive:   true,
    }

    _, err := api.DeleteFolder(context.Background(), req)
    if err != nil {
        fmt.Printf("Error: %v\n", err)
        return
    }
    fmt.Println("Folder deleted")
}
```
</details>

---

## انظر أيضًا

- **[إنشاء مجلد](/create-folder/)** – إنشاء مجلد جديد في مساحة التخزين السحابية.  
- **[نسخ مجلد](/copy-folder/)** – تكرار مجلد ومحتوياته.  
- **[نقل مجلد](/move-folder/)** – إعادة تحديد موقع مجلد إلى مسار مختلف.  
- **[مواصفات OpenAPI]** – <a href="https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder" rel="noopener noreferrer">عملية DeleteFolder</a> (مستكشف واجهة برمجة التطبيقات التفاعلي).

---

## قائمة التحقق من SEO والوصول (داخلي)

- يحتوي العنوان ورأس H1 على شَرطة نصف طويلة صحيحة (–) وتحتويان على الكلمة المفتاحية الأساسية *حذف مجلد*.  
- تتبع جميع العناوين تسلسلًا هرميًا منطقيًا (`H1 → H2 → H3`).  
- لا توجد آثار لترميز UTF-8.  
- تم توحيد كلمات مفتاحية Meta في قائمة واحدة نظيفة (أو تُركت حسب التفضيل).  
- تشمل الروابط الخارجية `rel="noopener noreferrer"` للأمان.  
- يجب أن تحمل أي أيقونات واجهة مستخدم وأعلام لغات (إن ظهرت في الصفحة) سمات `aria-label` أو `alt` (مثل `aria-label="English (US)"`).  
- يُوصى بإضافة علامات `<link rel="alternate" hreflang="xx" href="…">` في رأس الصفحة لكل نسخة لغوية.  

---