---
title: Aspose.Cells Cloud WEb API — Получить публичный ключ
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Получить публичный ключ
type: docs
url: /ru/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Получите асимметричный открытый ключ для безопасного шифрования данных
weight: 100
kwords: асимметричное шифрование, открытый ключ, REST API, Excel API, безопасность, шифрование данных, интеграция API, JSON, документация API
---
Извлекает открытый ключ из асимметричного алгоритма шифрования.

## **Получить открытый ключ API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Параметры запроса:**

| Имя параметра| Тип| Путь/Строка запроса/Тело HTTP| Описание|
|:- |:- |:- |:- |
|||||

### **Ответ**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## Как использовать открытый ключ Get API с SDK

### Спецификация OpenAPI

 The[Спецификация OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) определяет общедоступный программный интерфейс, позволяющий вам выполнять REST-взаимодействия непосредственно из вашего веб-браузера.

### Используйте облачные SDK Aspose.Cells

Использование SDK — лучший способ ускорить разработку. SDK берёт на себя все базовые детали, позволяя вам легко реализовать получение открытого ключа для ячеек с минимальным количеством кода.
 Пожалуйста, проверьте[Репозиторий GitHub](https://github.com/aspose-cells-cloud) для полного списка Aspose.Cells Cloud SDK.

Следующие примеры кода иллюстрируют, как взаимодействовать с веб-сервисами Aspose.Cells с использованием различных SDK:
