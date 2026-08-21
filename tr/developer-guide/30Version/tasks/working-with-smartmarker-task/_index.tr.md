---
title: "Aspose.Cells Cloud API'de SmartMarker Görevi ile Çalışmak"
type: docs
url: /tasks/smartmarker/
aliases: [/working-with-smartmarker-task/]
keywords: "SmartMarker görevi, Aspose.Cells Cloud, REST API, Excel, elektronik tablo otomasyonu"
description: "Aspose.Cells Cloud API'nin SmartMarker görevini, cURL ve SDK örnekleriyle birlikte nasıl kullanacağınızı, istek şemasını ve hata işleme yöntemlerini öğrenin."
weight: 60
ArticleTitle: "Aspose.Cells Cloud API'de SmartMarker Görevi ile Çalışmak"
---

## REST API

**SmartMarker**, Aspose.Cells Cloud API'nin bir özelliktir ve bir Excel şablonundaki yer tutuculara XML veya JSON kaynaklarından gelen verileri birleştirerek tamamen doldurulmuş bir çalışma kitabını oluşturur. Genellikle rapor oluşturma, posta birleştirme ve veri odaklı elektronik tablo oluşturma işlemleri için kullanılır.

**Ön Gereksinimler**

- Aspose.Cells Cloud API sürümü 3.0 veya üzeri.  
- Geçerli bir OAuth2/JWT erişim belirteci (`Authorization: Bearer <token>` başlığıyla iletilir).  
- Kaynak dosyaların (şablon çalışma kitabının ve veri dosyasının) Aspose Cloud deposuna yüklenmiş olması veya desteklenen bir dosya sistemi türü üzerinden erişilebilir olması gerekir.  
- HTTPS uç noktası (tüm istekler TLS kullanmalıdır).

| **API** | **Tür** | **Açıklama** | **Kaynak Bağlantısı** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Görevi Çalıştır | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Task/PostRunTask), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, bir SmartMarker görevini nasıl çalıştıracağınızı ve ardından sonuç çalışma kitabını nasıl kaydedeceğinizi göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <your_access_token>" \
     -d '{
  "TaskData": {
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "SmartMarker",
          "SmartMarkerTaskParameter": {
            "SourceWorkbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "Designer.xlsx"
            },
            "DestinationWorkbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "Temp.xlsx"
            },
            "xmlFile": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "DataSet.xml"
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "SaveResult",
          "SaveResultTaskParameter": {
            "ResultSource": "InMemoryFiles",
            "ResultDestination": {
              "DestinationType": "OutputStream",
              "InputFile": "Temp.xlsx",
              "OutputFile": "Output.xlsx"
            }
          }
        }
      }
    ]
  }
}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "FileLink": "https://api.aspose.cloud/v3.0/storage/file/Output.xlsx",
    "FileSize": 254321,
    "FileName": "Output.xlsx"
  }
}
```

{{< /tab >}}

{{< /tabs >}}

### İstek şeması (alıntı)

| Eleman | Tür | Zorunlu | Açıklama |
| ------- | ---- | -------- | ----------- |
| `TaskData` | nesne | Evet | Bir veya daha fazla `TaskDescription` nesnesini içeren kök eleman. |
| `Tasks` | nesneler dizisi | Evet | Sırayla çalıştırılacak görevler koleksiyonu. |
| `TaskDescription.TaskType` | dize | Evet | Görevin türü (`SmartMarker`, `SaveResult`, vb.). |
| `SmartMarkerTaskParameter.SourceWorkbook` | nesne | Evet | Şablon çalışma kitabının konumunu belirtir. |
| `SmartMarkerTaskParameter.DestinationWorkbook` | nesne | Evet | Ara çalışma kitabının nerede saklanacağını belirtir. |
| `SmartMarkerTaskParameter.xmlFile` | nesne | Evet | SmartMarker tarafından kullanılan veri kaynağı (XML/JSON). |
| `SaveResultTaskParameter.ResultDestination` | nesne | Evet | Son çalışma kitabının nasıl döndürüleceğini tanımlar (örneğin, `OutputStream`). |

### Hata işleme

API aşağıdaki HTTP durum kodlarını döndürebilir:

- **400 Bad Request** – Bozuk istek yükü veya eksik zorunlu alanlar.  
- **401 Unauthorized** – Geçersiz veya eksik kimlik doğrulama belirteci.  
- **404 Not Found** – Belirtilen kaynak dosyalardan biri bulunamadı.  
- **500 Internal Server Error** – Beklenmedik bir sunucu tarafı hatası oluştu.

Yanıt gövdesinde, bir `Code` ve açıklayıcı bir `Message` içeren bir `Error` nesnesini kontrol edin.

Geliştirme sürecini hızlandırmanın en iyi yolu SDK kullanmaktır. SDK, düşük seviye ayrıntıları ele alır ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud){:rel="noopener noreferrer"} göz atın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="1" tabID="4" tabName1="C#" >}}

{{< tab tabNum="1" >}}
```csharp
var xml = @"<TaskData>
    <Tasks>
        <TaskDescription>
            <TaskType>SmartMarker</TaskType>
            <SmartMarkerTaskParameter>
                <SourceWorkbook>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>Designer.xlsx</FilePath>
                </SourceWorkbook>
                <DestinationWorkbook>
                    <FileSourceType>InMemoryFiles</FileSourceType>
                    <FilePath>Temp.xlsx</FilePath>
                </DestinationWorkbook>
                <xmlFile>
                    <FileSourceType>CloudFileSystem</FileSourceType>
                    <FilePath>DataSet.xml</FilePath>
                </xmlFile>
            </SmartMarkerTaskParameter>
        </TaskDescription>
        <TaskDescription>
            <TaskType>SaveResult</TaskType>
            <SaveResultTaskParameter>
                <ResultSource>InMemoryFiles</ResultSource>
                <ResultDestination>
                    <DestinationType>OutputStream</DestinationType>
                    <InputFile>Temp.xlsx</InputFile>
                    <OutputFile>Output.xlsx</OutputFile>
                </ResultDestination>
            </SaveResultTaskParameter>
        </TaskDescription>
    </Tasks>
</TaskData>";

ServiceHelper helper = new ServiceHelper(sid, key);
using (HttpWebResponse response = helper.CallPost(
       "https://api.aspose.cloud/v3.0/cells/task/runtask",
       xml,
       "application/xml"))
{
    if (response.StatusCode == HttpStatusCode.OK)
    {
        Console.WriteLine("OK");
        using (Stream st = response.GetResponseStream())
        using (FileStream fs = new FileStream("Output.xlsx", FileMode.OpenOrCreate))
        {
            st.CopyTo(fs);
        }
    }
}
```
{{< /tab >}}

{{< /tabs >}}