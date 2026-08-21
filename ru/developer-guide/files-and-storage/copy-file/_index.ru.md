---
title: "Aspose.Cells Cloud File Copy API — интерфейс для быстрого копирования и пакетных операций с Excel-файлами в облаке"
second_title: "Документ"
ArticleTitle: "Решение для управления Excel-файлами в облаке — подробное объяснение пакетной функции копирования Aspose.Cells Copy File API"
linktitle: "Копирование файла"
type: docs
url: /ru/copy-file/
keywords: "Aspose.Cells, CopyFile API, копирование Excel-файла, облачное хранилище, REST API"
description: "Узнайте, как использовать Aspose.Cells Cloud CopyFile API для эффективного дублирования Excel-файлов и управления ими в различных местах хранения."
weight: 100
---

API **copyFile** позволяет пользователям дублировать Excel-файл из указанного исходного пути в целевой путь, поддерживая различные варианты хранения.

## **Excel API: Копирование файла**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Безопасность и аутентификация**

Aspose.Cells Cloud API защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации на основе JWT-токена</a>.

### Параметры запроса API **copyFile**:

| Имя параметра   | Тип    | Путь / Строка запроса / HTTPBody | Описание                                                  |
| --------------- | ------ | ------------------------------- | --------------------------------------------------------- |
| srcPath         | String | Path                            | Исходный путь к копируемому файлу.                        |
| destPath        | String | Query                           | Целевой путь, по которому будет сохранен файл.            |
| srcStorageName  | String | Query                           | Имя исходного хранилища.                                  |
| destStorageName | String | Query                           | Имя целевого хранилища.                                   |
| versionId       | String | Query                           | Необязательный идентификатор версии файла для копирования. |

### **Ответ**

При успешном выполнении операция не возвращает содержимого. Типичные коды состояния HTTP:

**Коды состояния HTTP**

| Код | Значение                | Описание                                                       |
| --- | ----------------------- | -------------------------------------------------------------- |
| 200 | OK (ОК)                 | Фильтр успешно применён; ответ содержит детали операции.      |
| 400 | Bad Request (Неверный запрос) | Отсутствуют или недопустимы параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized (Неавторизованный запрос) | Недействительный или отсутствующий JWT-токен.            |
| 413 | Payload Too Large (Слишком большой полезный груз) | Загружаемый файл превышает лимит размера.              |
| 500 | Internal Server Error (Внутренняя ошибка сервера) | Непредвиденная ошибка сервера.                          |

## Как использовать API копирования файла с помощью SDK?

### Спецификация API копирования файла

[Спецификация API копирования файла](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/File/CopyFile) предоставляет публично доступный программный интерфейс для выполнения REST-взаимодействий непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. Пример ниже показывает, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Запрос" tabName12="Ответ" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/storage/file/copy/MyFolder/Source.xlsx?destPath=MyFolder/Dest.xlsx&srcStorageName=MyStorage&destStorageName=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — это самый быстрый способ разработки, так как он абстрагирует низкоуровневые детали, позволяя, например, преобразовывать данные таблицы электронной таблицы в изображение с минимальным количеством кода. Полный список SDK Aspose.Cells Cloud доступен в [репозитории на GitHub](https://github.com/aspose-cells-cloud).

Приведённые ниже примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK: