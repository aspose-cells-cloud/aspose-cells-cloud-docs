---
title: Cómo ejecutar Docker Containe
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/getting-started/how-to-run-docker-container/
aliases: [/how-to-run-docker-container/]
description: Cómo ejecutar Docker Aspose.Cells Contenedor en la nube. Aspose.Cells La nube admite Excel para crear, convertir, fusionar, dividir, proteger, operación de objetos internos, etc.
weight: 100
---
 El**Estibador** La tecnología está diseñada para automatizar el despliegue de las aplicaciones mediante el uso de contenedores ligeros. Los desarrolladores pueden usar un**Contenedor Docker** para envolver una aplicación con todas sus bibliotecas y dependencias e implementar todo como un solo paquete.

 Aspose.Cells El equipo de la nube ha publicado Docker Container en[Centro acoplable](https://hub.docker.com/r/aspose/cells-cloud) para facilitar a los usuarios de Docker. Las siguientes secciones lo guiarán sobre cómo ejecutar los comandos de Docker o escribir la configuración en un archivo Yaml para la herramienta de redacción de Docker.

## Configuración de contenedores

### Volúmenes requeridos

|Ruta de montaje en contenedor|Descripción|
|:- |:- |
|C:\fuentes|Carpeta con fuentes, que se utilizará para representar documentos|
|C:\datos|Carpeta de almacenamiento de archivos|

### Parámetros

|Nombre|Descripción|
|:- |:- |
|LicensePublicKey|Clave pública de la licencia|
|LicensePrivateKey|Clave privada de la licencia|


Si se omiten los parámetros de "Licencia", la aplicación funcionará en modo de prueba.


### Ejecute un contenedor Docker usando la línea de comando

 Simplemente puede ejecutar el siguiente comando docker después de sacar el contenedor de[Centro acoplable](https://href.li/?https://hub.docker.com/r/aspose/cells-cloud).

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
