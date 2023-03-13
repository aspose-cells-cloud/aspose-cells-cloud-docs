---
title: Как запустить Docker-контейнер
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Как запустить Docker Aspose.Cells Облачный контейнер. Aspose.Cells Облако поддерживает Excel для создания, преобразования, слияния, разделения, защиты, операций с внутренними объектами и т. д.
weight: 100
---
**Докер** Технология предназначена для автоматизации развертывания приложений с помощью облегченных контейнеров. Разработчики могут использовать**Докер-контейнер** чтобы обернуть приложение со всеми его библиотеками и зависимостями и развернуть все как единый пакет.

 Aspose.Cells Команда Cloud опубликовала контейнер Docker на[Докер Хаб](https://hub.docker.com/r/aspose/cells-cloud) для облегчения работы пользователей Docker. В следующих разделах вы узнаете, как запускать команды Docker или записывать конфигурацию в файл Yaml для инструмента компоновки Docker.

## Конфигурация контейнера

### Требуемые объемы

|Путь монтирования в контейнере|Описание|
|:- |:- |
|C:\шрифты|Папка со шрифтами, которые будут использоваться для рендеринга документов|
|C:\данные|Папка для хранения файлов|

### Параметры

|Имя|Описание|
|:- |:- |
|LicensePublicKey|Открытый ключ лицензии|
|ЛицензияПриватКей|Закрытый ключ лицензии|


Если параметры «Лицензия» не указаны, приложение будет работать в пробном режиме.


### Запустите контейнер Docker с помощью командной строки

 Вы можете просто запустить следующую команду docker после извлечения контейнера из[Докер Хаб](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Конфигурации для инструмента Docker-Compose

Вы можете написать следующие конфигурации в файле yaml для инструмента Docker-Compose:

```JAVA
AsposeCellsCloud:
      image: aspose/cells-cloud
      ports: ["5000:80"]
      volumes: [
        "C:/Windows/Fonts:C:/Windows/Fonts",
        "c:/data:c:/data",
      ]
      environment:
        "LicensePublicKey": "yourKeyHere"
        "LicensePrivateKey": "yourKeyHere"
```
