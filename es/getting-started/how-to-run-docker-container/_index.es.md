---
title: "Ejecutar el contenedor Docker de Aspose.Cells Cloud: extraer, configurar e iniciar"
second_title: "Documento"
ArticleTitle: "Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud"
LinkTitle: "Contenedor Docker"
type: docs
url: /es/getting-started/how-to-run-docker-container/
aliases: [  /es/how-to-run-docker-container/ ]
description: "Aprenda cómo extraer, configurar y ejecutar el contenedor Docker de Aspose.Cells Cloud en Windows o Linux. Incluye YAML de Docker Compose, configuración de licencia, asignación de puertos y consejos para solucionar problemas."
weight: 100
keywords:
  - "Aspose.Cells Cloud Docker"
  - "contenedor Docker"
  - "Docker Compose"
  - "claves de licencia"
  - "Excel"
  - "hoja de cálculo"
  - "API en la nube"
  - "Docker"
  - "Aspose Cells"
  - "API"
---

La tecnología Docker está diseñada para automatizar la implementación de aplicaciones mediante contenedores ligeros. Los desarrolladores pueden usar un contenedor Docker para empaquetar una aplicación junto con todas sus bibliotecas y dependencias, e implementar todo como un único paquete.

El equipo de Aspose.Cells Cloud ha publicado el contenedor Docker en <a href="https://hub.docker.com/r/aspose/cells-cloud" target="_blank" rel="noopener noreferrer">Docker Hub</a> para facilitar su uso a los usuarios de Docker.

**Requisitos previos** – Asegúrese de tener instalado Docker Engine ≥ 20.x y de que su sistema operativo (Windows 10/Server 2019/2022 o una distribución Linux compatible) cumpla con los requisitos. Opcionalmente, puede proporcionar una clave de licencia para ejecutar en modo con licencia.

- Docker Engine ≥ 20.x instalado  
- Sistema operativo compatible (Windows 10/Server 2019/2022 o una distribución Linux)  
- Clave de licencia opcional para modo con licencia  

## Configuración del contenedor

### Volúmenes obligatorios

| Ruta de montaje en el contenedor | Descripción |
| :--- | :--- |
| C:\fonts | Carpeta con fuentes que se usarán para representar documentos |
| C:\data | Carpeta de almacenamiento de archivos |

**Alternativa para Linux/macOS** – Use `/fonts` y `/data` en el contenedor y asínelos a directorios del host, como `/home/user/fonts` y `/home/user/data`, al ejecutar el contenedor.

### Parámetros

| Nombre | Descripción |
| :--- | :--- |
| LicensePublicKey | Clave pública de la licencia |
| LicensePrivateKey | Clave privada de la licencia |

Si se omiten los parámetros **License**, la aplicación se ejecutará en modo de prueba.

### 1. Extraer la imagen de Aspose.Cells Cloud

```bash
# Extraer una versión específica de la imagen de Aspose.Cells Cloud
docker pull aspose/cells-cloud:25.9.0
```

```powershell
# Extraer la imagen de Aspose.Cells Cloud para Windows Server 2019
docker pull aspose/cells-cloud:ltsc2019.25.9.0

# Extraer la imagen de Aspose.Cells Cloud para Windows Server 2022
docker pull aspose/cells-cloud:ltsc2022.25.9.0

# Extraer la imagen de Aspose.Cells Cloud para Windows 11
docker pull aspose/cells-cloud:ltsc2022.25.9.0
```

> **Nota:** Para obtener siempre la versión más reciente, también puede extraer la etiqueta `latest`: `docker pull aspose/cells-cloud:latest`.

### 2. Configuraciones para la herramienta Docker Compose

Puede escribir la siguiente configuración en un archivo **docker-compose.yml**:

```yaml
AsposeCellsCloud:
  image: aspose/cells-cloud:25.9.0
  ports: ["5000:80"]   # host 5000 → contenedor 80
  volumes:
    - "C:/Windows/Fonts:C:/Windows/Fonts"
    - "c:/data:c:/data"
  environment:
    LicensePublicKey: "suPublicKey"
    LicensePrivateKey: "suPrivateKey"
```

> **Nota:** La asignación de puertos `5000:80` significa que la API estará accesible en `http://localhost:5000`.

### 3. Ejecutar un contenedor Docker mediante la línea de comandos

```bash
docker run \
  -e "LicensePublicKey=suPublicKey" \
  -e "LicensePrivateKey=suPrivateKey" \
  -v c:/data:c:/data \
  -v C:/Windows/Fonts:C:/Windows/Fonts \
  -p 5000:80 \
  aspose/cells-cloud:25.9.0
```

**Solución de problemas:**  
- **Conflicto de puertos:** Asegúrese de que el puerto 5000 del host esté libre o cambie la asignación a un puerto no utilizado.  
- **Fallo al cargar la licencia:** Verifique que las claves pública y privada se pasen correctamente como variables de entorno o se monten como archivos.  
- **Faltan fuentes:** Si los documentos se representan con fuentes incorrectas, confirme que el directorio de fuentes se haya montado correctamente y contenga los archivos de fuente necesarios.

**Recursos relacionados:**  
- <a href="/cells/api/">Referencia de la API</a> | <a href="/cells/license/">Guía de activación de licencia</a> | <a href="/cells/getting-started/">Resumen de introducción</a>

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "Ejecutar el contenedor Docker de Aspose.Cells Cloud",
  "step": [
    {
      "@type": "HowToStep",
      "url": "#1-pull-asposecells-cloud-image",
      "name": "Extraer la imagen Docker",
      "text": "Ejecute `docker pull aspose/cells-cloud:<versión>` para descargar la imagen requerida."
    },
    {
      "@type": "HowToStep",
      "url": "#2-configurations-for-docker-compose-tool",
      "name": "Crear un archivo docker-compose",
      "text": "Defina la imagen, los puertos, los volúmenes y las variables de entorno de la licencia en `docker-compose.yml`."
    },
    {
      "@type": "HowToStep",
      "url": "#3-run-a-docker-container-using-the-command-line",
      "name": "Ejecutar el contenedor",
      "text": "Ejecute `docker run` con las variables de entorno, los montajes de volúmenes y la asignación de puertos adecuados."
    }
  ]
}
```