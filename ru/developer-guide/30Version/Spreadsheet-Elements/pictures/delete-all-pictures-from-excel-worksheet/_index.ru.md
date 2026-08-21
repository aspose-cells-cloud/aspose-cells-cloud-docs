---
title: "Удаление всех изображений из рабочего листа Excel"
second_title: "Документ"
linktitle: "Очистка"
type: docs
url: /ru/pictures/clear/
aliases: [  /ru/delete-all-pictures-from-excel-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, удаление всех изображений, рабочий лист, REST API, очистка изображений"
description: "Узнайте, как удалить все изображения из рабочего листа Excel с помощью Aspose.Cells Cloud REST API, используя примеры cURL и SDK."
weight: 60
ArticleTitle: "Как удалить все изображения из рабочего листа Excel с помощью Aspose.Cells Cloud"
---

Этот REST API удаляет **все** изображения из рабочего листа.

**Необходимые условия**  
- Активная учетная запись Aspose.Cells Cloud с действительным токеном OAuth 2.0.  
- Требуется версия API 3.0 или выше; более ранние версии устарели.  
- Целевой файл Excel должен храниться в поддерживаемом хранилище (по умолчанию или пользовательском).

**Совместимость версий**  
Конечная точка следует спецификации Cells Cloud API версии 3.0. Убедитесь, что используемые клиентские библиотеки и URL-адреса запросов указывают на `api.aspose.cloud/v3.0`.

## API DeleteWorksheetPictures

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе JWT-токена</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Расположение | Описание                                         |
| ------------- | ----- | ------------ | ------------------------------------------------ |
| name          | string | Path         | Имя файла Excel.                                 |
| sheetName     | string | Path         | Имя рабочего листа, содержащего изображения.    |
| folder        | string | Query        | Папка, в которой хранится файл.                  |
| storageName   | string | Query        | Имя службы хранилища.                            |

### Ответы об ошибках

| Код HTTP | Описание                                                                 |
| -------- | ------------------------------------------------------------------------ |
| 401      | Неавторизован — отсутствует или недействителен токен.                   |
| 404      | Не найдено — указанный файл, рабочий лист или индекс разрыва страницы не существует. |
| 400      | Неверный запрос — некорректный синтаксис запроса или недопустимые параметры. |
| 500      | Внутренняя ошибка сервера — возникло непредвиденное условие.             |

[Спецификация OpenAPI](https://apireference.aspose.cloud/cells/#/Pictures/DeleteWorksheetPictures) определяет публично доступное программное интерфейсное определение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для легкого доступа к веб-службам Aspose.Cells. В следующем примере показано, как вызвать API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/pictures" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Семейство облачных SDK

Использование SDK — это самый быстрый способ разработки. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на бизнес-логике. Полный список SDK Aspose.Cells Cloud доступен в [репозитории GitHub](https://github.com/aspose-cells-cloud).

Следующие примеры кода демонстрируют, как вызывать веб-службы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPictures.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPictures.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPictures.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPictures.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPictures.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPictures.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPictures.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPictures.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Примечания:** Операция DELETE не поддерживает постраничную выборку и подчиняется стандартным ограничениям скорости API Aspose.Cells Cloud (по умолчанию 100 запросов в минуту). Скорректируйте логику клиента соответственно.

**См. также**:  
- [/pictures/delete/](../delete/) – Удаление конкретного изображения из рабочего листа.  
- [/pictures/add/](../add/) – Добавление изображения в рабочий лист.  
---