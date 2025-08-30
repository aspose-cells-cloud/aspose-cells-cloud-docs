---
title: Как запустить Docker-контейнер
second_title: Aspose.Cells Cloud Documen
type: docs
url: /ru/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Как запустить контейнер Docker Cloud Aspose.Cells. Cloud Aspose.Cells поддерживает Excel для создания, преобразования, слияния, разделения, защиты, внутренних операций с объектами и т. д.
weight: 100
kwords: Excel, Office Облако, REST API, Электронная таблица, PDF, CSV, Json, Markdown, Как запустить Docker-контейнер
---
 The**Докер** Технология предназначена для автоматизации развертывания приложений с помощью легковесных контейнеров. Разработчики могут использовать**Docker-контейнер** для упаковки приложения со всеми его библиотеками и зависимостями и развертывания всего как единого пакета.

 Aspose.Cells Команда Cloud опубликовала Docker-контейнер на[Докер-хаб](https://hub.docker.com/r/aspose/cells-cloud)Для удобства пользователей Docker. В следующих разделах вы узнаете, как выполнять команды Docker или записывать конфигурацию в файл Yaml для инструмента Docker Compose.

## Конфигурация контейнера

### Требуемые объемы

|Путь монтирования в контейнере|Описание|
|:- |:- |
|C:\fonts|Папка со шрифтами, которые будут использоваться для рендеринга документов|
|C:\data|Папка для хранения файлов|

### Параметры

|Имя|Описание|
|:- |:- |
|LicensePublicKey|Открытый ключ лицензии|
|LicensePrivateKey|Закрытый ключ лицензии|

Если параметры «Лицензия» не указаны, приложение будет работать в пробном режиме.

### Запуск Docker-контейнера с помощью командной строки

 Вы можете просто запустить следующую команду Docker после извлечения контейнера из[Докер-хаб](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Конфигурации для инструмента Docker-Compose

Вы можете прописать следующие конфигурации в файле yaml для инструмента Docker-Compose:

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
