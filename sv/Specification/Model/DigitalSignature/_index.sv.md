---
title: Digital Signatur
second_title: Aspose.Cells Cloud Documen
type: docs
url: /sv/specification/model/digitalsignature/
description: "Aspose.Cells Molnmodellspecifikation: DigitalSignature. Hantera enkelt Excel och andra kalkylarksdokument med funktioner som att öppna, generera, redigera, dela, slå samman, jämföra och konvertera"
kwords: Excel, Office, Kalkylblad, Cloud REST API, Digital Signatur
weight: 50
---
## **digital signatur**

 Signatur i fil.

| Egendomsnamn| Egenskapstyp| Nullbar| Endast läs| Standardvärde| Beskrivning|
|:- |:- |:- |:- |:- |:- |
| Kommentarer| Sträng| Sann| Falsk|| Syftet med att skriva under.|
| SignTime| Sträng| Sann| Falsk|| Tidpunkten då dokumentet undertecknades.|
| Id| Sträng| Sann| Falsk|| Anger en GUID som kan korsreferens med GUID för signaturraden som lagras i dokumentinnehållet. Standardvärdet är Tom (alla nollor) Guid.|
| Lösenord| Sträng| Sann| Falsk|| Anger texten för den faktiska signaturen i den digitala signaturen. Standardvärdet är Empty.|
| Bild|Array<Byte> | Sann| Falsk|| Anger en bild för den digitala signaturen. Standardvärdet är null.|
| ProviderId| Sträng| Sann| Falsk|| Anger klass-ID för signaturleverantören. Standardvärdet är Tom (alla nollor) Guid.|
| Är giltig| Boolean| Sann| Falsk|| Om denna digitala signatur är giltig och dokumentet inte har manipulerats kommer detta värde att vara sant.|
| XAdESType| Sträng| Sann| Falsk|| XAdES typ. Standardvärdet är None (XAdES är avstängt).|

