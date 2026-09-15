---
title: "Working with Excel AutoFilter"
second_title: "Document"
linktitle: "AutoFilter"
type: docs
url: /autofilter/
aliases: [/working-with-autofilter/]
keywords: "AutoFilter, Aspose.Cells Cloud, Excel filter, color filter, date filter, dynamic filter, number filter, text filter, blank filter, non-blank filter, custom filter"
description: "Learn to add, edit, and delete Excel AutoFilters (color, date, dynamic, number, text, blank, non-blank) using Aspose.Cells Cloud REST APIs. Includes code samples in C#, Python, Java, Node.js, and more."
weight: 100
ArticleTitle: "Working with Excel AutoFilter – Aspose.Cells Cloud Documentation"
date: 2024-03-15
last_modified: 2024-06-10
tags:
  - autofilter
  - excel
  - filtering
  - aspose.cells
categories:
  - cloud
  - cells
---

AutoFilter is the quickest way to display only the items you need from a worksheet. The AutoFilter feature lets users filter a list based on specified criteria—by text, numbers, or dates.

**Different Types of Filters**

Aspose.Cells Cloud provides multiple APIs to apply various filter types, such as Color Filter, Date Filter, Number Filter, Text Filter, Blank Filter, and Non-Blank Filter.

<!-- Use Hugo shortcode (if theme supports it) -->
<table class="table table-striped">
  <tr>
    <td class="col-md-2"><strong>Fill Color</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud offers <a href="/cells/autofilter/add-color-filter/">the Add Fill Color Filter API</a> to filter data based on the fill-color property of cells.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Date</strong></td>
    <td class="col-md-10">
      <p>Various date filters can be applied, such as filtering rows with dates in January 2018. Use <a href="/cells/autofilter/add-date-filter/">the Add Date Filter API</a> to add a date filter.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Dynamic Date</strong></td>
    <td class="col-md-10">
      <p>Dynamic date filters allow you to filter cells that fall in a specific month regardless of the year (e.g., all January dates). See <a href="/cells/autofilter/add-dynamic-filter/">the Dynamic Filter API</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Number</strong></td>
    <td class="col-md-10">
      <p>The <a href="/cells/autofilter/add-filter/">Custom Filters API</a> enables filtering cells whose numeric values fall within a given range.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Text</strong></td>
    <td class="col-md-10">
      <p>If a column contains text, you can select cells containing a specific string using <a href="/cells/autofilter/add-filter/">the Add Filter API</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Blanks</strong></td>
    <td class="col-md-10">
      <p>To retrieve rows where a column is blank, use <a href="/cells/autofilter/match-all-blank/">the Match All Blank Cells API</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Non-Blank</strong></td>
    <td class="col-md-10">
      <p>To filter rows where a column contains any non-blank value, use <a href="/cells/autofilter/match-all-non-blank/">the Match All Non-Blank Cells API</a>.</p>
    </td>
  </tr>
  <tr>
    <td class="col-md-2"><strong>Custom Filter</strong></td>
    <td class="col-md-10">
      <p>Aspose.Cells Cloud provides <a href="/cells/autofilter/add-custom-filter/">the Custom Filters API</a> for advanced scenarios, such as filtering rows that contain a specific substring or that start/end with a particular string.</p>
    </td>
  </tr>
</table>

> _Note:_ The `add-filter` endpoint supports multiple filter types (text, number, date, custom); use query parameters to specify the filter criteria.

**AutoFilter Operations**

- [How to add a color filter in an Excel worksheet](/cells/autofilter/add-color-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-color-filter/`
- [How to add a custom filter in an Excel worksheet](/cells/autofilter/add-custom-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-custom-filter/`
- [How to add a date filter in an Excel worksheet](/cells/autofilter/add-date-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-date-filter/`
- [How to add a dynamic filter in an Excel worksheet](/cells/autofilter/add-dynamic-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-dynamic-filter/`
- [How to add a custom filter (text/number/date) in an Excel worksheet](/cells/autofilter/add-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-filter/`
- [How to add an icon filter in an Excel worksheet](/cells/autofilter/add-icon-filter/) – **Method:** POST, **Endpoint:** `/cells/autofilter/add-icon-filter/`
- [How to delete a date filter in an Excel worksheet](/cells/autofilter/delete-a-date-filter/) – **Method:** DELETE, **Endpoint:** `/cells/autofilter/delete-a-date-filter/`
- [How to delete a filter in an Excel worksheet](/cells/autofilter/delete/) – **Method:** DELETE, **Endpoint:** `/cells/autofilter/delete/`
- [How to get an AutoFilter description from an Excel worksheet](/cells/autofilter/get/) – **Method:** GET, **Endpoint:** `/cells/autofilter/get/`
- [How to match all blank cells in an Excel worksheet](/cells/autofilter/match-all-blank/) – **Method:** POST, **Endpoint:** `/cells/autofilter/match-all-blank/`
- [How to match all non-blank cells in an Excel worksheet](/cells/autofilter/match-all-non-blank/) – **Method:** POST, **Endpoint:** `/cells/autofilter/match-all-non-blank/`
- [How to refresh an AutoFilter in an Excel worksheet](/cells/autofilter/refresh/) – **Method:** POST, **Endpoint:** `/cells/autofilter/refresh/`

> _Note:_ Icon filters are now managed via Conditional Formatting APIs. For details, see the [Conditional Formatting Guide](/conditional-formatting/).

**Prerequisites**

Ensure you have:

1. A valid Aspose.Cells Cloud API key
2. A sample Excel file uploaded to cloud storage

**Code Sample Preview**

The following Python example demonstrates how to apply a text filter to a column:

```python
import asposecellscloud
from asposecellscloud.api import CellsApi
from asposecellscloud.models import Filter

api = CellsApi(client_id='xxxx', client_secret='xxxx')
response = api.cells_autofilter_post_worksheet_autofilter(
    name='Sample.xlsx',
    sheet_name='Sheet1',
    field_index=0,
    filter_type='Text',
    criteria='=John*',
    match_blanks=False,
    case_sensitive=False
)
```

> Code samples in C#, Java, Node.js, PHP, and other languages are available in each operation’s dedicated documentation page.
