---
title: "Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud"
second_title: "Documentación"
ArticleTitle: "Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud"
linktitle: "Ejecución del contenedor"
type: docs
url: /es/run-aspose-cells-cloud-docker-container/
description: "Aprenda cómo iniciar Aspose.Cells Cloud en un contenedor Docker en Windows Server 2022. Comandos paso a paso para el modo de prueba, facturación por uso, facturación por licencia, configuración de almacenamiento y comprobación de estado."
weight: 30
keywords: "Aspose.Cells, Docker, Windows Server 2022, modo de prueba, facturación por uso, facturación por licencia, configuración de almacenamiento"
---

Aspose.Cells Cloud Docker proporciona una imagen de contenedor lista para ejecutar que aloja la API de Aspose.Cells Cloud de forma local o en una nube privada. Esta guía muestra cómo iniciar el contenedor en tres modos de licencia comunes: **Prueba**, **Facturación por uso** y **Facturación por licencia**, e incluye una variante que utiliza un token de acceso. Todos los comandos están escritos para PowerShell en Windows Server 2022; adapte las rutas de volumen si utiliza Linux.

**Requisitos previos**

- Motor Docker 20.10 o posterior instalado y en ejecución.  
- PowerShell 5.1 o PowerShell 7+.  
- Puerto abierto 5000 dentro del contenedor (mapeado al puerto 47900 del host) y asegúrese de que el cortafuegos del host permita tráfico entrante en el puerto 47900.  
- Para los modos de facturación por uso o por licencia, tenga disponibles su `LicensePublicKey`, `LicensePrivateKey` o un archivo de licencia, o un `AccessToken` si utiliza el modo por token.  
- Una carpeta local (por ejemplo, `C:\data`) que se montará como almacenamiento para el contenedor.

**Inicio rápido (modo de prueba)**  

Ejecute el siguiente comando para iniciar el contenedor en modo de prueba:

```powershell
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

## Ejecutar el contenedor Docker de Aspose.Cells Cloud en modo de prueba

```powershell
# Windows Server 2022
docker run -p 47900:5000 aspose/cells-cloud:ltsc2022.22.9.0
```

El contenedor se ejecuta en primer plano y escucha en el puerto del host **47900**, que se redirige al puerto interno del contenedor **5000**.

## Ejecutar el contenedor Docker de Aspose.Cells Cloud en modo de facturación por uso

```powershell
# Windows Server 2022
# Modo de facturación por uso: establezca LicensePublicKey y LicensePrivateKey como variables de entorno.
# Monte una carpeta de almacenamiento (host → contenedor)
#   -v c:/data:c:/data
# Monte la carpeta de fuentes de Windows para que la API pueda acceder a las fuentes del sistema
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicensePublicKey=suPublicKeyDeLicencia `
  -e LicensePrivateKey=suPrivateKeyDeLicencia `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

El contenedor se ejecuta en modo desacoplado (`-d`). Después de iniciar, puede verificar que el servicio es accesible:

```powershell
curl http://localhost:47900/v3.0/health
```

**Ejemplo de `storageResource.json`**

```json
{
  "default": {
    "type": "Local",
    "rootFolder": "c:/data"
  }
}
```

## Ejecutar el contenedor Docker de Aspose.Cells Cloud en modo de facturación por licencia

```powershell
# Windows Server 2022
# Modo de facturación por licencia: proporcione un archivo de licencia mediante la variable de entorno LicenseFile.
# Monte una carpeta de almacenamiento (host → contenedor)
#   -v c:/data:c:/data
# Monte la carpeta de fuentes de Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e LicenseFile=c:/data/aspose.cells.lic `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

## Ejecutar el contenedor Docker de Aspose.Cells Cloud con token de acceso

```powershell
# Windows Server 2022
# Modo con token de acceso: establezca AccessToken junto con las claves opcionales de facturación por uso.
# Monte una carpeta de almacenamiento
#   -v c:/data:c:/data
# Monte la carpeta de fuentes de Windows
#   -v C:/Windows/Fonts:C:/Windows/Fonts
docker run -d `
  -v c:/data:c:/data `
  -v C:/Windows/Fonts:C:/Windows/Fonts `
  -p 47900:5000 `
  -e AccessToken=ace8955d11cf82e9189ea349976da6f `
  -e LicensePublicKey=suPublicKeyDeLicencia `
  -e LicensePrivateKey=suPrivateKeyDeLicencia `
  -e storagesCredentialsFilePath=./storageResource.json `
  --name asposecellscloud `
  aspose/cells-cloud:ltsc2022.25.9.0
```

Después de iniciar el contenedor, confirme que el servicio está operativo con el mismo comando de comprobación de estado mostrado anteriormente.

## Documentación de referencia

- [Cómo configurar el almacenamiento del contenedor Docker de Aspose.Cells Cloud.](https://docs.aspose.cloud/cells/docker/storage/)

---

### Solución de problemas

- **Error en la comprobación de estado** – Asegúrese de que el puerto 47900 no esté bloqueado por un cortafuegos y de que el contenedor se esté ejecutando (`docker ps`).  
- **Errores de licencia** – Verifique que los valores de `LicensePublicKey`, `LicensePrivateKey` o `LicenseFile` sean correctos y que las variables de entorno se pasen sin espacios en blanco adicionales.  
- **Almacenamiento no accesible** – Confirme que la carpeta del host (`c:/data`) existe y que Docker tiene permisos para leer y escribir en ella.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Cómo ejecutar el contenedor Docker de Aspose.Cells Cloud",
  "description": "Guía paso a paso para iniciar Aspose.Cells Cloud en un contenedor Docker en Windows Server 2022, cubriendo los modos de prueba, facturación por uso, facturación por licencia y token de acceso.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "url": "https://docs.aspose.cloud/cells/run-aspose-cells-cloud-docker-container/",
  "keywords": "Aspose.Cells, Docker, Windows Server 2022, modo de prueba, facturación por uso, facturación por licencia, configuración de almacenamiento"
}
</script>
---