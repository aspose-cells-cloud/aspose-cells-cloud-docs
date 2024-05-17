---
title: "IconSet"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/iconset/
description: "Aspose.Cells Cloud model specification : IconSet. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, IconSet
weight: 50
---

## **iconSet**

Describe the IconSet conditional formatting rule. This conditional formatting    rule applies icons to cells according to their values. 

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| CfIcons | Container | True |  False |  | Get the from the collection  |  
| Cfvos | Container | True |  False |  | Get the CFValueObjects instance.  |  
| IsCustom | Boolean | True |  False |  | Indicates whether the icon set is custom.            Default value is false.  |  
| Reverse | Boolean | True |  False |  | Get or set the flag indicating whether to reverses the default order of the icons in this icon set.            Default value is false.  |  
| ShowValue | Boolean | True |  False |  | Get or set the flag indicating whether to show the values of the cells on which this icon set is applied.            Default value is true.  |  
| IconSetType | String | True |  False |  | Get or Set the icon set type to display.  Setting the type will auto check   if the current Cfvos's count is accord with the new type. If not accord,   old Cfvos will be cleaned and default Cfvos will be added.             |  

