---
title: "Aspose.Cells Cloud Web API: Convertir datos locales de rango de Excel a archivo JSON - Herramienta gratuita en línea"
second_title: "Documentación"
ArticleTitle: "Cómo convertir datos de rango de hoja de cálculo local a archivo JSON: Guía paso a paso"
linktitle: "Convertir rango a JSON"
type: docs
url: /es/convert-range-to-json/
keywords: "convertir rango a json, Aspose.Cells Cloud, Excel a JSON, conversión de hojas de cálculo, API"
description: "Convierta un rango específico de una hoja de cálculo local de Excel a JSON utilizando la API de Aspose.Cells Cloud."
weight: 100
---

Exportar datos de rango desde un archivo local de Excel a un archivo JSON mediante la API en la nube.

## **API para convertir rango a JSON**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/json
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ruta / Cadena de consulta / Cuerpo HTTP | Descripción                                                                 |
| -------------------- | ------ | --------------------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet          | File   | FormData                                | Subir el archivo de hoja de cálculo.                                        |
| worksheet            | String | Query                                   | Nombre de la hoja de cálculo dentro del archivo.                            |
| range                | String | Query                                   | Área de celdas a convertir, por ejemplo, A1:C10.                            |
| outPath              | String | Query                                   | (Opcional) Ruta de carpeta donde se almacena el libro; el valor predeterminado es null. |
| outStorageName       | String | Query                                   | Nombre del almacenamiento de salida del archivo.                            |
| fontsLocation        | String | Query                                   | Ubicación para almacenar fuentes personalizadas para uso local.              |
| region               | String | Query                                   | Configuración de región de la hoja de cálculo.                              |
| password             | String | Query                                   | Contraseña para abrir el archivo de hoja de cálculo.                         |

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

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Petición incorrecta     | Parámetros faltantes o no válidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                   |
| 413    | Carga demasiado grande   | El archivo subido supera el límite de tamaño.                  |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

## **¿Dónde debería utilizar la API para convertir rango a JSON?**

- **Dashboards en tiempo real**: Convertir datos de Excel en vivo a JSON para librerías de gráficos como Chart.js o D3.js.
- **Hoja de cálculo como servicio (Spreadsheet-as-a-Service)**: Exponer rangos de Excel como puntos finales JSON para otros servicios.
- **Cargas útiles de webhook**: Transformar datos de hojas de cálculo a JSON para notificaciones mediante webhook.
- **Prototipado rápido de datos**: Convertir rápidamente datos limpiados de Excel a JSON para análisis en Python o R.
- **Tuberías de aprendizaje automático**: Preprocesar datos de entrenamiento procedentes de hojas de cálculo mantenidas por negocios.
- **Operaciones de comercio electrónico**: Sincronizar catálogos de productos o hojas de precios con sitios web mediante JSON.
- **Automatización de reportes**: Generar fuentes de datos JSON a partir de modelos financieros para reportes automatizados.
- **Configuración de aplicaciones**: Gestionar *feature flags*, ajustes o parámetros de pruebas A/B en Excel → JSON.
- **Soporte multilenguaje**: Convertir hojas de cálculo de localización a JSON para librerías i18n.
- **Menús/navegación dinámicos**: Almacenar estructuras de navegación de sitios web en Excel y desplegarlas como JSON.

_Para otras opciones de conversión, consulte la guía [Convertir rango a CSV](/convert-range-to-csv/)._

## ¿Por qué debería utilizar la API para convertir rango a JSON?

- **Soporte de SDK**: Aspose.Cells Cloud proporciona bibliotecas para múltiples lenguajes, reduciendo la cantidad de código personalizado necesario.
- **Reducción de costos de almacenamiento**: El rango puede convertirse sin subir primero el libro completo, ahorrando espacio de almacenamiento.
- **Compatibilidad con aplicaciones web y móviles**: JSON es el formato de datos nativo para frameworks modernos de JavaScript como React, Vue y Angular.
- **Amplio soporte de lenguajes**: Casi todos los lenguajes de programación y bases de datos pueden consumir JSON.
- **Preservación de datos estructurados**
  - **Detección inteligente de estructura**: Convierte automáticamente datos tabulares en arrays u objetos JSON adecuados.
  - **Mapeo de encabezados**: Utiliza la primera fila como claves JSON para estructuras de objetos limpias.
  - **Conservación de tipos de datos**: Preserva tipos numérico, fecha y booleano en lugar de texto plano.

## ¿Cómo utilizar la API para convertir rango a JSON con SDK?

### Especificación de la API para convertir rango a JSON

La [Especificación de la API para convertir rango a JSON](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToJson) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube con cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Solicitud" tabName12="Respuesta" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/json?worksheet=Sheet1&range=A1:C10" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@/ruta/a/su/archivo.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.json"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDK de Aspose.Cells Cloud

Utilizar los SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole convertir un rango de datos a un archivo JSON con código conciso.  
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:
{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToJson.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToJson.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToJson.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToJson.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToJson.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToJson.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToJson.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToJson.go" >}}
{{</tab>}}
{{< /tabs >}}