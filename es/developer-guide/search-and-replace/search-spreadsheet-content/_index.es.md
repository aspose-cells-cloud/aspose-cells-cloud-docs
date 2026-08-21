---
title: "Buscar contenido de hoja de cálculo – API de Aspose.Cells Cloud (Buscar texto en Excel)"
second_title: "Documentación"
ArticleTitle: "Buscar texto en hojas de cálculo de Excel locales – Encontrar datos específicos"
linktitle: "Buscar contenido de hoja de cálculo"
type: docs
url: /search-spreadsheet-content/
keywords: "Aspose.Cells, API de búsqueda en Excel, búsqueda de contenido en hojas de cálculo, API de hojas de cálculo en la nube, búsqueda de texto"
description: "Utilice la API de Aspose.Cells Cloud para buscar texto, números o fórmulas en archivos locales de Excel. Admite consultas que no distinguen mayúsculas de minúsculas, alcance a nivel de hoja de cálculo y autenticación segura."
weight: 100
---

## **API para buscar contenido de hoja de cálculo**

Busque programáticamente texto específico dentro de cualquier hoja de cálculo de Excel mediante la API de Aspose.Cells Cloud. La API puede localizar texto, números o fórmulas en archivos locales almacenados en la nube, lo que permite automatizar la detección de datos, el análisis de contenido y los flujos de trabajo de auditoría de hojas de cálculo.


### **API web**

```
PUT https://api.aspose.cloud/v4.0/cells/search/content
```

Si prefiere utilizar HTTP en bruto, el siguiente ejemplo con cURL muestra la misma solicitud:

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/content?searchText=Invoice&ignoringCase=true" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: multipart/form-data" \
     -F "spreadsheet=@/path/to/your/file.xlsx"
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Parámetro    | Tipo    | Ubicación | Descripción                                                                                     |
| ------------ | ------- | --------- | ----------------------------------------------------------------------------------------------- |
| spreadsheet  | Archivo | FormData  | El archivo de Excel que se va a buscar.                                                        |
| searchText   | Cadena  | Consulta  | El texto (o valor numérico) que se va a localizar en el libro.                                 |
| ignoringCase | Booleano | Consulta | Establezca en `true` para realizar una búsqueda que no distinga mayúsculas de minúsculas.       |
| worksheet    | Cadena  | Consulta  | Nombre de la hoja de cálculo para limitar la búsqueda. Si se omite, se examinan todas las hojas. |
| cellArea     | Cadena  | Consulta  | Rango en estilo A1 (por ejemplo, `A1:C10`) que restringe el área de búsqueda.                  |
| region       | Cadena  | Consulta  | Región geográfica del servicio (por ejemplo, `us-east-1`).                                     |
| password     | Cadena  | Consulta  | Contraseña necesaria para abrir un libro protegido.                                            |


### **Respuesta**

La API devuelve un objeto `SearchResult` que contiene una matriz de celdas coincidentes. Cada elemento proporciona el nombre de la hoja de cálculo, la dirección de la celda y el texto coincidente.

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

### Códigos de error

- **400 Solicitud incorrecta** – El URI o los parámetros de la solicitud no son válidos.
- **401 No autorizado** – Falta el token de acceso, es inválido o las credenciales del cliente son incorrectas.
- **404 No encontrado** – No se puede acceder a la hoja de cálculo especificada.
- **500 Error interno del servidor** – Se produjo un error inesperado del servidor al procesar el libro.

## ¿Dónde debemos utilizar la API para buscar contenido dentro de la hoja de cálculo?

- **Auditoría integral de cumplimiento del libro** – Escanee todo el libro para localizar términos confidenciales (por ejemplo, “Cláusula confidencial”, “Datos internos”) en verificaciones de seguridad de datos y cumplimiento.
- **Consulta de asociación de datos entre hojas** – Encuentre un número de proyecto o nombre de cliente que aparezca en varias hojas de cálculo, lo que facilita la integración rápida entre hojas.
- **Verificación por lotes del contenido de plantillas** – Después de generar informes, verifique que todos los marcadores de posición, como `{{Date}}`, se hayan reemplazado correctamente en un lote de archivos de Excel.
- **Archivado y minería de datos históricos** – Busque códigos de eventos específicos o términos comerciales en archivos antiguos de Excel para acelerar la arqueología y el análisis de datos.

## ¿Por qué debería utilizar la API para buscar contenido dentro de la hoja de cálculo?

- **Fácil de usar para desarrolladores** – SDK disponibles para muchos lenguajes, lo que reduce el esfuerzo de desarrollo en comparación con construir una solución personalizada.
- **Reducción de costos laborales** – Automatiza tareas que de otro modo requerirían inspección manual de hojas de cálculo.
- **Pago por uso** – Solo paga por las llamadas a la API que realmente realice.
- **Sin mantenimiento** – No hay servidores que gestionar, actualizaciones de software ni preocupaciones por compatibilidad.
- **Preserva formatos complejos** – Los resultados se pueden exportar a PDF conservando el diseño original de Excel.

## Cómo utilizar la búsqueda de enlaces rotos dentro de la API de hojas de cálculo con SDK

### Especificación OpenAPI

La [especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchControllor/SearchSpreadsheetContent) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar un SDK es la forma más rápida de integrar la funcionalidad de búsqueda. El SDK abstracte la capa HTTP, permitiéndole llamar a la API con un código mínimo. Consulte la lista completa de SDK en el [repositorio de GitHub](https://github.com/aspose-cells-cloud).

Los siguientes ejemplos de código muestran cómo invocar la operación Buscar contenido de hoja de cálculo con diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchTextInLocalFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchTextInLocalFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchTextInLocalFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchTextInLocalFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchTextInLocalFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchTextInLocalFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchTextInLocalFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchTextInLocalFile.go" >}}
{{</tab>}}
{{< /tabs >}}