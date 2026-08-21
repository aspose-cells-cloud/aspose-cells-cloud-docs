---
title: "Обновление метаданных"
second_title: "Документ"
linktitle: "Обновление без использования хранилища"
type: docs
url: /metadata/update/
keywords: "метаданные, Excel, Aspose.Cells Cloud, REST API, обновление, электронная таблица"
description: "REST API Aspose.Cells Cloud позволяет обновлять метаданные в файлах Excel. Поддерживает множество SDK (C#, Java, Python, Ruby, Go и др.) для беспрепятственной интеграции в различные языки программирования."
weight: 35
ArticleTitle: "Обновление метаданных – Документация Aspose.Cells Cloud API"
---

Этот REST API обновляет **метаданные** в нескольких файлах Excel.

**Необходимые условия:** Активная учётная запись Aspose Cloud, действующий JWT-токен доступа и загруженные файлы Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/metadata/update
```

### **Безопасность и аутентификация**

REST API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе токена JWT</a>.

### Параметры запроса

| Имя параметра      | Тип    | Расположение      | Описание                                        |
| ------------------ | ------ | ---------------- | ----------------------------------------------- |
| file               | file   | formData          | Файл Excel для загрузки.                        |
| DocumentProperties | object | HTTP-тело (JSON)  | Свойства документа, которые необходимо установить для файла Excel. |

**Примечания:** За один запрос можно загрузить до 10 файлов. Поддерживаемые форматы: `.xlsx`, `.xls`, `.csv`. Общий объём запроса не должен превышать 100 МБ.

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/PostMetadata) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В приведённом ниже примере показано, как выполнять вызовы к Cloud API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/update" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'xxxxx1=@xxxx1.xlsx' \
  -F 'xxxxx2=@xxxx2.xlsx' \
  -d '[{ "name": "test", "value": "test" }]'
```

Запрос требует заголовок **Authorization** с токеном Bearer JWT. Убедитесь, что токен сгенерирован с использованием учётных данных клиента Aspose Cloud.

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "xxxxx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя вам сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}

**См. также:**  
- [Получение метаданных](/metadata/get/)  
- [Удаление метаданных](/metadata/delete/)  
---