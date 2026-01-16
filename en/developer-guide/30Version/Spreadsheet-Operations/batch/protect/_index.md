---
title: "Batch Protect Excel Files"
second_title: "Document"
type: docs
url: /batch/protect
keywords: "Batch Protect Excel Files, Aspose Cells Cloud, REST API, Excel protection, batch protection"
description: "Learn how to use Aspose.Cells Cloud REST API to batch protect multiple Excel files. Includes request details, cURL example, and SDK code samples for various languages."
weight: 100
---

This REST API enables **batch protection** of eligible Excel files.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/batch/protect
```

The request parameters are:

| Parameter Name        | Type                | Location | Description                                                                                              |
|-----------------------|---------------------|----------|----------------------------------------------------------------------------------------------------------|
| batchProtectRequest   | BatchProtectRequest | body     | JSON payload that specifies the source folder, match conditions, protection type, password, and output folder. |

### BatchProtectRequest Properties

| Name            | Type                     | Description                                                                                 | Notes |
|-----------------|--------------------------|---------------------------------------------------------------------------------------------|-------|
| SourceFolder    | string                   | Folder containing the source Excel files.                                                   | optional |
| MatchCondition  | MatchConditionRequest   | Criteria used to select files for protection.                                               | optional |
| ProtectionType  | string                   | Type of protection to apply (e.g., `All`, `ReadOnly`).                                      | optional |
| Password        | string                   | Password to set for the protected files.                                                    | optional |
| OutFolder       | string                   | Destination folder for the protected files.                                                 | optional |

### MatchConditionRequest Properties

| Name                | Type       | Description                                   | Notes |
|---------------------|------------|-----------------------------------------------|-------|
| RegexPattern        | string     | Regular expression used to match file names. | optional |
| FullMatchConditions | string[]   | List of exact file name conditions.          | optional |

The [OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PostProtectConvert) defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser.

You can use the cURL command‑line tool to access Aspose.Cells web services easily. The following example shows how to make a call to the Cloud API with cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "http://api.aspose.cloud/v3.0/cells/batch/protect" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\",\"ProtectionType\":\"All\"}"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK Family

Using an SDK is the best way to speed up development. An SDK handles low‑level details and lets you focus on your project tasks. Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.

The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchProtect.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchProtect.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchProtect.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchProtect.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchProtect.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchProtect.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchProtect.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchProtect.go" >}}

{{< /tab >}}

{{< /tabs >}}