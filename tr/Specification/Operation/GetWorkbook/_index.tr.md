---
title: GetWorkboo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/specification/operation/getworkbook/
description: Çeşitli formatlardaki çalışma kitaplarını alın
weight: 50
---
{{< blocks/products/cells/docs-title titlemsg="GetWorkbook" >}}
{{< blocks/products/cells/docs-title titlemsg="Retrieve workbooks in various formats." >}}

{{< blocks/products/cells/docs-Parameter parametertitle="REST API" columns="API,HttpMethod,Açıklama,API referans" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="/cells/{name},GET,Çeşitli formatlardaki çalışma kitaplarını alın.,<a href=\'https://apireference.aspose.cloud/cells/#/Conversion/GetWorkbook\'>GetWorkbook</a>" >}}
{{< /blocks/products/cells/docs-Parameter >}}


{{< blocks/products/cells/docs-Parameter parametertitle="Path Parameter" columns="Parametre Adı,Tip,Açıklama" >}}
     {{< blocks/products/cells/docs-Parameter-content columns="name,string,Dosya adı." >}} 
{{< /blocks/products/cells/docs-Parameter >}}
{{< blocks/products/cells/docs-Parameter parametertitle="Query Parameter" columns="Parametre Adı,Tip,Açıklama" >}}
    {{< blocks/products/cells/docs-Parameter-content columns="format,dize,Dönüştürme formatı(CSV/XLS/HTML/MHTML/ODS/PDF/XML/TXT/TIFF/XLSB/XLSM/XLSX/XLTM/XLTX/XPS/PNG/JPG/JPEG/GIF/EMF/076173 481/ MD[İşaretleme]/Numaralar)." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="şifre,string,Excel dosyasını açmak için gereken şifre." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="isAutoFit,boolean,Çalışma kitabı satırlarının otomatik olarak sığdırılıp sığdırılmayacağını belirtir." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="onlySaveTable,boolean,Yalnızca tablo verilerinin kaydedilip kaydedilmeyeceğini belirtir.Yalnızca excel için pdf kullanın." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="klasör,dize,Dosyanın bulunduğu klasör." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outPath,string,Path sonucu kaydetmek için. Tek bir dosya ise, \"outPath\" hem dosya adını hem de uzantıyı kapsamalıdır. Birden fazla dosya olması durumunda, \"outPath\" yalnızca klasörü içermelidir." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="depolamaAdı,dize,Dosyanın bulunduğu depolama adı." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="outStorageName,string,Çıktı dosyasının bulunduğu depolama adı." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="checkExcelRestriction,boolean,Kullanıcı hücrelerle ilgili nesneleri değiştirdiğinde excel dosyasının kısıtlamasının kontrol edilip edilmeyeceği." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="bölge,dize,Çalışma kitabının bölgesel ayarları." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageWideFitOnPerSheet,boolean,Sayfanın çalışma sayfasına sığması." >}} 
    {{< blocks/products/cells/docs-Parameter-content columns="pageTallFitOnPerSheet,boolean,Sayfanın çalışma sayfasına sığacak kadar uzun olması." >}} 
{{< /blocks/products/cells/docs-Parameter >}}

{{< blocks/products/cells/docs-title titlemsg="The <a href=\'https://apireference.aspose.cloud/cells/#/ConversionController/GetWorkbook\'>OpenAPI Specification</a> defines a publicly accessible programming interface and lets you carry out REST interactions directly from a web browser. " >}}
 
{{< blocks/products/cells/docs-title titlemsg="You can use <b>cURL</b> command-line tool to access Aspose.Cells web services easily. The following example shows how to make calls to Cloud API with cURL." >}}

{{< tabs tabTotal="1" tabID="1" tabName1="Request" >}}

{{< tab tabNum="1" >}}

```bash

curl -v "https://api.aspose.cloud/v3.0/cells/cells/Book1.xlsx?format=csv&folder=TestData/In"
    -X GET 
    -H "Authorization: Bearer \<jwt token> " \

```

{{< /tab >}}

{{< /tabs >}}

{{< blocks/products/cells/docs-title-h2 titlemsg="Cloud SDK Family" >}}

{{< blocks/products/cells/docs-title titlemsg="Using an SDK is the best way to speed up the development. An SDK takes care of low-level details and lets you focus on your project tasks. Please check out the <a href=\'https://github.com/aspose-cells-cloud\'>GitHub repository</a> for a complete list of Aspose.Cells Cloud SDKs. " >}}

{{< blocks/products/cells/docs-title titlemsg="The following code examples demonstrate how to make calls to Aspose.Cells web services using various SDKs:" >}}

{{< tabs tabTotal="3" tabID="11" tabName11="Go" tabName12="Java" tabName13="Net" tabName14="Node" tabName15="Perl" tabName16="PHP" tabName17="Python" tabName18="Ruby" >}}

{{< tab tabNum="11" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example_GetWorkbook.go" >}}
{{< /tab >}}

{{< tab tabNum="12" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}
{{< /tab >}}

{{< tab tabNum="13" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}
{{< /tab >}}

{{< tab tabNum="14" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}
{{< /tab >}}

{{< tab tabNum="15" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}
{{< /tab >}}

{{< tab tabNum="16" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}
{{< /tab >}}

{{< tab tabNum="17" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}
{{< /tab >}}

{{< tab tabNum="18" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}
{{< /tab >}}

{{< /tabs >}}
