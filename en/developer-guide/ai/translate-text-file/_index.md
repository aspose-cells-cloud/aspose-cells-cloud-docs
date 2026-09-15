---
url: /translate-text-file/
title: Translate Text File with AI-Powered Language Conversion
type: docs
description: Use Aspose.Cells Cloud's AI-powered TranslateTextFile API to convert text files into any supported language via REST. Supports file upload or raw text input, preserves formatting, and integrates with major SDKs.
keywords: AI text translation, Aspose.Cells Cloud API, REST API translate file, multilingual spreadsheet, neural machine translation
date: 2024-03-15
lastmod: 2024-04-27
tags: ["ai-translation", "rest-api", "multilingual", "cloud"]
categories: ["cells-api", "automation"]
weight: 100
---

## Overview

The **TranslateTextFile** endpoint leverages Aspose.Cells Cloud AI services to translate the content of a text file into a specified target language. It supports two operation modes:

1. **File Upload Mode** – send a text file via `multipart/form-data` and receive a translated file as a downloadable binary stream.
2. **Direct Content Mode** – post raw text in the request body and receive the translated text directly.

The service preserves original line breaks, indentation, and special characters, automatically appends a `_translated` suffix to uploaded filenames, and returns the result as a binary stream.

> **Prerequisites**  
> Before using this API, you need an [App SID and App Key](https://dashboard.aspose.cloud/) from the Aspose Cloud Dashboard. See the [Authentication Guide](/cells-cloud/authentication/) for implementation details.

---

## API Endpoint

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

> **Note**: This endpoint follows [SemVer](https://semver.org/) versioning. v4.0 is current as of April 2024. See the [API Versioning Policy](/cells-cloud/api-versioning/) for deprecation notices and upgrade guidance.

---

## Request Parameters

| Parameter Name | Type   | Location | Required | Description |
|:---------------|:-------|:---------|:---------|:------------|
| Spreadsheet    | File   | FormData | Yes      | The source file to translate. Accepts plain-text (`.txt`) or supported spreadsheet formats (e.g., `.csv`, `.xlsx`). Use form field name `file` in `multipart/form-data`. |
| targetLanguage | String | Query    | Yes      | ISO 639-1 language code for the target language (e.g., `es`, `fr`, `de`). Case-insensitive. |
| region         | String | Query    | No       | Locale identifier (e.g., `en-US`, `fr-FR`, `zh-CN`) that influences date, number, and currency formatting. **Note**: Only applies to spreadsheet inputs; ignored for plain-text files. |
| password       | String | Query    | No       | Password to decrypt encrypted spreadsheet files. Not required for plain-text (`.txt`) files. |

---

## Response

### Successful Response (200 OK)

**Headers**  
- `Content-Type: application/octet-stream`  
- `Content-Disposition: attachment; filename="<original_name>_translated.txt"`  
- `Content-Length: <size_in_bytes>`

**Body**  
Binary stream containing the translated content with preserved formatting, line breaks, and character encoding.

### Error Responses

| Code | Meaning               | Description |
|:-----|:----------------------|:------------|
| 200  | OK                    | Translation completed successfully. |
| 400  | Bad Request           | Missing `targetLanguage`, unsupported file type, empty payload, or invalid `region` code. |
| 401  | Unauthorized          | Invalid, expired, or missing JWT token. |
| 413  | Payload Too Large     | File size exceeds the 2 GB limit. |
| 500  | Internal Server Error | Translation service unavailable or internal processing failure. |

For authentication issues, see [Authentication Troubleshooting](/cells-cloud/authentication/#troubleshooting).

---

## Use Cases

- **Multilingual Documentation Portals**  
  Automatically translate user manuals or help files into regional languages on demand.

- **Content Management Systems (CMS)**  
  Integrate translation into publishing workflows to localize blog posts, articles, or product descriptions.

- **Enterprise Data Pipelines**  
  Process large batches of CSV/TXT reports, converting them to the language of regional offices while preserving formatting.

- **Customer Support Platforms**  
  Translate incoming plain-text tickets or chat logs in real time for agents working in multiple languages.

---

## Why Use This API?

- **AI-Driven Accuracy**  
  Powered by state-of-the-art neural machine translation models for context-aware, natural-sounding output.

- **Dual Input Flexibility**  
  Supports both file uploads and raw text payloads, simplifying integration across client and server environments.

- **Format Preservation**  
  Maintains line breaks, indentation, and special characters—no post-processing cleanup needed.

- **Seamless File Handling**  
  Automatically appends `_translated` to filenames for uploaded files, reducing client-side logic.

---

## How to Use the API

### 1. File Upload Mode (Multipart/Form-Data)

**cURL Example**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/ai/translate/text-file?targetLanguage=es" \
  -H "Authorization: Bearer <JWT token>" \
  -F "file=@document.txt"
```

### 2. Direct Content Mode (Raw Text)

**cURL Example**
```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/ai/translate/text-file?targetLanguage=fr&region=fr-FR" \
  -H "Authorization: Bearer <JWT token>" \
  -H "Content-Type: text/plain" \
  -d "Hello, this is a test message."
```

> **Tip**: For large files, use the [UploadFile API](/cells-cloud/file-handling/#upload-file) first, then reference the uploaded file with the [TranslateTextFileWithFileId](/cells-cloud/ai/#translate-text-file-by-id) endpoint.

---

## SDK Examples

Aspose.Cells Cloud SDKs abstract low-level HTTP details and simplify integration. Below are ready-to-run examples in popular languages.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go">}}
{{<tab tabNum="1">}}
```csharp
// Install Aspose.Cells.Cloud SDK via NuGet: Install-Package Aspose.Cells.Cloud

var cellsApi = new CellsApi("your_app_sid", "your_app_key");
using var fileStream = File.OpenRead("document.txt");
var response = await cellsApi.CellsAiTranslateTextFileAsync(
    file: fileStream,
    targetLanguage: "es"
);
Console.WriteLine($"Translated file saved as: {response.Name}");
```
{{</tab>}}
{{<tab tabNum="2">}}
```java
// Install Aspose.Cells.Cloud SDK via Maven: com.aspose:aspose-cells-cloud:22.3

CellsApi cellsApi = new CellsApi("your_app_sid", "your_app_key");
File file = new File("document.txt");
TranslateTextFileResponse response = cellsApi.cellsAiTranslateTextFile(
    "es", null, null, file, null
);
System.out.println("Translated file: " + response.getName());
```
{{</tab>}}
{{<tab tabNum="3">}}
```php
// Install via Composer: composer require aspose/cells-cloud

use Aspose\Cells\CellsApi;
use Aspose\Cells\Cloud\Configuration;

$configuration = new Configuration();
$configuration->setAppSid("your_app_sid");
$configuration->setAppKey("your_app_key");
$cellsApi = new CellsApi($configuration);

$file = realpath("document.txt");
$response = $cellsApi->cellsAiTranslateTextFile("es", null, null, $file);
echo "Translated file: " . $response->getName();
```
{{</tab>}}
{{<tab tabNum="4">}}
```ruby
# Install: gem install aspose_cells_cloud

require 'aspose_cells_cloud'

@cells_api = AsposeCellsCloud::API.new(
  client_id: "your_app_sid",
  client_secret: "your_app_key"
)

response = @cells_api.cells_ai_translate_text_file(
  target_language: "de",
  file: File.new("document.txt", 'r')
)
puts "Translated file: #{response.name}"
```
{{</tab>}}
{{<tab tabNum="5">}}
```javascript
// Install: npm install @aspose/cells-cloud

const cellsApi = new CellsApi("your_app_sid", "your_app_key");
const response = await cellsApi.cellsAiTranslateTextFile(
  "es", 
  { file: fs.createReadStream("document.txt") }
);
console.log("Translated file:", response.name);
```
{{</tab>}}
{{<tab tabNum="6">}}
```python
# Install: pip install asposecellscloud

from asposecellscloud.api import CellsApi
from asposecellscloud.models import TranslateTextFileRequest

api = CellsApi("your_app_sid", "your_app_key")
with open("document.txt", "rb") as f:
    response = api.cells_ai_translate_text_file(
        target_language="fr",
        file=f
    )
print(f"Translated file: {response.name}")
```
{{</tab>}}
{{<tab tabNum="7">}}
```perl
use AsposeCellsCloud::Configuration;
use AsposeCellsCloud::CellsApi;

my $config = AsposeCellsCloud::Configuration->new(
  app_sid => 'your_app_sid',
  app_key => 'your_app_key'
);
my $api = AsposeCellsCloud::CellsApi->new(config => $config);

my $file = 'document.txt';
my $response = $api->cells_ai_translate_text_file(
  target_language => 'de',
  file => $file
);
print "Translated file: " . $response->{name} . "\n";
```
{{</tab>}}
{{<tab tabNum="8">}}
```go
// Install: go get github.com/aspose-cells-cloud/aspose-cells-cloud-go

import (
  "context"
  "os"
  "github.com/aspose-cells-cloud/aspose-cells-cloud-go"
)

config := cells.NewConfiguration()
config.AppSid = "your_app_sid"
config.AppKey = "your_app_key"
client := cells.NewAPIClient(config)

file, _ := os.Open("document.txt")
defer file.Close()

resp, _, err := client.AiController.CellsAiTranslateTextFile(context.Background()).
  TargetLanguage("es").
  File(file).
  Execute()
if err != nil {
  log.Fatal(err)
}
fmt.Printf("Translated file: %s\n", *resp.Name)
```
{{</tab>}}
{{</tabs>}}

> **Note**: All SDK examples assume valid authentication credentials. For troubleshooting, see [Common SDK Errors](/cells-cloud/sdk-troubleshooting/).

---

## Related Resources

- [Authentication Guide](/cells-cloud/authentication/)  
- [File Handling & Uploads](/cells-cloud/file-handling/)  
- [AI API Overview](/cells-cloud/ai/)  
- [API Reference: TranslateTextFile](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile)  

---

## Changelog

| Date       | Version | Changes |
|:-----------|:--------|:--------|
| 2024-04-27 | v4.0    | Added support for direct text input mode; clarified `region` parameter scope; updated SDK examples. |
| 2024-03-15 | v4.0    | Initial stable release of the AI-powered `TranslateTextFile` endpoint. |