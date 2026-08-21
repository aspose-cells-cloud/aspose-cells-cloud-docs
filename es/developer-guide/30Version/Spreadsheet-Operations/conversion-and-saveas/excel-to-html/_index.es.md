---
---
title: Convertir Excel a HTML  
description: Convierta un libro de Excel en un archivo HTML mediante la API de Aspose.Cells Cloud v3.0.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Convertir Excel a HTML  

Aspose.Cells Cloud proporciona un punto de conexión REST robusto que convierte un libro de Excel (XLS, XLSX, CSV, etc.) en un documento HTML. La operación devuelve un objeto **FileInfo** que contiene el archivo HTML generado (nombre, tamaño y contenido codificado en Base64).

---

## Requisitos previos

| Requisito | Cómo cumplirlo |
|-----------|----------------|
| **Cuenta de Aspose Cloud** | Regístrese en [aspose.cloud](https://www.aspose.cloud). |
| **Token de acceso JWT** | Obtenga un token bearer mediante el punto de conexión OAuth 2.0 `POST /connect/token`. |
| **Almacenamiento (opcional)** | Si desea que la API lea o escriba archivos en un almacenamiento específico, créelo primero (por ejemplo, Amazon S3, Azure Blob o el almacenamiento de Aspose Cloud). |
| **cURL / SDK** | Cualquier cliente HTTP capaz de manejar multipart/form-data (cURL, Postman o uno de los SDK de Aspose.Cells). |

---

## Autenticación

Todas las solicitudes a Aspose.Cells Cloud requieren **autenticación basada en token JWT**.

```http
Authorization: Bearer <access-token>
```

El token debe incluirse en el encabezado `Authorization` de cada solicitud.

---

## Punto de conexión

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Nota:** La solicitud debe enviarse como `multipart/form-data`. El archivo Excel constituye la primera parte del cuerpo multipart.

---

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

## Parámetros de solicitud  

### Parámetros de consulta  

| Nombre                     | Tipo    | Obligatorio | Valor predeterminado | Descripción |
|----------------------------|---------|-------------|----------------------|-------------|
| `password`                 | string  | No          | –                    | Contraseña para abrir un libro protegido. |
| `storageName`              | string  | No          | –                    | Nombre del almacenamiento donde reside el archivo de origen. |
| `checkExcelRestriction`   | boolean | No          | `true`               | Si es `true`, el servicio valida las restricciones específicas de Excel (por ejemplo, hojas protegidas). |
| `region`                   | string  | No          | –                    | Configuración regional para el libro (por ejemplo, `es-ES`). |
| `FontsLocation`            | string  | No          | –                    | URL o ruta a una carpeta que contiene las fuentes personalizadas necesarias para la representación. |

### Datos de formulario (multipart)  

| Nombre | Tipo | Obligatorio | Descripción |
|--------|------|-------------|-------------|
| **File** | archivo | **Sí** | El libro de Excel que se va a convertir. Debe proporcionarse como la primera parte de la solicitud multipart. |

---

## Ejemplo de solicitud (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <access-token>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/ruta/a/su_libro.xlsx"
```

---

## Respuesta correcta  

**Código de estado:** `200 OK`

| Campo        | Tipo   | Descripción |
|--------------|--------|-------------|
| `Filename`   | string | Nombre del archivo HTML generado (por ejemplo, `ejemplo.html`). |
| `FileSize`   | int    | Tamaño del archivo HTML en bytes. |
| `FileContent`| string | Contenido HTML codificado en Base64. |

```json
{
  "Filename": "ejemplo.html",
  "FileSize": 12345,
  "FileContent": "cadena_codificada_en_base64"
}
```

El esquema de respuesta lo define el modelo **FileInfo**: [/cells/file-info](/cells/file-info/).

---

## Respuestas de error  

| Código | Significado                        | Ejemplo de carga útil |
|--------|------------------------------------|------------------------|
| `400`  | Solicitud incorrecta: parámetros faltantes o no válidos | ```json { "Code": "BadRequest", "Message": "La parte 'File' es obligatoria." } ``` |
| `401`  | No autorizado: token JWT inválido o faltante | ```json { "Code": "InvalidToken", "Message": "El token de acceso falta o ha caducado." } ``` |
| `404`  | No encontrado: archivo de origen no hallado en el almacenamiento especificado | ```json { "Code": "FileNotFound", "Message": "El archivo 'mi.xlsx' no existe en el almacenamiento 'MiAlmacenamiento'." } ``` |
| `413`  | Carga útil demasiado grande: el archivo cargado excede el tamaño permitido | ```json { "Code": "RequestEntityTooLarge", "Message": "El archivo cargado supera el límite de 100 MB." } ``` |
| `429`  | Demasiadas solicitudes: se ha superado el límite de tasa | ```json { "Code": "TooManyRequests", "Message": "Se ha superado el límite de tasa de 60 llamadas por minuto." } ``` |
| `500`  | Error interno del servidor: condición inesperada | ```json { "Code": "InternalError", "Message": "Se produjo un error inesperado. Inténtelo de nuevo más tarde." } ``` |

---

## Límites de tasa  

| Límite | Descripción |
|--------|-------------|
| **60 solicitudes por minuto** por cuenta (predeterminado) | Superar este límite devuelve `429 Too Many Requests`. Ajuste la lógica del cliente o solicite una cuota superior a través del portal de Aspose Cloud. |

---

## Soporte de SDK

Aspose ofrece SDK de primera clase que envuelven este punto de conexión para varios lenguajes. Los ejemplos siguientes muestran la misma conversión utilizando los SDK oficiales.

| Idioma | Ejemplo |
|--------|---------|
| C#     | <details><summary>Ver ejemplo</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java   | <details><summary>Ver ejemplo</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python | <details><summary>Ver ejemplo</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js| <details><summary>Ver ejemplo</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go     | <details><summary>Ver ejemplo</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP    | <details><summary>Ver ejemplo</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby   | <details><summary>Ver ejemplo</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl   | <details><summary>Ver ejemplo</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Para obtener la lista completa de SDK admitidos y las instrucciones de instalación, consulte el repositorio **Aspose.Cells Cloud SDKs**: <https://github.com/aspose-cells-cloud>.

---

## Puntos de conexión relacionados  

| Punto de conexión | Descripción |
|-------------------|-------------|
| `POST /cells/{name}/saveAs` | Guarda un archivo de Excel existente como HTML (u otros formatos) directamente en almacenamiento. |
| `PUT /cells/convert` | Convierte un libro en HTML con opciones adicionales de conversión; el resultado se devuelve en el cuerpo de la respuesta. |
| `GET /cells/{name}` | Recupera un libro ya almacenado como HTML (u otros formatos), con parámetros de consulta opcionales. |

---

## Preguntas frecuentes  

**P:** *¿Cómo me autentico al llamar a la API de conversión de Excel a HTML?*  
**R:** Incluya el encabezado `Authorization: Bearer <access-token>`, obtenido del punto de conexión OAuth 2.0 `/connect/token`.

**P:** *¿Qué contiene la respuesta `FileInfo`?*  
**R:** Tres campos: `Filename` (cadena), `FileSize` (entero, en bytes) y `FileContent` (contenido HTML codificado en Base64).

**P:** *¿Qué códigos de error podría encontrar?*  
**R:** `400` (Solicitud incorrecta), `401` (No autorizado), `404` (Archivo no encontrado), `413` (Carga útil demasiado grande), `429` (Demasiadas solicitudes), `500` (Error interno del servidor). Cada uno devuelve una carga útil JSON con `Code` y `Message`.

**P:** *¿Puedo especificar una ubicación personalizada para las fuentes?*  
**R:** Sí. Utilice el parámetro de consulta `FontsLocation` para indicar una carpeta o URL que contenga las fuentes necesarias.

**P:** *¿Existe un límite de tasa para esta operación?*  
**R:** El límite predeterminado es de **60 llamadas por minuto** por cuenta. Superarlo devuelve `429 Too Many Requests`.

---

## Breadcrumb JSON‑LD (Datos estructurados)

Incluir este bloque mejora el SEO al permitir breadcrumbs en forma de fragmentos enriquecidos en los resultados de búsqueda.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Inicio", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Centro para desarrolladores", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Conversión", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel a HTML", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Registro de cambios  

| Versión | Fecha       | Cambios |
|---------|-------------|---------|
| **v3.0** | 2024‑10‑01 | Lanzamiento inicial público de `PostConvertWorkbookToHtml`. |
| **v3.1** | 2025‑04‑15 | Se agregaron los parámetros de consulta `region` y `FontsLocation`; se actualizó el formato de carga útil de error. |
| **v3.2** | 2026‑03‑20 | Se introdujeron documentación sobre límites de tasa y ejemplos de respuestas de error. |

---

*Para mayor ayuda, contacte con el soporte de Aspose o visite la referencia oficial de la API:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---