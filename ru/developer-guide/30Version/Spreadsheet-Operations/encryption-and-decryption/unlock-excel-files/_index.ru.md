---
title: "Разблокировка файлов Excel"
second: "Документ"
linktitle: "Разблокировка файлов Excel"
type: docs
url: /ru/unlock-excel-files/
aliases: [  /ru/unlock/without-storage/ , /ru/unlock/ , /ru/unlock/without-using-storage/ ]
keywords: "Разблокировка Excel, Aspose.Cells Cloud, REST API, разблокировка Excel, защищённая паролем книга, SDK, C#, Java, Python, Node.js, Go, PHP, Ruby, Swift"
description: "Aspose.Cells Cloud REST API предоставляет конечную точку для разблокировки файлов Excel, защищённых паролем. SDK доступны для множества языков программирования, включая Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby и Swift."
ArticleTitle: "Разблокировка файлов Excel с использованием Aspose.Cells Cloud REST API"
weight: 70
---

Этот REST API позволяет разблокировать файлы Excel.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/unlock
```

### Безопасность и аутентификация

API Aspose.Cells Cloud защищены и требуют [аутентификации на основе JWT-токена](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

### Параметры запроса

| Имя параметра | Тип   | Местоположение           | Описание                                     |
|--------------|-------|-------------------------|---------------------------------------------|
| file         | файл  | formData (тело HTTP-запроса) | Загружаемый файл                             |
| password     | строка | строка запроса          | Пароль для разблокировки файла (если защищён) |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                     |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | OK (ОК)                     | Фильтр успешно применён; ответ содержит детали операции.    |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизовано) | Недействительный или отсутствующий JWT-токен.              |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загруженный файл превышает лимит размера.                   |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                              |

## Как использовать API PostUnlock с SDK

### Спецификация API PostUnlock

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/LightCells/PostUnlock) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для лёгкого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/unlock?password=123456" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

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

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах проекта. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

**Примечания**  
- API может разблокировать несколько файлов Excel за один запрос; каждый файл возвращается в массиве `Files` ответа.  
- Убедитесь, что версия SDK соответствует версии API (`v3.0`), чтобы избежать проблем совместимости.

Примеры кода ниже демонстрируют, как выполнять вызовы в веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnlock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnlock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnlock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnlock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnlock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnlock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnlock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnlock.go" >}}

{{< /tab >}}

{{< /tabs >}}