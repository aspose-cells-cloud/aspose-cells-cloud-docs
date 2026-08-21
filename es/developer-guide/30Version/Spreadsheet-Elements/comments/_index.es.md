---
title: "Trabajar con comentarios de Excel"
second_title: "Document"
linktype: "Comentarios"
type: docs
url: /es/comments/
aliases: [  /es/working-with-comments/ ]
keywords: "Aspose.Cells Cloud, API de comentarios de Excel, comentarios de hojas de cálculo, API REST"
description: "Aprenda cómo agregar, recuperar, actualizar y eliminar comentarios de Excel mediante la API REST de Aspose.Cells Cloud v3.0, con ejemplos de código, requisitos previos y manejo de errores."
weight: 100
ArticleTitle: "Trabajar con comentarios de Excel – Guía de la API de Aspose.Cells Cloud"
---

Al crear un libro de Excel, los usuarios pueden agregar comentarios por diversas razones. Una utilización común es explicar una fórmula en una celda, especialmente cuando el archivo se compartirá con otras personas. Los comentarios también pueden servir como recordatorios, notas para colaboradores o como medio para hacer referencias cruzadas con otros libros. Una vez agregado un comentario, Excel permite al usuario redimensionar, reconfigurar y dar formato al cuadro de comentario según su estilo preferido. Dominar la gestión de comentarios ayuda a los usuarios a sacar el máximo partido a esta función.

**Requisitos previos**

- Una cuenta activa de Aspose.Cells Cloud.  
- Un **token de acceso** válido obtenido mediante OAuth 2.0.  
- Versión de la API **v3.0** (los puntos de conexión utilizados en esta guía pertenecen a esta versión).  
- Opcional: SDK de Aspose.Cells para su lenguaje preferido para simplificar la construcción de solicitudes.

**Versión**

Los ejemplos que se muestran a continuación están orientados a la **API REST de Aspose.Cells Cloud v3.0**. Futuras versiones de la API podrían introducir parámetros adicionales o modificar las estructuras de respuesta; siempre consulte la referencia más reciente de la API para obtener detalles actualizados.

**Agregar un comentario**

Para agregar un comentario, envíe una solicitud **POST** al siguiente punto de conexión:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Parámetros de ruta**

| Parámetro | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| `file`    | string | Sí          | Nombre del archivo del libro (incluida la extensión). |
| `sheet`   | string | Sí          | Nombre de la hoja de cálculo donde se agregará el comentario. |

**Esquema del cuerpo de la solicitud**

| Campo     | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| `CellName`| string | Sí          | Dirección en formato estilo A1 de la celda (por ejemplo, **B2**). |
| `Comment` | string | Sí          | Texto del comentario que se almacenará. |
| `Author`  | string | No          | Nombre del autor del comentario. |

**Ejemplo de cuerpo de solicitud**

```json
{
  "CellName": "B2",
  "Comment": "Revisión necesaria",
  "Author": "Juan Pérez"
}
```

**Ejemplo de respuesta correcta** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "Juan Pérez",
    "HtmlComment": "Revisión necesaria",
    "Note": "Revisión necesaria"
  }
}
```

**Códigos de error comunes**

| Código | Significado |
|--------|-------------|
| 400    | Dirección de celda inválida o cuerpo de solicitud incorrecto |
| 401    | No autorizado – token ausente o inválido |
| 404    | Libro o hoja de cálculo no encontrados |

**Obtener comentarios**

Recuperar todos los comentarios de una hoja de cálculo:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Parámetros de ruta**

| Parámetro | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| `file`    | string | Sí          | Nombre del archivo del libro. |
| `sheet`   | string | Sí          | Nombre de la hoja de cálculo. |

**Ejemplo de respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Ana",
      "HtmlComment": "Valor inicial",
      "Note": "Valor inicial"
    },
    {
      "CellName": "B2",
      "Author": "Juan Pérez",
      "HtmlComment": "Revisión necesaria",
      "Note": "Revisión necesaria"
    }
  ]
}
```

**Actualizar un comentario**

Para modificar un comentario existente, envíe una solicitud **PUT**. El comentario se identifica mediante su **índice** en la colección de comentarios de la hoja de cálculo (comenzando en 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Parámetros de ruta**

| Parámetro      | Tipo   | Obligatorio | Descripción |
|----------------|--------|-------------|-------------|
| `file`         | string | Sí          | Nombre del archivo del libro. |
| `sheet`        | string | Sí          | Nombre de la hoja de cálculo. |
| `commentIndex` | int    | Sí          | Índice de base cero del comentario que se va a actualizar. |

**Esquema del cuerpo de la solicitud**

| Campo    | Tipo   | Obligatorio | Descripción |
|----------|--------|-------------|-------------|
| `Comment`| string | Sí          | Nuevo texto del comentario. |
| `Author` | string | No          | Nombre del autor actualizado (opcional). |

**Ejemplo de cuerpo de solicitud**

```json
{
  "Comment": "Texto de nota actualizado",
  "Author": "Juan Pérez"
}
```

La respuesta sigue la misma estructura que la respuesta de **Agregar un comentario**.

**Eliminar un comentario**

Eliminar un único comentario mediante su índice:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Parámetros de ruta**

| Parámetro      | Tipo   | Obligatorio | Descripción |
|----------------|--------|-------------|-------------|
| `file`         | string | Sí          | Nombre del archivo del libro. |
| `sheet`        | string | Sí          | Nombre de la hoja de cálculo. |
| `commentIndex` | int    | Sí          | Índice de base cero del comentario que se va a eliminar. |

Una eliminación correcta devuelve:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Eliminar todos los comentarios**

Para borrar todos los comentarios de una hoja de cálculo:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Parámetros de ruta**

| Parámetro | Tipo   | Obligatorio | Descripción |
|-----------|--------|-------------|-------------|
| `file`    | string | Sí          | Nombre del archivo del libro. |
| `sheet`   | string | Sí          | Nombre de la hoja de cálculo. |

**Guía de manejo de errores**

- **404 Not Found (No encontrado)** – Verifique que el ID del libro, el nombre de la hoja de cálculo y el índice del comentario sean correctos.  
- **400 Bad Request (Solicitud incorrecta)** – Verifique la sintaxis JSON y los campos obligatorios (`CellName`, `Comment`).  
- **429 Too Many Requests (Demasiadas solicitudes)** – Implemente un retraso exponencial y respete el encabezado `Retry-After`.

**Resumen**

- Los comentarios de Excel se utilizan para [agregar una nota o explicar una fórmula en una celda](/es/cells/comments/add/).  
- Excel proporciona a los usuarios la flexibilidad de [editar](/es/cells/comments/update/), [eliminar](/es/cells/comments/delete/) y [mostrar](/es/cells/comments/get/) u [ocultar](/es/cells/comments/update/) comentarios en una hoja de cálculo.  
- Los usuarios también pueden [redimensionar](/es/cells/comments/update/) y [mover](/es/cells/comments/update/) el cuadro de comentario.  

Para obtener más información sobre el trabajo con otros elementos de hojas de cálculo, consulte la guía sobre [trabajar con celdas](/es/cells/working-with-cells/).