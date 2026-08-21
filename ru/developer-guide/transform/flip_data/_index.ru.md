---
title: "FlipData"
ArticleTitle: "FlipData – Aspose.Cells Cloud"
second_title: "Документ"
linktype: "docs"
url: /cells/flip
aliases: []
keywords: "FlipData, Преобразование, Aspose.Cells"
description: "Транспонирует заданный диапазон данных в файле электронной таблицы."
weight: 100
---

## FlipData облачных веб-сервисов Aspose.Cells

Этот API меняет ориентацию заданной матрицы данных. Например, диапазон 3×2 (3 строки, 2 столбца) будет преобразован в диапазон 2×3 (2 строки, 3 столбца) в выходных данных. Обычно используется для переструктуризации данных в соответствии с требованиями к входным данным различных диаграмм, отчётов или моделей данных.

### Конечная точка веб-API

```http
PUT https://api.aspose.cloud/v4.0/cells/flip
```

### **Безопасность и аутентификация**

API облачных сервисов Aspose.Cells защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификацию на основе JWT-токена</a>.

### Параметры запроса

| Имя параметра   | Тип    | Путь/Строка запроса/Тело HTTP-запроса | Описание |
|-----------------|--------|----------------------------------------|----------|
| Spreadsheet     | File   | FormData                               | Загрузка файла электронной таблицы. |
| worksheet       | String | Query                                  | Имя листа. |
| cellArea        | String | Query                                  | Заданный диапазон данных. |
| Horizontal      | Boolean| Query                                  | Горизонтальное/вертикальное отражение. По умолчанию: true |
| outPath         | String | Query                                  | (Необязательно) Путь к папке, где хранится рабочая книга. По умолчанию: null. |
| outStorageName  | String | Query                                  | Имя хранилища для выходного файла. |
| region          | String | Query                                  | Региональные/языковые настройки электронной таблицы (например, `en-US`, `fr-FR`). Влияет на форматирование чисел, разбор дат и поведение, зависящее от региона. |
| password        | String | Query                                  | Пароль для открытия файла электронной таблицы. |

### Параметр тела запроса

| Имя параметра | Тип | Описание |
|--------------|-----|----------|
| *Нет*        | *N/A* | *Дополнительное тело в формате JSON не требуется; файл отправляется как multipart/form-data.* |

### **Ответ**

```json
{
  "File": "<двоичный поток преобразованной рабочей книги>"
}
```

**Коды статуса ответа**

| Код | Значение | Описание |
|-----|----------|----------|
| 200 | OK | Операция завершена успешно, возвращён преобразованный файл электронной таблицы. |
| 400 | Bad Request | Отсутствует или некорректен один или несколько обязательных параметров. |
| 401 | Unauthorized | Ошибка аутентификации — отсутствует или некорректен JWT-токен. |
| 413 | Payload Too Large | Загруженный файл превышает допустимый предельный размер. |
| 500 | Internal Server Error | На сервере произошла непредвиденная ошибка. |

## Как использовать FlipData с SDK

### Спецификация FlipData

[Спецификация API FlipData](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TransformController/FlipData) определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия напрямую из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells Cloud. В следующем примере показано, как выполнять вызовы облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Используйте HTTPS для безопасного соединения
curl -v "https://api.aspose.cloud/v4.0/cells/flip?worksheet=Sheet1&cellArea=A1:B3&Horizontal=true&outPath=output%2Ffolder&outStorageName=MyStorage&region=en-US&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "File": "<двоичный поток преобразованной рабочей книги>"
}
```

{{< /tab >}}

{{< /tabs >}}

### Использование SDK облачных сервисов Aspose.Cells

Использование SDK — это самый быстрый способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах проекта. Полный список SDK облачных сервисов Aspose.Cells доступен в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells Cloud с использованием различных SDK:
 `[TBD]`
---