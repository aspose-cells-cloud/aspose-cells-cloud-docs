---
title: "Блокировка файлов Excel"
second_title: "Документ"
linktitle: "Блокировка файлов Excel"
type: docs
url: /ru/lock-excel-files/
aliases: [/lock/without-storage/, /lock/, /lock/without-using-storage/]
keywords: "Блокировка, Excel, API, Aspose.Cells, Облако, REST, Рабочая тетрадь, Электронная таблица, SDK"
description: "Узнайте, как блокировать рабочие тетради Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает HTTPS-эндпоинт, аутентификацию, cURL-запрос, схему ответа и примеры кода SDK для C#, Java, Python и других языков."
ArticleTitle: "Блокировка файлов Excel – Документация API Aspose.Cells Cloud"
weight: 70
---

**Версия API:** v3.0 (текущая)

Этот REST API **блокирует** рабочие тетради Excel.

## API PostLock

```http
POST https://api.aspose.cloud/v3.0/cells/lock
```

**Необходимые условия** – Запрос должен отправляться по протоколу **HTTPS** и включать действительный токен OAuth 2.0 Bearer в заголовке `Authorization`.

### Параметры запроса:

| Имя параметра | Тип   | Расположение                  | Описание                                            |
|---------------|-------|-------------------------------|-----------------------------------------------------|
| file          | file  | form‑data (multipart body)    | Рабочая тетрадь Excel, подлежащая загрузке и блокировке. |
| password      | string| query string                  | Пароль для рабочей тетради (необязательно).        |

<a href="https://apireference.aspose.cloud/cells/#/LightCells/PostLock" target="_blank" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное решение и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать утилиту командной строки cURL для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как **вызвать** облачный API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/lock?password=123456" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

*Вы можете загрузить тестовую рабочую тетрадь — [Sample.xlsx](https://example.com/Sample.xlsx) — для проверки запроса.*

**Примечание:** API поддерживает файлы размером до 100 МБ; более крупные данные могут привести к ответу с кодом 413 («Payload Too Large» — «Слишком большой объем данных»).

### **Детали ответа**

| Поле        | Тип             | Описание                                            |
|-------------|-----------------|-----------------------------------------------------|
| Filename    | string          | Имя заблокированной рабочей тетради, возвращаемое сервисом. |
| FileSize    | integer         | Размер заблокированного файла в байтах.            |
| FileContent | string (Base64) | Заблокированная рабочая тетрадь, закодированная в формате Base64. |

Для извлечения заблокированной рабочей тетради декодируйте значение `FileContent` из Base64 и сохраните его, используя имя файла `Filename`, указанное в ответе.

### **Обработка ошибок**

– API возвращает стандартные HTTP-коды состояния (например, `400 Bad Request`, `401 Unauthorized`, `500 Internal Server Error`) вместе с объектом ошибки в формате JSON, содержащим поля `Code` и `Message`.

## Семейство облачных SDK

Использование SDK — это лучший способ ускорить разработку. SDK скрывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Ознакомьтесь со <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">репозиторием на GitHub</a>, чтобы получить полный список SDK Aspose.Cells Cloud.

Следующие примеры кода демонстрируют, как вызывать веб-сервисы Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostLock.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostLock.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostLock.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostLock.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostLock.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostLock.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostLock.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostLock.go" >}}

{{< /tab >}}

{{< /tabs >}}