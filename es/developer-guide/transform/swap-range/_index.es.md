---
title: "Aspose.Cells Cloud: Intercambiar columnas, filas y rangos (v4.0)"
second_title: "Documento"
ArticleTitle: "Intercambiar/exchange datos entre columnas, filas y celdas en Excel"
linktype: "Intercambiar rango"
type: docs
url: /swap-range/
keywords: "Aspose Cells, API de Excel, intercambiar rango, hoja de cálculo en la nube"
description: "Intercambia columnas, filas o rangos en archivos de Excel con la API de Aspose.Cells Cloud. Preserva el formato, las fórmulas y las referencias a celdas en una única solicitud."
weight: 100
---

Intercambia automáticamente datos entre cualquier par de columnas, filas, rangos o celdas en archivos de Excel utilizando la API de Aspose.Cells Cloud. La API de intercambio de rangos permite un intercambio preciso de datos, preservando todo el formato, las fórmulas y las referencias a celdas. Admite reorganizaciones complejas de datos, procesamiento por lotes e integración fluida en la nube para flujos de trabajo empresariales.

## **API de intercambio de rangos**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/swap/range
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Parámetros de solicitud**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                 |
|----------------------|--------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Spreadsheet**      | Archivo | FormData  | **Obligatorio.** Archivo de libro de Excel de origen (`.xlsx`, `.xls`).                                                                                     |
| **worksheet1**       | Cadena  | Query     | **Obligatorio.** Nombre de la hoja de cálculo que contiene la primera área de datos.                                                                        |
| **range1**           | Cadena  | Query     | **Obligatorio.** Rango de celdas (por ejemplo, `A1:D10`) en `worksheet1` que se va a intercambiar.                                                           |
| **worksheet2**       | Cadena  | Query     | **Obligatorio.** Nombre de la hoja de cálculo que contiene la segunda área de datos (puede ser la misma que `worksheet1`).                                   |
| **range2**           | Cadena  | Query     | **Obligatorio.** Rango de celdas (por ejemplo, `F1:I10`) en `worksheet2` que se va a intercambiar. **Importante:** `range1` y `range2` deben tener dimensiones idénticas. |
| **outPath**          | Cadena  | Query     | **Opcional.** Carpeta en el almacenamiento en la nube donde se guardará el libro modificado.                                                                |
| **outStorageName**   | Cadena  | Query     | **Obligatorio.** Nombre del servicio de almacenamiento en la nube configurado (por ejemplo, `MyCompanyStorage`).                                            |
| **region**           | Cadena  | Query     | **Opcional.** Configuración regional (por ejemplo, `es-ES`, `ja-JP`) que podría afectar al formato.                                                         |
| **password**         | Cadena  | Query     | **Opcional.** Contraseña para descifrar una hoja de cálculo protegida. Omítala si no está cifrada.                                                            |

**Solicitud de ejemplo (cURL)**  

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/swap/range?worksheet1=Sheet1&range1=A1:D10&worksheet2=Sheet2&range2=F1:I10&outStorageName=MyCompanyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/path/to/workbook.xlsx"
```

### **Respuesta**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**Notas:**  
- La API devuelve el libro modificado como flujo de archivos. Si se especifica `outPath`, el archivo también se guarda en la ubicación del almacenamiento en la nube indicada.  
- Una discrepancia en las dimensiones de los rangos provocará un error **400 Bad Request**.

### Códigos de error

| Código               | Descripción                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| **400 Bad Request**  | URI de solicitud inválida o dimensiones de rango no coincidentes.             |
| **401 Unauthorized** | Token de acceso inválido o caducado; el client-id o el secret no son correctos. |
| **404 Not Found**    | No se puede acceder al archivo de hoja de cálculo especificado.                |
| **500 Server Error** | Se produjo un error interno al procesar el libro.                             |

## ¿Dónde debemos usar la API de intercambio de rangos?

- **Reestructuración de modelos financieros**: Reorganiza bloques de datos (por ejemplo, mover la previsión del tercer trimestre al cuarto) manteniendo las fórmulas y el formato condicional.
- **Procesos de canalización de datos y ETL**: Intercambia rangos de datos crudos con rangos limpiados en una hoja de trabajo intermedia antes de generar el resultado final.
- **Corrección de errores y recuperación de datos**: Corrige rápidamente datos colocados incorrectamente sin necesidad de copiar y pegar manualmente.

## ¿Por qué usar la API de intercambio de rangos?

- **Fácil de usar para desarrolladores**: SDK disponibles para múltiples lenguajes, lo que reduce el esfuerzo de desarrollo frente a la creación de soluciones personalizadas.
- **Reducción de costos laborales**: Automatiza el reordenamiento de datos, disminuyendo la necesidad de consolidación manual.
- **Pago por uso**: Solo se paga por las llamadas a la API que realmente se realizan.
- **Sin mantenimiento**: No hay servidores que gestionar, ni actualizaciones de software ni preocupaciones por compatibilidad.

## Cómo usar la API de intercambio de rangos con SDK

### Especificación de la API de intercambio de rangos

La [especificación de la API de intercambio de rangos](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Transform/SwapRange) define una interfaz de programación accesible públicamente y permite realizar interacciones REST directamente desde un navegador web.

### Utilizar los SDK de Aspose.Cells Cloud

Usar un SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiendo intercambiar rangos con código conciso. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SwapRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SwapRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SwapRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SwapRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SwapRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SwapRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SwapRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SwapRange.go" >}}
{{</tab>}}
{{< /tabs >}}