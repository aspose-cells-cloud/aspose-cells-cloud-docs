---
title: "Удаление метаданных из файлов Excel"
second_title: "Документ"
linktitle: "Удаление без использования хранилища"
type: docs
url: /metadata/delete/
keywords: "Aspose.Cells, удаление метаданных, Excel API, свойства рабочей книги"
description: "Удаление метаданных рабочей книги (автор, заголовок, пользовательские данные) с помощью API Aspose.Cells Cloud. Включает конечную точку, аутентификацию, параметры, примеры cURL и SDK."
weight: 55
ArticleTitle: "Удаление метаданных из файлов Excel – документация Aspose.Cells Cloud"
---

**Обзор**  
Операция удаления метаданных безвозвратно удаляет все свойства рабочей книги (стандартные и пользовательские) из загруженных файлов Excel и возвращает обработанные файлы в ответе.

**Необходимые условия**  
- Действующий JWT-токен Aspose.Cells Cloud (получаемый в рамках потока аутентификации OAuth 2.0).  
- Версия API **v3.0** (конечная точка, используемая в данном примере).  
- Для использования SDK установите соответствующий SDK Aspose.Cells Cloud для вашего языка программирования (например, через NuGet, Maven, npm, pip, CPAN или Go modules).

Этот REST API удаляет **метаданные** из одного или нескольких файлов Excel. Он удаляет свойства рабочей книги, такие как автор, заголовок и пользовательские данные, и возвращает очищенные файлы.

## API

```http
POST https://api.aspose.cloud/v3.0/cells/metadata/delete
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                                |
|---------------|-------|-------------|---------------------------------------------------------|
| file          | файл  | formData    | Файл Excel для загрузки с целью удаления **метаданных** |
| type          | строка| query       | Тип операции; установите значение **all**, чтобы удалить все **метаданные** |

<a href="https://apireference.aspose.cloud/cells/#/DeleteMetadata" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Для удобного доступа к веб-сервисам Aspose.Cells вы можете использовать утилиту командной строки cURL. В следующем примере показано, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/metadata/delete?type=all" \
  -X POST \
  -H "Authorization: Bearer <jwt token>" \
  -F "file=@file1.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Files": [
    {
      "Filename": "file1.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

**Ответы об ошибках** могут включать:

- **400 Bad Request** — отсутствует файл или указано недопустимое значение `type`.
- **401 Unauthorized** — недействительный или отсутствующий JWT-токен.
- **500 Internal Server Error** — ошибка обработки на стороне сервера.

API возвращает JSON-объект, содержащий поле `Error` с деталями ошибки для каждого случая.

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Метаданные удалены, файл возвращён |
| 400 | Bad Request | Отсутствует файл или недопустимое значение `type` |
| 401 | Unauthorized | Недействительный или отсутствующий JWT |
| 500 | Internal Server Error | Сбой обработки на стороне сервера |

## Семейство облачных SDK

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Ознакомьтесь с полным списком SDK Aspose.Cells Cloud в <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозитории GitHub</a>.

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteMetadata.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteMetadata.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteMetadata.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteMetadata.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteMetadata.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteMetadata.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteMetadata.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteMetadata.go" >}}

{{< /tab >}}

{{< /tabs >}}