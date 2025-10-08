---
title: Aspose.Cells Cloud Web API - Токен доступа к почте
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Токе доступа после
type: docs
url: /ru/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Получите токен доступа с помощью Cells Cloud Get Token API, который действует как прокси-сервис, перенаправляющий запросы пользователей на сервер аутентификации Cloud Aspose и безопасно возвращает полученный токен доступа клиенту.
weight: 100
kwords: Excel, Office Облако, REST API, Аутентификация, Управление токенами, Интеграция промежуточного ПО, Безопасный API, Aspose Облако
---
Получите токен доступа, используя Cloud Get Token Cells API с идентификатором клиента и секретом.

## **Токен доступа API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/HTTPBody| Описание|
|:- |:- |:- |:- |
| Идентификатор клиента| нить| запрос| Идентификатор клиента|
| Секрет клиента| нить| запрос| Секрет клиента|

### **Ответ**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## Как использовать открытый ключ Get API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) определяет общедоступный программный интерфейс, позволяющий осуществлять REST-взаимодействие непосредственно из веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя все базовые детали, позволяя вам легко реализовать получение токена доступа для ячеек с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) Полный список облачных SDK Aspose.Cells. nt. SDK берёт на себя низкоуровневые задачи и позволяет вам сосредоточиться на задачах проекта. Ознакомьтесь с[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

В следующих примерах кода показано, как совершать вызовы веб-служб Aspose.Cells с использованием различных SDK:
