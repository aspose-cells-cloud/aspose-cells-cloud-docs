---
title: "Task API'de Destek İsteği Dosyası"
second_title: "Belge"
type: docs
url: /tr/tasks/support-request-file/
aliases: [  /tr/support-request-file-in-task-api/ ]
keywords: "Aspose.Cells, REST API, Excel, Bulut"
description: "Aspose.Cells Cloud API, Excel çalışma kitapları için istek dosyalarının görev tabanlı işlenmesini sağlar."
weight: 10
ArticleTitle: "Aspose.Cells Task API'de Destek İsteği Dosyası"
---

## REST API

| **API** | **Tür** | **Açıklama** | **Kaynak Bağlantısı** |
| :- | :- | :- | :- |
| /cells/task/runtask | POST | Görev Çalıştır | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Task/PostRunTask), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**İstek Parametreleri**

| Parametre | Tür | Zorunlu | Açıklama |
|-----------|------|----------|-------------|
| TaskDescription | object | Evet | Tek bir görev tanımının container’ı. |
| TaskType | string | Evet | Görev türü, örneğin `ImportData` veya `SaveResult`. |
| Workbook.FileSourceType | string | Evet | Çalışma kitapı dosyasının kaynağı (`CloudFileSystem`, `InMemoryFiles`). |
| Workbook.FilePath | string | Evet | Seçilen kaynaktaki çalışma kitabı dosyasının yolu. |
| ImportBatchDataOption.DestinationWorksheet | string | Evet | İçe aktarılan veriler için hedef çalışma sayfası adı. |
| ImportBatchDataOption.IsInsert | boolean | Evet | Satırların ekleneceği (`true`) mi yoksa üzerine yazılacağı (`false`) mı. |
| ImportBatchDataOption.Source.FileSourceType | string | Evet | İsteği dosyasının kaynağı (`RequestFiles`). |
| ImportBatchDataOption.Source.FilePath | string | Evet | Toplu verileri içeren istek dosyasının yolu. |
| SaveResultTaskParameter.ResultSource | string | Evet | Sonuç dosyasının kaynağı (`InMemoryFiles`). |
| SaveResultTaskParameter.ResultDestination.DestinationType | string | Evet | Sonuç için hedef türü (`CloudFileSystem`). |
| SaveResultTaskParameter.ResultDestination.InputFile | string | Evet | Giriş çalışma kitabı dosyası adı. |
| SaveResultTaskParameter.ResultDestination.OutputFile | string | Evet | İstenen çıktı dosyası adı. |

**Yanıt**

| Alan | Tür | Açıklama |
|------|-----|----------|
| Code | integer | HTTP durum kodu (örneğin, başarı için 200). |
| Status | string | İşlem durumu (`OK` veya hata mesajı). |
| Result | object | Oluşturulan dosyalar dahil, görev yürütmesinin detayları. |

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -H "accept: application/json" \
  -H "Content-Type: application/json" \
  -H "x-aspose-client: Containerize.Swagger" \
  -d '{
    "Tasks": [
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "CloudFileSystem",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet1",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml.txt"
              }
            }
          }
        }
      },
      {
        "TaskDescription": {
          "TaskType": "ImportData",
          "ImportDataTaskParameter": {
            "Workbook": {
              "FileSourceType": "InMemoryFiles",
              "FilePath": "TaskBook.xlsx"
            },
            "ImportBatchDataOption": {
              "DestinationWorksheet": "Sheet2",
              "IsInsert": true,
              "Source": {
                "FileSourceType": "RequestFiles",
                "FilePath": "Batch_data_xml_2.txt"
              }
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
              "DestinationType": "CloudFileSystem",
              "InputFile": "TaskBook.xlsx",
              "OutputFile": "ImpDataBook.xlsx"
            }
          }
        }
      }
    ]
  }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "Result": {
    "GeneratedFiles": [
      {
        "FilePath": "ImpDataBook.xlsx",
        "FileUrl": "https://api.aspose.cloud/v3.0/cells/storage/file/ImpDataBook.xlsx"
      }
    ]
  }
}
```

{{< /tab >}}

{{< /tabs >}}

İlgili görevler hakkında daha fazla bilgi için [ImportData görevi](/tr/cells/tasks/importdata/) ve [SaveResult görevi](/tr/cells/tasks/save-result/) sayfalarına bakın.

## Bulut SDK Geliştirme Seti Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="1" tabID="4" tabName1="PHP" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostTaskDataMultipart-.php" >}}

{{< /tab >}}

{{< /tabs >}}
---