---
title: "Evaluar Aspose.Cells Cloud"
second_title: "Documentos"
ArticleTitle: "Evaluar Aspose.Cells Cloud"
LinkTitle: "Evaluar"
type: docs
url: /es/evaluate-aspose-cells/
description: "Explore Aspose.Cells Cloud, la API REST para crear, convertir, fusionar, dividir, proteger y manipular archivos de Excel y otros formatos de hojas de cálculo."
weight: 60
keywords:
  - Aspose.Cells Cloud
  - Excel API
  - REST API
  - manipulación de hojas de cálculo
  - prueba gratuita
  - evaluar
---

Puede evaluar las **API REST de Aspose.Cells Cloud** creando una cuenta de prueba gratuita en el panel de control de Aspose Cloud. Tras registrarse, recibirá un **Client Id** y un **Client Secret**, que le permitirán realizar hasta 150 llamadas a la API al mes.

**Requisitos previos**  
Antes de comenzar, asegúrese de tener una conexión activa a Internet y un entorno de desarrollo compatible. La API puede llamarse directamente mediante HTTP, o bien puede utilizar uno de los SDK de Aspose.Cells (por ejemplo, para .NET, Java, Python o PHP) para facilitar la integración.

**Pasos iniciales rápidos**

1. **Crear una cuenta de prueba gratuita** – visíte la [consola de Aspose Cloud](https://dashboard.aspose.cloud), regístrese y confirme su dirección de correo electrónico.  
2. **Obtener credenciales** – localice el *Client Id* y el *Client Secret* en la sección **Autenticación** del panel de control.  
3. **Generar un token de acceso** – envíe una solicitud `POST` a `https://api.aspose.cloud/connect/token` con sus credenciales (consulte la referencia de la API para conocer la carga exacta).  
4. **Realizar su primera llamada a la API** – incluya el token en el encabezado `Authorization: Bearer <token>` y llame a un punto de acceso sencillo, por ejemplo, `GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets`.  

La prueba gratuita le brinda una idea práctica de las capacidades del servicio, permitiéndole iniciar el desarrollo y las pruebas sin ningún costo.

**Resumen de referencia de la API**

| Operación | Método | URL | Parámetros obligatorios | Respuesta de ejemplo |
|-----------|--------|-----|-------------------------|----------------------|
| Obtener token de acceso | POST | `https://api.aspose.cloud/connect/token` | `grant_type=client_credentials`, `client_id`, `client_secret` (codificado como `application/x-www-form-urlencoded`) | `{ "access_token": "eyJ0eXAi...", "expires_in": 3600 }` |
| Listar hojas de cálculo | GET | `https://api.aspose.cloud/v3.0/cells/{file}/worksheets` | Ruta: `{file}` – nombre del libro cargado; Encabezado: `Authorization: Bearer <token>` | `{ "Worksheets": { "WorksheetList": [ { "Name": "Hoja1" }, { "Name": "Hoja2" } ] } }` |

Para obtener información detallada sobre precios, límites de uso y opciones adicionales de planes, consulte la página del [Plan de prueba](https://purchase.aspose.cloud/trial).