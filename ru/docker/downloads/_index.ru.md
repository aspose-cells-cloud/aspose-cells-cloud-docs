---
title: "Скачивание Docker-образа Aspose.Cells Cloud"  
second_title: "Документация"  
ArticleTitle: "Скачивание Docker-образа Aspose.Cells Cloud"  
linktitle: "Скачивание образа"  
type: docs  
url: /ru/docker/downloads/
description: "Получите последнюю версию Docker-образов Aspose.Cells Cloud для Windows Server 2016/2019 и Linux. Следуйте пошаговым инструкциям, требованиям и рекомендациям по безопасности для локального запуска контейнера."  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, контейнер, образ, скачивание, Windows Server, Linux, REST API"  
---  

## Обзор  

`aspose/cells-cloud` — официальный Docker-образ, развертывающий **Aspose.Cells Cloud** REST API. Образ позволяет запускать полнофункциональный движок обработки электронных таблиц внутри контейнера, обеспечивая автономные или частные облачные развертывания без использования публичных облачных сервисов Aspose.  

**Последнее обновление:** 2026-06-30  

**Краткий чек-лист для начала работы**

- Убедитесь, что версия Docker Engine — 20.10 или выше.  
- Выполните скачивание подходящего образа для вашей ОС (см. разделы ниже).  
- Задайте переменные окружения `ASPOSE_CLIENT_ID` и `ASPOSE_CLIENT_SECRET`.  
- Запустите контейнер с привязкой порта 8080 хоста к внутреннему порту 80.  

---  

## Требования  

| Требование | Подробности |
|------------|-------------|
| **Docker Engine** | Docker 20.10 или выше, установленный на хостовой ОС. |
| **Операционная система** | Windows Server 2016, Windows Server 2019 или любая современная дистрибутив Linux. |
| **Доступ к Docker Hub** | Аккаунт Docker Hub (необязательно, но рекомендуется для частных образов). Выполните `docker login`, если планируете скачивать образы из частного репозитория. |
| **Учетные данные Aspose Cloud** | `ASPOSE_CLIENT_ID` и `ASPOSE_CLIENT_SECRET` — получите их в панели управления Aspose Cloud. |

> **Совет:** Проверьте установку Docker с помощью команды `docker --version`.  

---  

## Windows Server 2016  

```powershell
docker pull aspose/cells-cloud:ltsc2016.21.9
```

---  

## Windows Server 2019  

```powershell
docker pull aspose/cells-cloud:ltsc2019.21.9
```

---  

## Linux  

```sh
docker pull aspose/cells-cloud:linux.21.9
```

---  

## Запуск контейнера  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=YOUR_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=YOUR_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Переменные окружения** — `ASPOSE_CLIENT_ID` и `ASPOSE_CLIENT_SECRET` задают учетные данные, необходимые API.  
* **Проброс портов** — контейнер открывает порт 80; пробросите его на порт хоста (например, 8080), чтобы получить доступ к сервису.  
* **Фоновый режим (`-d`)** — запускает контейнер в фоновом режиме.  

---  

## Версионирование и обновления  

| ОС | Тег | Дата выпуска | Как получить последнюю версию |
|----|-----|--------------|-------------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Примечание:** Тег `21.9` — текущая стабильная версия. Используйте тег `latest` или ознакомьтесь с [release notes Aspose.Cells Cloud](/cells/release-notes/) для получения более новых версий.  

---  

## Проверка и безопасность  

* **Проверка дайджеста образа**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Сканирование на уязвимости** (рекомендуется)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Рекомендации по безопасности** — обновляйте Docker вовремя, запускайте контейнеры с минимально необходимыми привилегиями и регулярно проверяйте образы на наличие известных уязвимостей (CVE).  

* **Пример структурированных данных (JSON-LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Aspose.Cells Cloud Docker Image",
    "operatingSystem": "Windows Server 2016/2019, Linux",
    "softwareVersion": "21.9",
    "downloadUrl": "https://hub.docker.com/r/aspose/cells-cloud",
    "offers": {
      "price": "0",
      "priceCurrency": "USD"
    }
  }
  </script>
  ```

---  

## Типичные проблемы и устранение неполадок  

| Симптом | Возможная причина | Решение |
|--------|-------------------|---------|
| `docker: command not found` | Docker не установлен или не настроен PATH | Установите Docker и перезапустите терминал. |
| Ошибка аутентификации при скачивании | Отсутствует или неверен `docker login` | Выполните `docker login` с корректными учетными данными Docker Hub. |
| Контейнер немедленно завершает работу | Отсутствуют обязательные переменные окружения | Укажите `ASPOSE_CLIENT_ID` и `ASPOSE_CLIENT_SECRET`, как показано в разделе **Запуск контейнера**. |
| Конфликт порта на хосте | Порт хоста уже занят | Выберите другой порт хоста (например, `-p 8081:80`). |

---  

## См. также  

* [Документация API Aspose.Cells Cloud](/cells/cloud/api/)  
* [Release notes Aspose.Cells Cloud](/cells/release-notes/) — подробный список изменений для версии 21.9 и новее.  
* [Функции Docker-контейнера Aspose.Cells](/cells/docker/features/)  
* [Теги Docker-образа Aspose.Cells](/cells/docker/tag-list/)  

---  

*Автор: инженерная команда Aspose Cloud.*