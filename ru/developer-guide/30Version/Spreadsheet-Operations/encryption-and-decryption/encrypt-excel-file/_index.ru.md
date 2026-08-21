---
title: "Шифрование рабочей тетради Excel с помощью API Aspose.Cells Cloud – примеры cURL и SDK"
second_title: "Документ"
linktype: "Шифрование файла Excel"
type: docs
url: /ru/excel-file-encrypt/
aliases: [  /ru/encrypt-excel-workbooks/ , /ru/workbook/encrypt/ ]
keywords: "шифрование рабочей тетради Aspose Cells, API шифрования Excel, REST API, cURL, .NET, Java, Python, PHP, Ruby, Node.js, Go, Perl"
description: "Узнайте, как зашифровать рабочую тетрадь Excel с помощью REST API Aspose.Cells Cloud (версия 3.0). Включает команду cURL, примеры кода SDK (C#, Java, Python и др.), необходимые параметры и обработку ошибок."
weight: 20
ArticleTitle: "Шифрование рабочей тетради Excel с помощью API Aspose.Cells Cloud – примеры cURL и SDK"
---

Этот REST API шифрует **рабочую тетрадь** Excel.

**Необходимые условия:** Перед вызовом этой конечной точки у вас должен быть действительный JWT-токен и рабочая тетрадь, загруженная в хранилище.

## API PostEncryptDocument

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/encryption
```

### **Безопасность и аутентификация**

API Aspose.Cells Cloud защищены и требуют <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">аутентификации по токену JWT</a>.

### **Параметры запроса**

| Имя параметра | Тип   | Обязательный | Описание                                 |
| ------------- | ----- | ----------- | ---------------------------------------- |
| folder        | string | ✗          | Путь к папке с исходной рабочей тетрадью. |
| storageName   | string | ✗          | Имя используемого хранилища.             |

### **Параметр тела запроса**

| Имя параметра | Тип                        | Обязательный | Описание                            |
| ------------- | -------------------------- | ----------- | ----------------------------------- |
| encryption    | WorkbookEncryptionRequest | ✓           | Параметры шифрования рабочей тетради. |

#### **WorkbookEncryptionRequest**

| Имя параметра | Тип     | Обязательный | Описание                                                                                   |
| ------------- | ------- | ----------- | ------------------------------------------------------------------------------------------ |
| EncryptionType | string  | ✓          | Алгоритм шифрования. См. таблицу ниже с поддерживаемыми значениями и их описанием.         |
| KeyLength     | integer | ✗          | Длина ключа шифрования в битах (игнорируется для `XOR` и `Compatible`).                    |
| Password      | string  | ✓          | Пароль, используемый для шифрования.                                                       |

#### **Значения EncryptionType**

| Значение                          | Описание                                       |
| --------------------------------- | ---------------------------------------------- |
| `XOR`                             | Простой алгоритм XOR (устаревший, низкая защита). |
| `Compatible`                      | Совместимое шифрование Excel 97‑2003 (40 бит). |
| `EnhancedCryptographicProviderV1` | AES‑128 с хэшем SHA‑1.                         |
| `StrongCryptographicProvider`     | AES‑256 с хэшем SHA‑512 (самый надежный).      |

### Ответ

```json
{
  "Status":"OK",
  "Code":200
}
```

**Коды HTTP-статуса**

| Код | Значение                    | Описание                                                           |
|-----|-----------------------------|--------------------------------------------------------------------|
| 200 | OK                          | Фильтр успешно применён; ответ содержит сведения об операции.      |
| 400 | Bad Request                 | Отсутствуют или некорректны параметры (например, неподдерживаемый тип файла). |
| 401 | Unauthorized                | Некорректный или отсутствующий JWT-токен.                         |
| 413 | Payload Too Large           | Загруженный файл превышает допустимый размер.                      |
| 500 | Internal Server Error       | Непредвиденная ошибка сервера.                                     |

## Как использовать API PostEncryptDocument с SDK

### Спецификация API PostEncryptDocument

<a href="https://apireference.aspose.cloud/cells/#/Workbook/PostEncryptDocument" rel="noopener noreferrer">Спецификация OpenAPI</a> определяет публично доступное программное интерфейсное описание и позволяет выполнять REST-взаимодействия непосредственно из веб-браузера.

Вы можете использовать инструмент командной строки **cURL** для простого доступа к веб-сервисам Aspose.Cells. В следующем примере показано, как выполнить вызов облачного API с помощью cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Запрос" tabName2="Ответ" >}}

{{< tab tabNum="1" >}}

```bash
# Зашифровать рабочую тетрадь "test.xlsx" с использованием алгоритма XOR (ключ 128 бит) и пароля "mateen".
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/encryption" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{ "EncryptionType": "XOR", "KeyLength": 128, "Password": "mateen"}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**Возможные ответы об ошибках**

| HTTP-статус | Код                 | Сообщение                                             |
| ----------- | ------------------- | ----------------------------------------------------- |
| 400         | BadRequest          | Отсутствуют или некорректны параметры.                |
| 401         | Unauthorized        | Токен аутентификации отсутствует или некорректен.     |
| 403         | Forbidden           | Недостаточно прав для доступа к хранилищу.            |
| 500         | InternalServerError | Непредвиденная ошибка сервера.                        |

{{< /tab >}}

{{< /tabs >}}

### Использование SDK Aspose.Cells Cloud

Использование SDK — лучший способ ускорить разработку. SDK обрабатывает низкоуровневые детали, позволяя сосредоточиться на задачах вашего проекта. Полный список SDK Aspose.Cells Cloud см. в <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">репозитории GitHub</a>.

Следующие примеры кода демонстрируют вызов веб-сервисов Aspose.Cells с использованием различных SDK:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostEncryptWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostEncryptWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostEncryptWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostEncryptWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostEncryptWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostEncryptWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostEncryptWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostEncryptWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}