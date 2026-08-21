---
title: "Aspose.Cells Cloud – Verificar el estado del servicio (API)"
second_title: "Documento"
ArticleTitle: "Comprobación del estado de Aspose.Cells Cloud"
linktitle: "Verificar el estado del servicio en la nube"
type: docs
url: /es/check-cloud-service-health/
keywords: "Aspose.Cells Cloud, comprobación del estado de la API, estado REST, supervisión del servicio en la nube"
description: "Supervise en tiempo real el estado de Aspose.Cells Cloud. Conozca el endpoint GET /v4.0/cells/status/check, sus parámetros, el formato de respuesta y ejemplos de SDK."
weight: 100
---

Compruebe el estado de salud de los servicios de Aspose.Cells Cloud.

**Requisitos previos**  
Para llamar a este endpoint, debe disponer de un token de acceso válido de Aspose Cloud. Obtenga el token registrando una aplicación en el panel de control de Aspose Cloud y solicitando un token Bearer mediante el endpoint OAuth2, utilizando el client-id y client‑secret. Incluya el token en el encabezado `Authorization`, tal como se muestra a continuación.

## **Comprobar el estado del servicio en la nube**

### **API Web**

```http
GET https://api.aspose.cloud/v4.0/cells/status/check
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

### **Parámetros de solicitud**

| Parámetro     | Tipo   | Obligatorio | Descripción                                                        |
| ------------- | ------ | ----------- | ------------------------------------------------------------------ |
| Authorization | header | Sí          | Token Bearer para autenticación (`Authorization: Bearer <token>`). |
| detail        | query  | No          | Establecer en `true` para incluir información detallada de los componentes. |
| Accept        | header | No          | Formato de respuesta deseado; el valor predeterminado es `application/json`. |

### **Respuesta**

El servicio devuelve una carga útil JSON cuando la solicitud se realiza correctamente.

```json
{
  "status": "OK",
  "service": "Cells",
  "timestamp": "{{timestamp}}",
  "components": {
    "api": "Operativo",
    "storage": "Operativo",
    "database": "Operativo"
  }
}
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                              |
| ------ | --------------------- | -------------------------------------------------------- |
| 200    | OK                    | El servicio está en buen estado; consulte el ejemplo JSON anterior. |
| 401    | No autorizado         | Token de autenticación inválido o ausente.               |
| 503    | Servicio no disponible| El servicio no está en buen estado o se encuentra en mantenimiento. |
| 4xx    | Error del cliente     | Parámetros incorrectos o solicitud con formato incorrecto. |
| 5xx    | Error del servidor    | Fallo inesperado del servidor; reintente más tarde.      |

## Cómo utilizar la API de estado de Aspose.Cells Cloud con SDK

### Especificación OpenAPI

<a href="https://reference.aspose.cloud/cells/#/CellsStatusController/CheckCloudServiceHealth" target="_blank" rel="noopener noreferrer">Especificación OpenAPI</a>, que define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

El uso de los SDK constituye la mejor manera de acelerar el desarrollo. Los SDK gestionan los detalles subyacentes, lo que le permite implementar una comprobación del estado en la nube para Cells con un código mínimo.  
Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.

A continuación se muestran fragmentos de código de ejemplo que demuestran cómo invocar el endpoint de comprobación de estado con los SDK más utilizados.

---