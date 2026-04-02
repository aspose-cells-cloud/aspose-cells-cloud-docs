---
title: "Aspose.Cells Cloud SDK for Ruby: Convert, merge, split, protect, search, replace, and more"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Ruby: Convert, merge, split, protect, search, replace, and more"
linktitle: "Aspose.Cells Cloud SDK for Ruby"
type: docs
url: /available-sdks/aspose-cells-cloud-ruby/
description: "The Aspose.Cells Cloud SDK for Ruby provides a fluent, cross‑platform API for creating, converting, merging, splitting, protecting, searching, and replacing Excel objects without requiring Office installations."
weight: 30
keywords: "Ruby, Aspose.Cells Cloud, Excel SDK, REST API, Convert, Merge, Split, Protect, Search, Replace, Chart, Pivot Table, Table/List Object, PDF, CSV, JSON, Markdown"
---

The SDK is open‑source and licensed under the MIT License. You can access [the Ruby library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-ruby).

# **How to use Aspose.Cells Cloud SDK for Ruby**

Aspose.Cells Cloud SDK for Ruby is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Ruby programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we'll explore how to use Aspose.Cells Cloud SDK for Ruby to perform common tasks such as creating a new workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for Ruby, you need to set up your development environment and install the necessary dependencies. Refer to [the article](https://docs.aspose.cloud/cells/quickstart/) on the Aspose website to obtain your client ID and client secret.

## How to install the Ruby package for Aspose.Cells Cloud

You can install Aspose.Cells Cloud SDK for Ruby with the following command:

```bash
gem install aspose_cells_cloud
```

## How to use the Ruby package to convert XLSX to other formats

- **Import Aspose.Cells Cloud library**  
  Begin by requiring the Aspose.Cells Cloud Ruby SDK in your project.

- **Configure the API client with credentials**  
  Authenticate the client using your client ID and client secret.

- **Prepare conversion parameters**  
  Define the source file name, desired output format, and the storage folder path.

- **Execute workbook conversion**  
  Call the `post_convert_workbook` method and handle the response.

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_AvailableSDKs.rb" >}}