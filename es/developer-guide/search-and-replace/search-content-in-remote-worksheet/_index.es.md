---
title: "Aspose.Cells Cloud Excel Text Search Web API – Buscar texto en hoja de cálculo remota"
second_title: "Documento"
ArticleTitle: "Buscar texto en hoja de cálculo Excel remota – Encontrar datos específicos"
linktitle: "Buscar contenido en hoja de cálculo remota"
type: docs
url: /search-content-in-remote-worksheet/
keywords: "Aspose Cells, Excel API, búsqueda de texto, hoja de cálculo remota"
description: "Busque texto, números o fórmulas en una hoja de cálculo Excel remota mediante la API de Aspose.Cells Cloud. Admite archivos que no distinguen mayúsculas de minúsculas y archivos protegidos con contraseña."
weight: 100
---

## **Buscar contenido en hoja de cálculo remota**

Busque texto específico dentro de cualquier hoja de cálculo Excel mediante la API de Aspose.Cells Cloud. El servicio puede localizar texto, números o fórmulas en archivos remotos almacenados en almacenamiento en la nube, permitiendo automatizar flujos de trabajo de descubrimiento de datos, análisis de contenido y auditoría de hojas de cálculo.

### **API web**

```curl
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/content
```

### **Seguridad y autenticación**

Las APIs de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo    | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                       |
| --------------------- | ------- | --------------------------------------- | ------------------------------------------------------------------------------------------------- |
| name                  | String  | Ruta                                    | **Obligatorio.** El nombre del archivo del libro de trabajo objetivo (por ejemplo, `annual_report.xlsx`). |
| worksheet             | String  | Ruta                                    | **Obligatorio.** La hoja de cálculo dentro del libro de trabajo donde se realiza la búsqueda.    |
| searchText            | String  | Cadena de consulta                      | **Obligatorio.** La cadena exacta de texto o número que se desea localizar.                       |
| ignoreCase            | Boolean | Cadena de consulta                      | **Opcional.** Cuando es `true`, la búsqueda no distingue mayúsculas de minúsculas. El valor predeterminado es `false`. |
| folder                | String  | Cadena de consulta                      | **Opcional.** Ruta de la carpeta que contiene el libro de trabajo. Si se omite, se usa la carpeta raíz. |
| storageName           | String  | Cadena de consulta                      | **Opcional.** Nombre de un almacenamiento en la nube configurado personalmente. Si se omite, se usa el almacenamiento predeterminado. |
| region                | String  | Cadena de consulta                      | **Opcional.** Configuración regional (por ejemplo, `es-ES`) que podría afectar la comparación de texto. |
| password              | String  | Cadena de consulta                      | **Opcional.** Contraseña para un libro de trabajo protegido. Omítala si el archivo no está cifrado. |

### **Respuesta**

```json
{
  "textItems": [
    {
      "cellName": "A1",
      "text": "Total",
      "occurrences": 1
    },
    {
      "cellName": "B5",
      "text": "Total",
      "occurrences": 2
    }
  ],
  "code": 200,
  "status": "OK"
}
```

- **textItems** – Matriz de coincidencias. Cada elemento contiene la dirección de la celda (`cellName`), la cadena encontrada (`text`) y el número de veces que aparece en esa celda (`occurrences`).
- **code** – Código de estado HTTP devuelto por el servicio.
- **status** – Descripción textual del resultado.

### **Códigos de error**

- **400 Bad Request** – URI de API no válido o parámetros mal formados.
- **401 Unauthorized** – Token OAuth 2.0 faltante o no válido.
- **404 Not Found** – No se puede localizar el libro de trabajo ni la hoja de cálculo.
- **500 Server Error** – Se produjo una condición inesperada durante el procesamiento de la solicitud.

## ¿Dónde debemos utilizar la función Buscar contenido dentro de la hoja de cálculo de la API de hojas de cálculo?

- **Auditoría de cumplimiento del libro de trabajo:** Localice rápidamente términos confidenciales (por ejemplo, "Confidencial") en todo el archivo.
- **Asociación de datos entre hojas:** Encuentre un número de proyecto o nombre de cliente que aparezca en varias hojas.
- **Verificación de plantillas:** Tras generar informes, confirme que los marcadores de posición, como `{{Date}}`, han sido reemplazados.
- **Minado de datos históricos:** Busque códigos de eventos específicos en hojas de cálculo antiguas para comprender la lógica empresarial pasada.

## ¿Por qué debería utilizar la función Buscar contenido dentro de la hoja de cálculo de la API de hojas de cálculo?

- **Amigable para desarrolladores:** Los SDK para múltiples lenguajes aceleran el desarrollo y están completamente documentados.
- **Reducción de costos laborales:** Disminuye la necesidad de personal dedicado a la consolidación manual de datos.
- **Pago por uso:** Solo paga por las llamadas a la API que realmente realiza.
- **Cero mantenimiento:** No hay servidores que gestionar, actualizaciones de software ni preocupaciones por compatibilidad.
- **Preserva el formato complejo de Excel** al exportar resultados a PDF u otros formatos.

## Cómo utilizar la función Buscar enlaces rotos dentro de la hoja de cálculo de la API de hojas de cálculo mediante SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchContentInRemoteWorksheet) define una interfaz de programación accesible públicamente y permite interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor forma de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar fácilmente la búsqueda de contenido dentro de la hoja de cálculo de los libros de cálculo con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.
---