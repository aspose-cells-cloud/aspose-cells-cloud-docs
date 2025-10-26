---
title: "Cómo ejecutar el contenedor Docker en la nube Aspose.Cells: ejecute el contenedor en la nube oficial Aspose.Cells en 3 pasos: extraer, configurar, iniciar"
second_title: Documen
ArticleTitle: How to Run Aspose.Cells Cloud Docker Containe
LinkTitle: Docker Containe
type: docs
url: /es/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Cómo ejecutar el contenedor Docker Aspose.Cells en la nube. Aspose.Cells en la nube admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Cómo ejecutar un contenedor Docker
---
 El**Estibador** La tecnología está diseñada para automatizar la implementación de aplicaciones mediante el uso de contenedores ligeros. Los desarrolladores pueden usar un**Contenedor Docker** para envolver una aplicación con todas sus bibliotecas y dependencias e implementar todo como un solo paquete.

 Aspose.Cells El equipo de Cloud ha publicado el contenedor Docker en[Centro de Docker](https://hub.docker.com/r/aspose/cells-cloud) Para facilitar el uso de Docker, las siguientes secciones le guiarán sobre cómo ejecutar comandos de Docker o escribir la configuración en un archivo Yaml para la herramienta Docker Compose.

## Configuración del contenedor

### Volúmenes requeridos

|Ruta de montaje en el contenedor|Descripción|
|:- |:- |
|C:\fuentes|Carpeta con fuentes, que se utilizarán para renderizar documentos|
|C:\datos|Carpeta de almacenamiento de archivos|

### Parámetros

|Nombre|Descripción|
|:- |:- |
|Clave pública de licencia|Clave pública de la licencia|
|LicenciaClavePrivada|Clave privada de la licencia|

Si se omiten los parámetros "Licencia", la aplicación funcionará en modo de prueba.

### 1. Extraiga la imagen de la nube Aspose.Cells

```bash
# Pull Aspose.Cells Cloud Image latest version
docker pull aspose/cells-cloud:latest
```

```powershell
# Pull Aspose.Cells Cloud Image  version on windows server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
# Pull Aspose.Cells Cloud Image  version on windows server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0 

# Pull Aspose.Cells Cloud Image  version on windows 11
docker pull aspose/cells-cloud:ltsc2019.25.9.0 
```

### 2. Configuraciones para la herramienta Docker-Compose

Puede escribir las siguientes configuraciones en su archivo yaml para la herramienta Docker-Compose:

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

### 3. Ejecute un contenedor Docker mediante la línea de comandos

 Simplemente puede ejecutar el siguiente comando de Docker después de extraer el contenedor de[Centro de Docker](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```
