---
title: "Aspose.Cells Cloud SDK for Perl – Convert, Merge, Split, Protect & More"
second_title: "Document"
ArticleTitle: "Aspose.Cells Cloud SDK for Perl – Convert, Merge, Split, Protect & More"
linktitle: "Aspose.Cells Cloud SDK for Perl"
type: docs
url: /available-sdks/aspose-cells-cloud-perl/
description: "Explore the Aspose.Cells Cloud Perl SDK – a cross‑platform library to create, convert, merge, split, protect, search and replace Excel files without Office installed."
weight: 30
keywords: "Perl SDK, Aspose.Cells Cloud, Excel conversion Perl, Excel SDK for Perl, Cloud SDK"
---

The SDK is open‑source and licensed under the MIT License. You can access [the Perl library source code for Aspose.Cells Cloud](https://github.com/aspose-cells-cloud/aspose-cells-cloud-perl).

# **How to use Perl library of Aspose.Cells Cloud**

Aspose.Cells Cloud SDK for Perl is a powerful library that allows developers to manipulate and process Microsoft Excel files using the Perl programming language. With this SDK, you can create, edit, and convert Excel documents in the cloud, without installing additional software or dependencies on your local machine.

In this article, we’ll explore how to use Aspose.Cells Cloud SDK for Perl to perform common tasks such as creating a new workbook, inserting data into cells, and saving the modified workbook to the cloud.

## Getting Started

Before you can start using the Aspose.Cells Cloud SDK for **Perl**, you need to set up your development environment and install the required dependencies.

* **Perl version** – Perl 5.30 or later is required.  
* **Credentials** – Obtain a *client ID* and *client secret* from the Aspose Cloud console. Set them as environment variables (`ASPOSE_CLIENT_ID`, `ASPOSE_CLIENT_SECRET`) or pass them directly to the API client.  
* **CPAN configuration** – Ensure your CPAN client is configured and can install modules from CPAN.

Refer to the [Aspose quick‑start guide](https://docs.aspose.cloud/cells/quickstart/) for detailed steps on obtaining your credentials.

## How to install the Perl package for Aspose.Cells Cloud

Install the SDK via CPAN:

```perl
# Open a CPAN shell and install the module
perl -MCPAN -e "install AsposeCellsCloud::CellsApi"
```

*On Linux/macOS you may need to prepend `sudo` if you install system‑wide.*

## How to use Perl package to convert Xlsx to other formats

The conversion workflow consists of the following steps:

| Step | Description |
|------|-------------|
| **Import the library** | `use AsposeCellsCloud::CellsApi;` |
| **Configure the API client** | Provide the `client_id` and `client_secret` (or rely on the environment variables). |
| **Upload the source workbook** | Use `UploadFile` to place the XLSX file in the chosen storage folder. |
| **Define conversion parameters** | Specify the source file name, the target format (e.g., `pdf`), and the output path. |
| **Execute the conversion** | Call `PostConvertWorkbook` and capture the response. |
| **Download the result** | Retrieve the converted file from the storage location. |
| **Handle errors** | Check the response status and use `eval { … }` or `$api->error` for exception handling. |

Below is a complete, runnable Perl script that demonstrates an end‑to‑end conversion from **XLSX** to **PDF**, including basic error handling:

```perl
use strict;
use warnings;
use AsposeCellsCloud::CellsApi;

# -----------------------------------------------------------------
# Prerequisites – set these values or export them as environment vars
# -----------------------------------------------------------------
my $client_id     = $ENV{'ASPOSE_CLIENT_ID'}     // 'YOUR_CLIENT_ID';
my $client_secret = $ENV{'ASPOSE_CLIENT_SECRET'} // 'YOUR_CLIENT_SECRET';
my $source_file   = 'sample.xlsx';      # file to upload
my $output_file   = 'sample.pdf';       # desired output name
my $storage_path  = 'MyFolder';         # optional storage folder

# -----------------------------------------------------------------
# Initialise the API client
# -----------------------------------------------------------------
my $api = AsposeCellsCloud::CellsApi->new($client_id, $client_secret);

eval {
    # Upload the source workbook
    $api->UploadFile(
        path      => "$storage_path/$source_file",
        file      => $source_file
    );

    # Convert the workbook
    my $result = $api->PostConvertWorkbook(
        file   => "$storage_path/$source_file",
        format => 'pdf',
        outPath=> "$storage_path/$output_file"
    );

    # Check the conversion result
    if ($result->{status} && $result->{status} eq 'OK') {
        print "Conversion successful: $output_file\n";
    } else {
        die "Conversion failed: " . ($result->{error}->{message} // 'unknown error');
    }
};
if ($@) {
    warn "An error occurred: $@\n";
}
```

**Explanation of the script**

* `use strict; use warnings;` – Enforces good Perl coding practices.  
* `AsposeCellsCloud::CellsApi->new` – Creates an authenticated client.  
* `UploadFile` – Places the source workbook in the cloud storage.  
* `PostConvertWorkbook` – Performs the conversion; `format => 'pdf'` selects PDF output.  
* The `eval` block captures any runtime exceptions, and the final `if ($@)` prints a helpful error message.

---

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_AvailableSDKs.pl" >}}