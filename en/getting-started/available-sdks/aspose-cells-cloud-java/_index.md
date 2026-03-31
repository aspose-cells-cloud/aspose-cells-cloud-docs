---
title: "Aspose.Cells Cloud SDK for Java: Convert, merge, split, protect, search, replace, and more"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Java: Convert, merge, split, protect, search, replace, and more"
linktitle: "Aspose.Cells Cloud SDK for Java"
type: docs
url: /available-sdks/aspose-cells-cloud-java/
description: "Use Aspose.Cells Cloud Java SDK to create, convert, merge, split, protect, search & replace Excel files without Office installed."
weight: 30
keywords: "Aspose Cells Java SDK, Excel conversion Java, Cloud spreadsheet API, Java Excel library, Aspose.Cells Cloud Java"
---

The SDK is open‑source and licensed under the MIT License. You can access [the Java library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **How to use Java library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Java is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Java programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we’ll explore how to use Aspose.Cells Cloud Java SDK to perform common tasks such as creating a new workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for **Java**, set up your development environment and install the required dependencies. Refer to the official [Aspose.Cells Cloud quick‑start guide](https://docs.aspose.cloud/cells/quickstart/) to obtain your **client ID** and **client secret**.

## Prerequisites

- **Java version** ≥ 11  
- **Maven** or **Gradle** for dependency management  
- An active **Aspose Cloud** account (client ID & client secret)  
- A storage bucket configured in Aspose Cloud (default “Default” storage works for most scenarios)

## How to use Maven to add dependencies for Aspose.Cells Cloud

In your Maven project, add the Aspose repository and the SDK dependency to `pom.xml`:

**Aspose Maven Repository**

```xml
<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>
```

**Maven Dependency**

```xml
<dependency>
    <groupId>com.aspose</groupId>
    <artifactId>aspose-cloud-cells</artifactId>
    <version>24.5</version>
</dependency>
```

## How to use Java package to convert Xlsx to PDF

1. **Import the SDK classes**  
   ```java
   import com.aspose.cloud.cells.ApiException;
   import com.aspose.cloud.cells.api.CellsApi;
   import com.aspose.cloud.cells.client.ApiClient;
   import com.aspose.cloud.cells.model.*;
   import java.io.FileOutputStream;
   import java.io.InputStream;
   ```

2. **Configure API client with credentials**  
   ```java
   ApiClient apiClient = new ApiClient();
   apiClient.setAppKey("YOUR_CLIENT_ID");      // clientId
   apiClient.setAppSid("YOUR_CLIENT_SECRET");  // clientSecret
   CellsApi cellsApi = new CellsApi(apiClient);
   ```

3. **Upload the source workbook (if it is not already in cloud storage)**  
   ```java
   String localFile = "sample.xlsx";
   InputStream fileStream = Files.newInputStream(Paths.get(localFile));
   cellsApi.uploadFile("sample.xlsx", fileStream, null);
   ```

4. **Prepare conversion parameters and execute the conversion**  
   ```java
   ConvertWorkbookRequest request = new ConvertWorkbookRequest();
   request.setFileName("sample.xlsx");
   request.setOutputFormat("pdf");
   request.setStorageName(null);          // use default storage
   request.setFolder(null);               // root folder

   InputStream pdfStream = cellsApi.postConvertWorkbook(request);
   ```

5. **Save the resulting PDF locally (or re‑upload to cloud storage)**  
   ```java
   try (FileOutputStream out = new FileOutputStream("sample.pdf")) {
       pdfStream.transferTo(out);
   }
   ```

### Sample Code

```java
import com.aspose.cloud.cells.ApiException;
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.client.ApiClient;
import com.aspose.cloud.cells.model.ConvertWorkbookRequest;
import java.io.FileOutputStream;
import java.io.InputStream;
import java.nio.file.Files;
import java.nio.file.Paths;

public class ConvertXlsxToPdf {
    public static void main(String[] args) throws Exception {
        // 1. Initialise API client
        ApiClient apiClient = new ApiClient();
        apiClient.setAppKey("YOUR_CLIENT_ID");
        apiClient.setAppSid("YOUR_CLIENT_SECRET");
        CellsApi cellsApi = new CellsApi(apiClient);

        // 2. Upload source file (optional if already in cloud)
        try (InputStream uploadStream = Files.newInputStream(Paths.get("sample.xlsx"))) {
            cellsApi.uploadFile("sample.xlsx", uploadStream, null);
        }

        // 3. Convert workbook to PDF
        ConvertWorkbookRequest convertRequest = new ConvertWorkbookRequest();
        convertRequest.setFileName("sample.xlsx");
        convertRequest.setOutputFormat("pdf");
        InputStream pdfStream = cellsApi.postConvertWorkbook(convertRequest);

        // 4. Save PDF locally
        try (FileOutputStream out = new FileOutputStream("sample.pdf")) {
            pdfStream.transferTo(out);
        }

        System.out.println("Conversion completed: sample.pdf");
    }
}
```

## Next Steps / Common Use‑Cases

- Convert to other formats (e.g., **XLS**, **CSV**, **HTML**) by changing `outputFormat`.  
- Merge multiple workbooks using `cellsApi.postMergeWorkbooks`.  
- Protect worksheets or the entire workbook with passwords.  
- Search and replace cell values via `cellsApi.postWorksheetRangeReplace`.  

## FAQ

### How do I authenticate the Aspose.Cells Cloud Java SDK?

Create an `ApiClient` instance, set your `clientId` (`AppKey`) and `clientSecret` (`AppSid`), and pass the client to `CellsApi`. The code snippet in the **Configure API client** step demonstrates this.

### How can I convert an XLSX file to PDF using the SDK?

Use the `postConvertWorkbook` method as shown in the **Prepare conversion parameters** step. The method returns an `InputStream` that you can write to a file or upload back to cloud storage.

### What Maven dependencies are required?

Add the Aspose Cloud repository and the `aspose-cloud-cells` dependency (version 24.5) to your `pom.xml`. See the **How to use Maven** section for the exact XML snippets.

### Where can I find the full API reference?

The official reference is available at <https://reference.aspose.cloud/cells/java/>. Each method used in this guide (e.g., `uploadFile`, `postConvertWorkbook`) is documented there with parameter details and response types.

---