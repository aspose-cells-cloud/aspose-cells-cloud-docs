---
title: "Aspose.Cells Cloud – API de detección de enlaces rotos en Excel – Escaneo y validación de enlaces de hojas de cálculo en hojas remotas"
second_title: "Documento"
ArticleTitle: "Buscar y corregir enlaces rotos en una hoja de cálculo de Excel remota – Comprobador de enlaces de hojas de cálculo en la nube"
linktype: "Search Broken Links in Remote Worksheet"
type: docs
url: /es/search-broken-links-in-remote-worksheet/
keywords: "Aspose Cells, enlaces rotos, API de Excel, hoja de cálculo en la nube, validación de enlaces"
description: "Detectar y corregir enlaces externos rotos en hojas de cálculo de Excel almacenadas en almacenamiento en la nube. Utilice la API de Aspose.Cells Cloud para escanear rangos, devolver detalles de enlaces y automatizar comprobaciones de calidad."
weight: 100
---

## **Búsqueda de enlaces rotos en hoja de cálculo remota mediante API**

Detecte automáticamente enlaces rotos en una hoja de cálculo de Excel almacenada en almacenamiento en la nube. Nuestra API escanea rangos especificados para localizar referencias externas rotas, fórmulas no válidas y fuentes de datos ausentes. Admite auditoría de hojas de cálculo remotas, comprobaciones automáticas de calidad e integración con proveedores de almacenamiento en la nube. API RESTful para automatización de flujos de trabajo empresariales.

### **API web**

```
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/search/broken-links
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                                                                                                                                                                                |
| :------------------- | :----- | :--------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name                 | String | Ruta                                     | **Obligatorio.** Nombre del archivo (con extensión) del libro de Excel en el que se buscarán enlaces rotos (por ejemplo, `Annual_Report.xlsx`).                                                                                         |
| worksheet            | String | Ruta                                     | **Obligatorio.** Nombre exacto de la hoja de cálculo donde se realizará el escaneo de enlaces (por ejemplo, `DataSheet1`).                                                                                                                |
| folder               | String | Consulta                                 | **Opcional.** Ruta del directorio dentro del almacenamiento en la nube donde se encuentra el libro objetivo. Si se omite, se utiliza la carpeta raíz.                                                                                      |
| storageName          | String | Consulta                                 | **Opcional.** Identificador del almacenamiento en la nube configurado personalmente. Si no se proporciona, la API utiliza el almacenamiento predeterminado de la cuenta.                                                                    |
| region               | String | Consulta                                 | **Opcional.** Configuración regional que se aplicará durante la búsqueda (por ejemplo, `fr-FR`). Esto puede influir en la interpretación de ciertas fórmulas o formatos regionales de datos. _Los códigos regionales admitidos incluyen `en-US`, `fr-FR`, `de-DE`, `es-ES`, etc._ |
| password             | String | Consulta                                 | **Opcional.** Contraseña de descifrado para una hoja de cálculo protegida con contraseña. Omitir si el archivo no está cifrado.                                                                                                            |

**Ejemplo de solicitud con cURL**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/Annual_Report.xlsx/worksheets/DataSheet1/search/broken-links?folder=Reports&storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/json"
```

### **Respuesta**

```json
{
  "Code": 200,
  "Status": "OK",
  "BrokenLinks": [
    {
      "Address": "='C:\\Data\\Source.xlsx'!A1",
      "ErrorCode": "404",
      "ErrorMessage": "Source file not found"
    }
  ]
}
```

El objeto de respuesta es del tipo **BrokenLinksResponse** y contiene:

- **BrokenLinks** – colección de elementos `BrokenLink`, cada uno describe la referencia problemática (dirección, código de error y mensaje).
- **Code** – código de estado numérico devuelto por el servicio.
- **Status** – descripción textual del resultado.

**Notas**: La API no pagina los resultados. Se pueden devolver hasta 10 000 enlaces rotos por solicitud. El límite de tasa es de 100 solicitudes por minuto por cuenta.

### Códigos de error

- **400 Bad Request** – URI de la API de Aspose.Cells Cloud inválido.
- **401 Unauthorized** – Token de acceso inválido o ausente.
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.
- **500 Server Error** – Se produjo una anomalía al obtener los datos de cálculo.

## ¿Dónde se debe utilizar la búsqueda de enlaces rotos en la hoja de cálculo mediante API?

- **Auditoría regular de grandes modelos financieros**: Antes de publicar informes mensuales o trimestrales, escanee automáticamente las áreas clave de cálculo (como `Dashboard!B5:K50`) que contienen numerosas referencias a datos externos, para garantizar que todos los enlaces apunten a archivos fuente válidos.
- **Integración de datos en fusiones y adquisiciones**: Al fusionar varios archivos de hojas de cálculo que representan unidades de negocio, escanee la hoja "Overview" tras el proceso de integración para identificar enlaces que hayan quedado rotos debido a cambios en las rutas de los archivos fuente o problemas de permisos.
- **Preparación de paquetes de datos para inversores**: Antes de finalizar los materiales de presentación que contienen gráficos y tablas vinculados a bases de datos externas o fuentes de datos de mercado, verifique la validez de todos los enlaces.

## ¿Por qué debería utilizar la búsqueda de enlaces rotos en la hoja de cálculo mediante API?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y viene acompañado de una documentación completa. En comparación con la construcción de soluciones personalizadas de representación de gráficos, esto reduce significativamente la carga de desarrollo.
- **Reducción de costos laborales**: Elimina la necesidad de personal dedicado a la consolidación manual de documentos y la verificación de enlaces.
- **Pago por uso**: Sin inversión inicial; solo se paga por las llamadas a la API que realmente se utilicen.
- **Costos cero de mantenimiento**: Sin servidores que mantener, sin actualizaciones de software y sin problemas de compatibilidad que gestionar.
- **Preserva el formato complejo de Excel** en formato PDF universalmente accesible.

## Cómo utilizar la búsqueda de enlaces rotos en la hoja de cálculo mediante API con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/ReplaceContentInRemoteWorksheet) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

El uso del SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar fácilmente la búsqueda de enlaces rotos en hojas de cálculo con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}