---
title: "Descarga de imagen Docker de Aspose.Cells Cloud"  
second_title: "Documento"  
ArticleTitle: "Descarga de imagen Docker de Aspose.Cells Cloud"  
linktitle: "Descarga de imagen"  
type: docs  
url: /es/docker/downloads/
description: "Obtenga las últimas imágenes Docker de Aspose.Cells Cloud para Windows Server 2016/2019 y Linux. Siga las instrucciones paso a paso, los requisitos previos y las recomendaciones de seguridad para ejecutar el contenedor localmente."  
weight: 30  
keywords: "Aspose.Cells, Cloud, Docker, contenedor, imagen, descarga, Windows Server, Linux, REST API"  
---  

## Información general  

`aspose/cells-cloud` – la imagen Docker oficial que aloja la API REST de **Aspose.Cells Cloud**. La imagen le permite ejecutar el motor completo de procesamiento de hojas de cálculo dentro de un contenedor, lo que permite implementaciones sin conexión o en nube privada sin depender de los servicios públicos en la nube de Aspose.  

**Última actualización:** 2026-06-30  

**Lista de verificación para inicio rápido**

- Verifique que la versión de Docker Engine sea 20.10 o posterior.  
- Extraiga la imagen adecuada para su sistema operativo (consulte las secciones siguientes).  
- Configure las variables de entorno `ASPOSE_CLIENT_ID` y `ASPOSE_CLIENT_SECRET`.  
- Ejecute el contenedor mapeando el puerto 8080 del host al puerto interno 80.  

---  

## Requisitos previos  

| Requisito | Detalles |
|-----------|----------|
| **Motor Docker** | Docker 20.10 o posterior instalado en el sistema operativo del host. |
| **Sistema operativo** | Windows Server 2016, Windows Server 2019 o cualquier distribución moderna de Linux. |
| **Acceso a Docker Hub** | Una cuenta activa en Docker Hub (opcional, pero recomendada para imágenes privadas). Ejecute `docker login` si necesita extraer imágenes desde un repositorio privado. |
| **Credenciales de Aspose Cloud** | `ASPOSE_CLIENT_ID` y `ASPOSE_CLIENT_SECRET`: obténgalas desde el panel de control de Aspose Cloud. |

> **Consejo:** Verifique la instalación de Docker con `docker --version`.  

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

## Ejecución del contenedor  

```sh
docker run -d \
  -e ASPOSE_CLIENT_ID=SU_CLIENT_ID \
  -e ASPOSE_CLIENT_SECRET=SU_CLIENT_SECRET \
  -p 8080:80 \
  --name aspose-cells \
  aspose/cells-cloud:ltsc2019.21.9
```

* **Variables de entorno** – `ASPOSE_CLIENT_ID` y `ASPOSE_CLIENT_SECRET` proporcionan las credenciales requeridas por la API.  
* **Mapeo de puertos** – El contenedor expone el puerto 80; mápelo a un puerto del host (por ejemplo, 8080) para acceder al servicio.  
* **Modo desacoplado (`-d`)** – Ejecuta el contenedor en segundo plano.  

---  

## Numeración de versiones y actualizaciones  

| Sistema operativo | Etiqueta | Fecha de lanzamiento | Cómo obtener la última versión |
|-------------------|----------|----------------------|-------------------------------|
| Windows Server 2016 | `ltsc2016.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2016.latest` |
| Windows Server 2019 | `ltsc2019.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:ltsc2019.latest` |
| Linux | `linux.21.9` | 2026-06-30 | `docker pull aspose/cells-cloud:linux.latest` |

> **Nota:** La etiqueta `21.9` corresponde a la versión estable actual. Utilice la etiqueta `latest` o consulte las [notas de lanzamiento de Aspose.Cells Cloud](/cells/release-notes/) para versiones más recientes.  

---  

## Verificación y seguridad  

* **Comprobación del digest de la imagen**  

  ```sh
  docker image inspect aspose/cells-cloud:ltsc2019.21.9 --format='{{.RepoDigests}}'
  ```

* **Escaneo de vulnerabilidades** (recomendado)  

  ```sh
  trivy image aspose/cells-cloud:ltsc2019.21.9
  ```

* **Prácticas recomendadas** – Mantenga Docker actualizado, ejecute los contenedores con los mínimos privilegios necesarios y realice escaneos periódicos en las imágenes en busca de CVE conocidos.  

* **Ejemplo de datos estructurados (JSON-LD)**  

  ```html
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "SoftwareApplication",
    "name": "Imagen Docker de Aspose.Cells Cloud",
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

## Problemas comunes y solución de problemas  

| Síntoma | Causa posible | Solución |
|---------|---------------|----------|
| `docker: command not found` | Docker no está instalado o la variable PATH no está configurada | Instale Docker y reinicie la terminal. |
| Fallo de autenticación al extraer la imagen | Falta `docker login` o las credenciales son incorrectas | Ejecute `docker login` con credenciales válidas de Docker Hub. |
| El contenedor termina inmediatamente | Faltan variables de entorno obligatorias | Proporcione `ASPOSE_CLIENT_ID` y `ASPOSE_CLIENT_SECRET` como se muestra en la sección **Ejecución del contenedor**. |
| Conflicto de puertos en el host | El puerto del host ya está en uso | Seleccione un puerto del host distinto (por ejemplo, `-p 8081:80`). |

---  

## Consulte también  

* [Documentación de la API de Aspose.Cells Cloud](/cells/cloud/api/)  
* [Notas de lanzamiento de Aspose.Cells Cloud](/cells/release-notes/) – registro detallado de cambios para la versión 21.9 y versiones posteriores.  
* [Características del contenedor Docker de Aspose.Cells](/cells/docker/features/)  
* [Etiquetas de la imagen Docker de Aspose.Cells](/cells/docker/tag-list/)  

---  

*Autorizado por el equipo de ingeniería de Aspose Cloud.*