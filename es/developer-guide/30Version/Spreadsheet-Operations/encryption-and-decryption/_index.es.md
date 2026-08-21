---
title: "Cifrar, descifrar y firmar digitalmente archivos de Excel"
second_title: "Documento"
linktype: "Proteger Excel"
type: docs
url: /es/protect/
aliases: [  /es/workbook/password/ ]
keywords: "Excel, proteger, cifrar, descifrar, firma digital, Aspose.Cells Cloud, API REST, contraseña, seguridad"
description: "Aprenda a proteger, cifrar, descifrar y firmar digitalmente libros de Excel con la API REST de Aspose.Cells Cloud – ejemplos de código para Android, C#, Java, Python y más."
ArticleTitle: "Cifrar, descifrar, firmar digitalmente y proteger archivos de Excel mediante la API de Aspose.Cells Cloud"
weight: 36
---

## **Protección y desprotección de archivos de Excel**

**¿Qué es la "protección" en Aspose.Cells Cloud?**  
La operación **Protect** (Proteger) asegura un libro de Excel aplicando una contraseña que restringe la apertura, edición o modificación de la estructura del archivo. La API también admite el cifrado y descifrado del libro, así como la adición de una firma digital para verificar que no ha sido alterado.

**Referencia de la API**

| Método HTTP | Endpoint | Parámetros requeridos (consulta/cuerpo) | Cuerpo de solicitud de ejemplo | Respuestas típicas |
|-------------|----------|----------------------------------------|--------------------------------|-------------------|
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/protect` | `fileName` (ruta), `password` (consulta) | `{ "password": "MiSecreto123" }` | `200 OK` – protección aplicada, `400 Solicitud incorrecta`, `401 No autorizado`, `500 Error interno del servidor` |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/unprotect` | `fileName` (ruta), `password` (consulta) | N/A | `200 OK` – protección eliminada, códigos de error como arriba |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/encrypt` | `fileName` (ruta), `password` (consulta) | N/A | `200 OK` – archivo cifrado |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/decrypt` | `fileName` (ruta), `password` (consulta) | N/A | `200 OK` – archivo descifrado |
| POST | `https://api.aspose.cloud/v3.0/cells/{fileName}/sign` | `fileName` (ruta) | `{ "certificatePath": "/certs/mycert.pfx", "certificatePassword": "contraseñaCert" }` | `200 OK` – firma digital añadida |

**Ejemplo de código (C#)**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

// Inicializar el cliente de la API
var config = new Configuration
{
    AppSid = "SU_APP_SID",
    AppKey = "SU_APP_KEY",
    BaseUrl = "https://api.aspose.cloud"
};
var api = new CellsApi(config);

// Proteger el libro
var protectRequest = new PostProtectWorkbookRequest(
    name: "Ejemplo.xlsx",
    password: "MiSecreto123"
);
api.PostProtectWorkbook(protectRequest);
```

**Requisitos previos**  
- Una suscripción activa a Aspose.Cells Cloud.  
- `AppSid` y `AppKey` para autenticación.  

**Autenticación**  
Todas las solicitudes deben incluir el encabezado `Authorization` con un token JWT válido obtenido desde el punto final de autenticación de Aspose Cloud.

**Manejo de errores**  
Compruebe el código de estado HTTP y el objeto `Error` devuelto en el cuerpo de la respuesta. Los errores comunes incluyen contraseña inválida (`400`), archivo ausente (`404`) y fallos de autenticación (`401`).

**Notas**  
- El mismo endpoint puede usarse para **cifrar** o **descifrar** cambiando el segmento de acción (`/encrypt`, `/decrypt`).  
- Las firmas digitales requieren un archivo de certificado válido accesible para la API.

- [Cifrar un archivo de Excel con la API de Aspose.Cells Cloud](/cells/excel-file-encrypt/)
- [Proteger un archivo de Excel con la API de Aspose.Cells Cloud](/cells/protect-excel-file/)
- [Añadir una firma digital a un archivo de Excel](/cells/excel-digital-signature/)
- [Proteger archivos de Excel – guía detallada](/cells/protect-excel-files/)
- [Establecer una contraseña para un archivo de Excel](/cells/workbook/password/modify/)
- [Descifrar un archivo de Excel](/cells/excel-file-decrypt/)
- [Desproteger un archivo de Excel](/cells/excel-file-unprotect/)
- [Desbloquear archivos de Excel](/cells/unlock-excel-files/)
- [Borrar la contraseña de un archivo de Excel](/cells/clear-excel-files-password/)
---