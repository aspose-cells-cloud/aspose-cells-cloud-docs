---
title: "Buscar enlaces rotos en hojas de cálculo – Aspose.Cells Cloud API"
second_title: "Documentos"
ArticleTitle: "Encontrar y corregir enlaces rotos en Excel – Comprobador de enlaces en hojas de cálculo en la nube"
linktitle: "Buscar enlaces rotos en hojas de cálculo"
type: docs
url: /es/search-spreadsheet-broken-links/
keywords: "Aspose Cells, enlaces rotos, auditoría de hojas de cálculo, API de Excel, hoja de cálculo en la nube, comprobador de enlaces"
description: "Detectar y corregir enlaces rotos en libros de Excel mediante la API de Aspose.Cells Cloud. Escanear rangos, obtener resultados detallados en JSON e integrarse con cualquier SDK de lenguaje."
weight: 100
---

## **API para buscar enlaces rotos en hojas de cálculo**

Detecte automáticamente enlaces rotos en archivos de Excel. Nuestra API escanea rangos especificados en busca de referencias externas rotas, fórmulas no válidas y fuentes de datos ausentes. Admite auditoría remota de hojas de cálculo, comprobaciones automáticas de calidad e integración con proveedores de almacenamiento en la nube. API RESTful para automatización de flujos de trabajo empresariales.

**Resumen:** Utilice este extremo para identificar y reparar rápidamente enlaces no válidos en libros, garantizando la integridad de los datos en modelos financieros, conjuntos de datos para fusiones y adquisiciones y paquetes listos para inversores.

### **API web**

```bash
PUT https://api.aspose.cloud/v4.0/cells/search/broken-links
```

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/search/broken-links?worksheet=Hoja1" \
     -H "Authorization: Bearer {token_de_acceso}" \
     -F "Spreadsheet=@ejemplo.xlsx"
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {token_de_acceso}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación             | Descripción                                                                                                           |
| -------------------- | ------ | --------------------- | --------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | Archivo | FormData (multipart)  | **Obligatorio.** El archivo del libro de Excel (`.xlsx`, `.xls`, etc.) que se va a analizar.                         |
| worksheet            | Cadena  | Consulta              | **Opcional.** El nombre de la hoja de cálculo a analizar. Si se omite, se utiliza la primera hoja.                   |
| cellArea             | Cadena  | Consulta              | **Opcional.** Rango de celdas objetivo en notación A1 (por ejemplo, `B2:D10`). Si no se especifica, se analiza todo el rango utilizado. |
| region               | Cadena  | Consulta              | **Opcional.** Configuración regional (por ejemplo, `es‑ES`) que puede afectar la interpretación de fechas, números o monedas. |
| password             | Cadena  | Consulta              | **Opcional.** Contraseña para libros cifrados. Déjelo vacío si el archivo no está protegido.                          |

### Respuesta

```json
{
  "BrokenLinks": [
    {
      "CellName": "B5",
      "Link": "C:\\Data\\source.xlsx",
      "ErrorMessage": "Archivo no encontrado",
      "Status": "Roto"
    },
    {
      "CellName": "C12",
      "Link": "http://ejemplo.com/datos.csv",
      "ErrorMessage": "404 No encontrado",
      "Status": "Roto"
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

### Códigos de error

| Código | Descripción |
|--------|-------------|
| **400 Bad Request** | URI inválido de la API de Aspose.Cells Cloud. |
| **401 Unauthorized** | Token de acceso, ID de cliente o secreto de cliente inválido. |
| **404 Not Found** | El archivo de hoja de cálculo no es accesible. |
| **429 Too Many Requests** | Límite de tasa excedido (60 llamadas / minuto). |
| **500 Server Error** | El archivo de hoja de cálculo encontró una anomalia al obtener datos de cálculo. |


## ¿Dónde debemos utilizar la API de búsqueda de enlaces rotos en hojas de cálculo?

- **Auditoría regular de grandes modelos financieros**: Antes de publicar informes mensuales o trimestrales, escanee automáticamente las áreas clave de cálculo (por ejemplo, `Panel!B5:K50`) que contienen muchas referencias a datos externos para asegurarse de que todos los enlaces apunten a archivos de origen válidos.  
- **Integración de datos para fusiones y adquisiciones**: Al combinar varios archivos de hojas de cálculo que representan unidades empresariales, escanee la hoja "Resumen" tras la integración para identificar enlaces que se han vuelto inválidos debido a cambios en las rutas de archivo o problemas de permisos.  
- **Preparación de paquetes de datos para inversores**: Antes de finalizar materiales de presentación que contengan gráficos y tablas vinculados a bases de datos externas o fuentes de datos de mercado, verifique la validez de todos los enlaces.

## ¿Por qué debería utilizar la API de búsqueda de enlaces rotos en hojas de cálculo?

- **Amigable para desarrolladores**: Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación exhaustiva. Comparado con la creación de soluciones personalizadas, esto reduce significativamente la carga de trabajo de desarrollo.  
- **Reducción de costos laborales**: Elimina la necesidad de personal dedicado para verificar manualmente los enlaces de los documentos.  
- **Pago por uso**: Sin inversión inicial; solo paga por las llamadas a la API que realmente utiliza.  
- **Cero costos de mantenimiento**: No hay servidores que mantener, actualizaciones de software ni problemas de compatibilidad.  
- **Conserva el formato complejo de Excel**: Los resultados se devuelven en un formato JSON universalmente accesible, conservando al mismo tiempo el diseño original del libro.

## Cómo utilizar la API de búsqueda de enlaces rotos en hojas de cálculo con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/#/SearchController/SearchSpreadsheetBrokenLinks){:target="_blank" rel="noopener noreferrer"} define una interfaz de programación accesible públicamente, lo que le permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, permitiéndole implementar simplemente la funcionalidad de búsqueda de enlaces rotos con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud){:target="_blank" rel="noopener noreferrer"} para ver la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código ilustran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchSpreadsheetBrokenLinks.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchSpreadsheetBrokenLinks.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchSpreadsheetBrokenLinks.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchSpreadsheetBrokenLinks.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchSpreadsheetBrokenLinks.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchSpreadsheetBrokenLinks.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchSpreadsheetBrokenLinks.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchSpreadsheetBrokenLinks.go" >}}
{{</tab>}}
{{< /tabs >}}