---
title: "Aspose.Cells Cloud Folder Copy API — Быстрое копирование папок в облаке"
second_title: "Документ"
ArticleTitle: "Решение для управления Excel-файлами в облаке — Подробное описание пакетной функции копирования папок API Aspose.Cells Copy Folder"
linktype: "docs"
url: /copy-folder/
keywords: "Копирование папки, Aspose.Cells Cloud, REST API, облачное хранилище, управление электронными таблицами"
description: "Узнайте, как копировать папки в облачном хранилище Aspose.Cells Cloud с помощью одного REST-вызова. Включает endpoint, параметры, примеры запросов, коды ошибок и примеры SDK."
weight: 100
---

API **CopyFolder** дублирует существующую папку в облачном хранилище Aspose.Cells Cloud. Это полезно для создания резервных копий, реорганизации данных или подготовки иерархии папок для дальнейшей обработки без ручного перемещения файлов.

## **Excel API: Копирование папки**

### Web API

```
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/{srcPath}
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры, принимаемые API CopyFolder

| Имя параметра     | Обязательный | Тип    | Расположение (Путь/Запрос) | Описание                                                       |
| ----------------- | ------------ | ------ | -------------------------- | -------------------------------------------------------------- |
| `srcPath`         | Да           | String | Path                       | Путь к исходной папке, которую нужно скопировать.             |
| `destPath`        | Да           | String | Query                      | Путь, по которому будет создана новая папка.                   |
| `srcStorageName`  | Нет          | String | Query                      | Имя хранилища, в котором находится исходная папка.             |
| `destStorageName` | Нет          | String | Query                      | Имя целевого хранилища, в которое следует скопировать папку.   |

### Пример ответа

Успешный вызов возвращает **HTTP 200** с пустым JSON-телом:

```json
{}
```

**Пример запроса с помощью cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy" \
     -H "Authorization: Bearer {access_token}"
```

**Коды HTTP-статуса**

| Код  | Значение                | Описание                                                   |
| ---- | ----------------------- | ---------------------------------------------------------- |
| 200  | OK (Успех)             | Фильтр применён успешно; ответ содержит детали операции.  |
| 400  | Bad Request (Ошибка)   | Отсутствуют или неверны параметры (например, неподдерживаемый тип файла). |
| 401  | Unauthorized (Неавторизовано) | Неверный или отсутствующий JWT-токен.                |
| 413  | Payload Too Large (Слишком большой payload) | Загруженный файл превышает допустимый размер. |
| 500  | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера. |

## Спецификация OpenAPI

[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/FolderController/CopyFolder) определяет общедоступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Следующий пример демонстрирует, как выполнять вызовы в облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/folder/copy/MyFolder?destPath=MyFolderCopy
Authorization: Bearer {access_token}
Content-Type: application/json
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя обработку низкоуровневых деталей и позволяет сосредоточиться на задачах проекта. Ознакомьтесь с [репозиторием на GitHub](https://github.com/aspose-cells-cloud), чтобы увидеть полный список SDK для Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как выполнять вызовы веб-сервисов Aspose.Cells с использованием различных SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFolder.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFolder.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFolder.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFolder.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFolder.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFolder.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFolder.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFolder.go" >}}
{{</tab>}}
{{< /tabs >}}