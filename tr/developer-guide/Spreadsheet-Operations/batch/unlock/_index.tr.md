---
title: Toplu Kilit Açma
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/batch/unlock
keywords: Batch unlock of multiple Excel files
description: Aspose.Cells Cloud API, birden fazla excel dosyasının toplu kilidini açmayı destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 100
kwords: Excel, Office Bulut, REST API, E-Tablo, PDF, CSV, Json, Markdown, Toplu Kilit Açma
---
Bu REST API, `batch unlock`'e uygun dosyaları gösterir.

## RSETAPI

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/unlock
 
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| Toplu Kilit İsteği|| vücut||

**BatchLockRequest Özellikleri**

İsim | Tür | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 KaynakKlasörü | dize | | [isteğe bağlı]EşleşmeKoşulu | EşleşmeKoşuluİsteği | | [isteğe bağlı]Parola | dize | | [isteğe bağlı]ÇıkışKlasörü | dize | | [isteğe bağlı]**MatchConditionRequest Özellikleri**

İsim | Tür | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 RegexPattern | dize | | [isteğe bağlı]FullMatchConditions | dize[]| | [isteğe bağlı][OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchUnlock) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/unlock" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Password\":\"123456\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve kilit açma görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostBatchUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostBatchUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostBatchUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostBatchUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostBatchUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostBatchUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostBatchUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostBatchUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}
