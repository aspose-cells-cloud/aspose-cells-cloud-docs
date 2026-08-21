---
title: "Aspose.Cells Cloud Replace Web API – Actualizar texto en hojas de cálculo remotas"
second_title: "Documentación"
ArticleTitle: "Sustitución masiva de texto en archivos Excel en la nube – API de buscar y reemplazar"
linktitle: "Reemplazar contenido en hoja de cálculo remota"
type: docs
url: /replace-content-in-remote-spreadsheet/
keywords: "Aspose.Cells Cloud, reemplazar contenido, hoja de cálculo remota, API de buscar y reemplazar, Excel en la nube, sustitución masiva de texto"
description: "Utilice la API de buscar y reemplazar de Aspose.Cells Cloud para actualizar masivamente el texto en libros de Excel alojados en la nube. Endpoint seguro mediante HTTPS, autenticación OAuth2 y ejemplos listos para usar de SDKs para una integración rápida."
weight: 100
---

Realice la sustitución masiva de texto en archivos Excel alojados en la nube. Busque y actualice eficientemente cadenas de texto específicas mediante la API de buscar y reemplazar de Aspose.Cells para hojas de cálculo en la nube.


## **Reemplazar contenido en la API de hoja de cálculo remota**

### **API web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/replace/content
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de la solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                        |
|----------------------|--------|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **name**             | Cadena | Ruta      | Nombre del archivo del libro almacenado en el almacenamiento en la nube que se va a modificar (por ejemplo, `"informe.xlsx"`).                                   |
| **searchText**       | Cadena | Consulta  | Cadena que se buscará en todo el libro. La búsqueda distingue entre mayúsculas y minúsculas y se aplica a todas las hojas de cálculo, salvo que se restringa mediante otros parámetros. |
| **replaceText**      | Cadena | Consulta  | Cadena que reemplazará todas las apariciones de `searchText`.                                                                                                     |
| **folder**           | Cadena | Consulta  | Ruta de la carpeta en el almacenamiento en la nube donde se encuentra el libro de origen (por ejemplo, `"/documents/quarterly/"`).                               |
| **storageName**      | Cadena | Consulta  | _(Opcional)_ Nombre de un almacenamiento en la nube personalizado (por ejemplo, `"MiS3Bucket"`). Si se omite, se utilizará el almacenamiento predeterminado configurado para la cuenta. |
| **region**           | Cadena | Consulta  | _(Opcional)_ Identificador regional que puede afectar la codificación de caracteres y el comportamiento de búsqueda específico del idioma (por ejemplo, `"es-ES"`). |
| **password**         | Cadena | Consulta  | _(Opcional)_ Contraseña para abrir un libro protegido.                                                                                                            |

### Respuesta

Una respuesta correcta típica devuelve el estado de la operación y el número de reemplazos realizados:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error

- **400 Bad Request (Solicitud incorrecta)** – URI inválido de la API de Aspose.Cells Cloud.
- **401 Unauthorized (No autorizado)** – Token de acceso OAuth 2.0 ausente o inválido.
- **404 Not Found (No encontrado)** – No se pudo acceder al archivo de hoja de cálculo especificado.
- **500 Server Error (Error del servidor)** – Se produjo un problema inesperado del lado del servidor al procesar la solicitud.

## ¿Cuándo debería utilizar la API de reemplazar contenido en hoja de cálculo remota?

- **Actualización por lotes de archivos en la nube** – Modifique el contenido de varios archivos Excel almacenados en almacenamientos en la nube como AWS S3 o Azure Blob.
- **Relleno dinámico de plantillas en la nube** – Rellene plantillas de informes alojadas en la nube con datos actualizados.
- **Sincronización de archivos entre regiones** – Mantenga la coherencia de los archivos Excel en diferentes regiones geográficas de almacenamiento.

## ¿Por qué debería utilizar la API de reemplazar contenido en hoja de cálculo remota?

- **Amigable para desarrolladores** – Aspose.Cells Cloud proporciona bibliotecas SDK para múltiples lenguajes de programación, reduciendo el esfuerzo de desarrollo frente a la creación de una solución personalizada.
- **Reducción de costos de mano de obra** – Elimina la necesidad de personal dedicado para consolidar documentos manualmente.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente realice.
- **Costos cero de mantenimiento** – Sin servidores que gestionar, sin actualizaciones de software y sin preocupaciones por compatibilidad.
- **Conservación de todo formato de celda, fórmulas y gráficos** – La operación conserva la disposición y los cálculos originales del libro tras la sustitución del texto.

## Cómo utilizar la API de reemplazar contenido en hoja de cálculo remota con SDKs

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteRange) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDKs de Aspose.Cells Cloud

Utilizar los SDKs es la mejor forma de acelerar el desarrollo. Los SDK gestionan los detalles subyacentes, permitiéndole implementar simplemente la sustitución de contenido en hojas de cálculo con un mínimo de código. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDKs:


---