---
title: "API en la nube de Aspose.Cells: Obtener clave pública (v4.0) | Documentación REST"
second_title: "Documento"
ArticleTitle: "Obtener clave pública"
linktype: "Obtener clave pública"
type: docs
url: /es/get-public-key/
keywords: "Aspose.Cells, Clave pública, RSA, API, Nube"
description: "Recupere la clave pública RSA utilizada para cifrar datos con Aspose.Cells Cloud. Incluye el punto de conexión, parámetros, ejemplo de solicitud/respuesta, códigos de estado y ejemplos de uso de SDK."
weight: 100
---

Esta API recupera la clave pública de un algoritmo de cifrado asimétrico.

**Resumen breve:** Utilice la API de Aspose.Cells para obtener la clave pública RSA (2048 bits) necesaria para cifrar datos al trabajar con archivos de Excel en la nube. El punto de conexión devuelve la clave en formato JSON y está protegido con OAuth 2.0.

## **API para obtener la clave pública**

**Prerrequisitos:**  
Obtenga un token de acceso válido de OAuth 2.0 que incluya el ámbito `Cells.Read` antes de llamar a este punto de conexión.

### **API web**

```
GET https://api.aspose.cloud/v4.0/cells/publickey
```

**Solicitud de ejemplo (cURL)**

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/publickey" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de la solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                 |
|----------------------|--------|-----------|-----------------------------------------------------------------------------|
| Authorization        | string | Header    | Token Bearer para autenticación OAuth2 (requerido).                         |
| Accept               | string | Header    | Formato de respuesta deseado, por ejemplo, `application/json` (opcional, por defecto JSON). |

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "CellsCloudPublicKey": {
    "PublicKey": "MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAr...",
    "Algorithm": "RSA",
    "KeySize": 2048
  }
}
```

**Códigos de estado HTTP**

| Código | Significado           | Descripción                                                   |
|--------|-----------------------|---------------------------------------------------------------|
| 200    | OK                    | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta  | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado         | Token JWT no válido o faltante.                               |
| 413    | Carga útil demasiado grande | El archivo subido supera el límite de tamaño.           |
| 500    | Error interno del servidor | Error inesperado en el servidor.                         |

## Cómo usar la API para obtener la clave pública con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde su navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, permitiéndole simplemente implementar la obtención de la clave pública para celdas con un código mínimo.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

A continuación se presentan ejemplos concretos para los lenguajes más comunes:

---