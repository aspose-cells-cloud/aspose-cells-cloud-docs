﻿---
title: Цифроваяподпись
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/specification/model/digitalsignature/
description: "Aspose.Cells Спецификация облачной модели: DigitalSignature. Легко обрабатывайте Excel и другие документы электронных таблиц с помощью таких функций, как открытие, создание, редактирование, разделение, слияние, сравнение и преобразование."
kwords: Excel, Office, электронная таблица, Cloud REST API, DigitalSignature
weight: 50
---
## **цифровая подпись**

 Подпись в файле.

| Имя свойства| Тип недвижимости| Обнуляемый| Только чтение| Значение по умолчанию| Описание|
|:- |:- |:- |:- |:- |:- |
| Комментарии| Нить| Истинный| ЛОЖЬ|| Цель подписи.|
| SignTime| Нить| Истинный| ЛОЖЬ|| Время подписания документа.|
| Идентификатор| Нить| Истинный| ЛОЖЬ|| Указывает GUID, на который можно ссылаться с GUID строки подписи, хранящейся в содержимом документа. Значение по умолчанию — пустой (все нули). Guid.|
| Пароль| Нить| Истинный| ЛОЖЬ|| Указывает текст фактической подписи в цифровой подписи. Значение по умолчанию — пусто.|
| Изображение|Множество<Byte> | Истинный| ЛОЖЬ|| Указывает изображение для цифровой подписи. Значение по умолчанию — ноль.|
| идентификатор поставщика| Нить| Истинный| ЛОЖЬ|| Указывает идентификатор класса поставщика подписи. Значение по умолчанию — пустой (все нули). Guid.|
| Действует| логическое значение| Истинный| ЛОЖЬ|| Если эта цифровая подпись действительна и документ не был подделан, это значение будет истинным.|
| XAdESType| Нить| Истинный| ЛОЖЬ|| Тип XAdES. Значение по умолчанию — Нет (XAdES отключен).|

