---
title: "Aspose.Cells Cloud Web API – Translate Text File with AI-Powered Language Conversion"
second_title: "Document"
ArticleTitle: "How to Translate Text Files Using Aspose.Cells Cloud AI Translation API"
linktitle: "Translate Text File"
type: docs
url: /translate-text-file/
keywords: "Aspose.Cells, Cloud API, AI translation, translate text file, multilingual conversion, REST PUT, target language code, file upload translation, raw text translation, spreadsheet AI"
description: "Learn how to use the Aspose.Cells Cloud AI TranslateTextFile endpoint to convert text files into any supported language. Supports both multipart file upload and raw text payload, preserves formatting, and returns a downloadable translated file."
weight: 100
---

The **TranslateTextFile** endpoint leverages Aspose.Cells Cloud AI services to translate the content of a text file into a specified target language. It supports two operation modes: (1) **File Upload Mode** – send a text file via multipart/form-data and receive a translated file; (2) **Direct Content Mode** – post raw text in the request body and get the translated text directly. The service preserves original line breaks and formatting, automatically appends a "\_translated" suffix to the filename, and returns the result as a downloadable stream. Ideal for batch translation of documents, integration into multilingual workflows, or on‑the‑fly translation of user‑generated content.

## **Translate Text File API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Request Parameters:**

| Parameter Name | Type   | Location | Required/Optional | Description                                                                                                                                                                    |
| :------------- | :----- | :------- | :---------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet    | File   | Required | FormData          | The source text file to be translated. Must be a plain‑text (.txt) or supported spreadsheet format. Example: upload `document.txt` via multipart/form-data field named "file". |
| targetLanguage | String | Required | Query             | ISO‑639‑1 language code of the desired output (e.g., "es" for Spanish, "fr" for French, "de" for German). The code is case‑insensitive.                                        |
| region         | String | Optional | Query             | Optional region hint for the translation service (e.g., "us-east", "eu-west"). If omitted, the service selects the default region.                                             |
| password       | String | Optional | Query             | Password required to open encrypted spreadsheet files. Not needed for plain‑text files.                                                                                        |

### **Response**

Successful response (200 OK)
Headers:
Content-Type: application/octet-stream // binary stream of the translated file
Content-Disposition: attachment; filename="<original_name>\_translated.txt"
Content-Length: <size in bytes>

Body: binary stream containing the translated text preserving original line breaks and formatting.

### Error Codes

- **400 Bad Request**: Invalid Aspose.Cells Cloud API URI.
- **401 Unauthorized**: Invalid access token. Or invalid client id and secret.
- **404 Not Found**: The spreadsheet file not accessible.
- **500 Server Error**: The spreadsheet has encountered an anomaly in obtaining calculation data.

## Where should we use the Translate Text File API?

- **Multilingual Documentation Portals** – Automatically translate user manuals or help files uploaded as text documents, delivering localized versions on demand.
- **Content Management Systems (CMS)** – Integrate into a CMS workflow to translate blog posts or articles before publishing to international audiences.
- **Enterprise Data Pipelines** – Use in batch jobs that process large volumes of CSV or TXT reports, converting them to the language of regional offices while keeping original formatting.
- **Customer Support Platforms** – Translate incoming plain‑text tickets or chat logs in real time to assist support agents working in different languages.

## Why should you use the Translate Text File API?

- **AI‑Driven Accuracy** – Leverages state‑of‑the‑art neural translation models for natural, context‑aware output.
- **Dual Input Flexibility** – Accepts both file uploads and raw text payloads, simplifying integration with diverse client applications.
- **Preserves Original Layout** – Maintains line breaks, indentation, and special characters, eliminating post‑processing cleanup.
- **Seamless File Handling** – Returns a ready‑to‑download file with an auto‑generated "\_translated" suffix, reducing client‑side code complexity.

## How to Use the Translate Text File API with SDKs

### Translate Text File API Specification

The [Translate Text File API Specification](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) provides a publicly accessible programming interface for executing REST interactions directly from a web browser.

## Excel API SDK

### Use Aspose.Cells Cloud SDKs

Using the SDK is the fastest way to develop, as it abstracts away the low-level details, allowing you to merge a spreadsheet into another spreadsheet with short code.
Please check out the [GitHub repository](https://github.com/aspose-cells-cloud) for a complete list of Aspose.Cells Cloud SDKs.
The following code examples demonstrate how to interact with Aspose.Cells web services using various SDKs:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}
