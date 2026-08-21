---
title: "Aspise.Cells Cloud Web API – Otras características: Verificación de estado, Obtener clave pública"
linktitle: "Otras características"
ArticleTitle: "Otras características: Verificación de estado, Obtener clave pública"
second_title: "Documento"
type: docs
url: /other-features/
keywords: "Aspose.Cells, API en la nube, verificación de estado, clave pública, token de acceso, Excel, REST"
description: "Explore otras características de Aspose.Cells Cloud: punto final de verificación de estado del servicio, recuperación de clave pública y generación de tokens para asegurar sus integraciones con la API de Excel."
weight: 180
---

**Requisitos previos** – Para utilizar las características que se enumeran a continuación, debe tener una suscripción válida a Aspose Cloud y un par **Client ID** / **Client Secret** activo para la autenticación.

Estas “otras características” proporcionan operaciones de soporte esenciales para la API de Aspose.Cells Cloud, como confirmar la disponibilidad del servicio, recuperar claves criptográficas y obtener tokens de acceso. Normalmente, se llaman antes de trabajar con puntos finales relacionados con libros de cálculo.

- **[Verificación de estado del servicio en la nube de Aspose.Cells](https://docs.aspose.cloud/cells/check-cloud-service-health/)**  
  Confirme que el servicio de Aspose.Cells Cloud es accesible y opera correctamente. Una llamada exitosa devuelve **HTTP 200** con el JSON `{ "status": "OK" }`. Utilice este punto final al principio de su flujo de trabajo para evitar fallos innecesarios.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/check-cloud-service-health/">Más información</a>

- **[Obtener estado de ejecución de Aspose.Cells Cloud](https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/)**  
  Recupere el estado actual de ejecución del servicio. La respuesta indica si la API está completamente operativa, en modo de mantenimiento o experimentando problemas.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-aspose-cells-cloud-status/">Más información</a>

- **[Obtener clave pública](https://docs.aspose.cloud/cells/get-public-key/)**  
  Obtenga la clave pública RSA (formato PEM) utilizada para verificar los tokens JWT emitidos por Aspose.Cells Cloud. Esta clave es necesaria cuando valida tokens en su lado del servidor.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/get-public-key/">Más información</a>

- **[Obtener token de acceso con Client ID y Client Secret](https://docs.aspose.cloud/cells/post-access-token/)**  
  Genere un token de acceso OAuth 2.0 utilizando el tipo de concesión **client_credentials**. Incluya su **Client ID** y **Client Secret** en el cuerpo de la solicitud; la respuesta contiene `access_token`, `token_type` y `expires_in`. Este token debe suministrarse en el encabezado `Authorization` para todas las llamadas posteriores a la API.  
  <a class="btn btn-primary" href="https://docs.aspose.cloud/cells/post-access-token/">Más información</a>