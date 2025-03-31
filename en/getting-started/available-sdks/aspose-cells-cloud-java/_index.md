---
title: "Aspose.Cells Cloud SDK for Java"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /available-sdks/aspose-cells-cloud-java/
description: "Aspose.Cells Cloud supports Excel to create, convert, merge, split, protected, inner object operation, and so on."
weight: 30
kwords: Excel, Office Cloud, REST API, Spreadsheet, PDF, CSV, Json, Markdwon, Java
---


The SDK is open-source and licensed under the MIT License. You can access the Java library source code for Aspose.Cells Cloud [here](https://github.com/aspose-cells-cloud/aspose-cells-cloud-java).

# **How to use Java library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Java is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Java programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Java to perform some common tasks, such as creating a new Excel workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Go, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to use Maven to add dependencies for Aspose.Cells Cloud

In your Maven project, add dependencies for the Aspose.Cells Cloud SDK. Include the following dependencies in the pom.xml file:

**Aspose Maven Repository**

```java

<repositories>
    <repository>
        <id>aspose-cloud-repository</id>
        <name>Aspose Cloud Repository</name>
        <url>https://repository.aspose.cloud/repo/</url>
    </repository>
</repositories>

```

**Maven Dependency**

```java

<dependency>
      <groupId>com.aspose</groupId>
      <artifactId>aspose-cloud-cells</artifactId>
      <version>24.5</version>
</dependency>

```

## How to use Java package to convert Xlsx to PDF

- Import Aspose.Cells Cloud Library
  Begin by importing the necessary package from the Aspose.Cells Cloud Java SDK into your project.
- Configure API Client with Credentials
  Authenticate your API client with your unique client ID and client secret.
- Prepare Conversion Parameters
  Define parameters for the conversion task, including the source file name, desired output format, and the storage folder path.
- Execute Workbook Conversion
  Invoke the conversion process using the PostConvertWorkbook method and handle the response.

### **Sample Code**

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}
