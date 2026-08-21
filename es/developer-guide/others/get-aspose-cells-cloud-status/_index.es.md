---
title: "Aspose.Cells Cloud Web API - Obtener el estado de Aspose.Cells Cloud"
second_title: "Documento"
ArticleTitle: "Obtener el estado de Aspose.Cells Cloud"
linktitle: "Obtener el estado de Aspose.Cells Cloud"
type: docs
url: /get-aspose-cells-cloud-status/
keywords: "Aspose.Cells, API en la nube, comprobación de salud, Excel, REST"
description: " supervise el estado de salud del servicio Aspose.Cells Cloud en tiempo real."
weight: 100
---

Obtenga el estado de salud del servicio Aspose.Cells Cloud en tiempo real.

**Prerrequisitos:** Para llamar a esta API, debe obtener un token de acceso Bearer mediante sus credenciales de cliente de Aspose Cloud. Incluya el token en el encabezado `Authorization` como `Bearer {access_token}`.

## **Obtener el estado de Aspose.Cells Cloud**

### **API web**

El extremo utiliza el método HTTP **GET** y no requiere un cuerpo de solicitud.

```
GET https://api.aspose.cloud/v4.0/cells
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                   |
| -------------------- | ------ | --------------------------------------- | --------------------------------------------- |
| Authorization        | String | Cabecera                                | Token Bearer para autenticación (obligatorio) |
| format               | String | Consulta                                | Formato de respuesta deseado, p. ej., `json` |

### **Respuesta**

```json
{
  "status": "OK",
  "service": "Aspose.Cells Cloud",
  "timestamp": "2026-07-06T12:34:56Z"
}
```

**Esquema de respuesta**

| Campo     | Tipo              | Descripción                                |
| --------- | ----------------- | ------------------------------------------ |
| status    | string            | Estado del servicio (`OK`, `Degradado`, etc.) |
| service   | string            | Nombre del servicio.                       |
| timestamp | string (ISO‑8601) | Hora de la comprobación del estado.        |

La API devuelve una carga JSON estándar que incluye el **estado** de salud actual del servicio Aspose.Cells Cloud.

**Códigos de estado HTTP**

- **200 OK** – El servicio está operativo y la respuesta contiene la información de estado.
- **401 Unauthorized** – Token de autenticación faltante o no válido.
- **503 Service Unavailable** – El servicio está actualmente fuera de servicio para mantenimiento o presenta problemas.

## Cómo utilizar la API de Obtener el estado de Aspose.Cells Cloud con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/CellsStatusController/GetAsposeCellsCloudStatus) define una interfaz de programación accesible públicamente que le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

El uso del SDK simplifica la integración y reduce el código repetitivo. El SDK gestiona los detalles subyacentes, lo que le permite obtener el estado de ejecución de Aspose.Cells Cloud con un esfuerzo mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver la lista completa de SDK de Aspose.Cells Cloud.

---