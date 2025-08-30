---
title: Cómo ejecutar Docker Container
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Cómo ejecutar el contenedor Docker Aspose.Cells en la nube. Aspose.Cells en la nube admite Excel para crear, convertir, fusionar, dividir, proteger, realizar operaciones con objetos internos, etc.
weight: 100
kwords: Excel, Office Nube, REST API, Hoja de cálculo, PDF, CSV, Json, Markdown, Cómo ejecutar un contenedor Docker
---
 El**Estibador** La tecnología está diseñada para automatizar la implementación de las aplicaciones mediante el uso de contenedores ligeros. Los desarrolladores pueden usar un**Contenedor Docker** para envolver una aplicación con todas sus bibliotecas y dependencias e implementar todo como un solo paquete.

 Aspose.Cells El equipo de Cloud ha publicado el contenedor Docker en[Centro de Docker](https://hub.docker.com/r/aspose/cells-cloud)Para facilitar el uso de Docker, las siguientes secciones le guiarán sobre cómo ejecutar comandos de Docker o escribir la configuración en un archivo Yaml para la herramienta Docker Compose.

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
|Clave privada de licencia|Clave privada de la licencia|

Si se omiten los parámetros de "Licencia", la aplicación funcionará en modo de prueba.

### Ejecutar un contenedor Docker mediante la línea de comandos

 Simplemente puede ejecutar el siguiente comando de Docker después de extraer el contenedor de[Centro de Docker](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

```JAVA
docker run   -e "LicensePublicKey=public_key" -e "LicensePrivateKey=private_key" -v c:/data:c:/data  -v C:/Windows/Fonts:C:/Windows/Fonts -p 80:5000   aspose/cells-cloud
```

### Configuraciones para la herramienta Docker-Compose

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
