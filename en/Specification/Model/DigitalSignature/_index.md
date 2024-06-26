---
title: "DigitalSignature"
second_title: "Aspose.Cells Cloud Document"
type: docs
url: /specification/model/digitalsignature/
description: "Aspose.Cells Cloud model specification : DigitalSignature. Effortlessly handle Excel and other spreadsheet documents with features like opening, generating, editing, splitting, merging, comparing, and converting."
kwords: Excel, Office, Spreadsheet, Cloud REST API, DigitalSignature
weight: 50
---

## **digitalSignature**

Signature in file.             

| Property Name | Property Type | Nullable |  ReadOnly | DefaultValue | Description | 
| :- | :- | :- |:- |  :- | :- |
| Comments | String | True |  False |  | The purpose to signature. |  
| SignTime | String | True |  False |  | The time when the document was signed. |  
| Id | String | True |  False |  | Specifies a GUID which can be cross-referenced with the GUID of the signature line stored in the document content. Default value is Empty (all zeroes) Guid. |  
| Password | String | True |  False |  | Specifies the text of actual signature in the digital signature. Default value is Empty.             |  
| Image | Array<Byte> | True |  False |  | Specifies an image for the digital signature. Default value is null. |  
| ProviderId | String | True |  False |  | Specifies the class ID of the signature provider. Default value is Empty (all zeroes) Guid.             |  
| IsValid | Boolean | True |  False |  | If this digital signature is valid and the document has not been tampered with, this value will be true. |  
| XAdESType | String | True |  False |  | XAdES type. Default value is None(XAdES is off). |  

