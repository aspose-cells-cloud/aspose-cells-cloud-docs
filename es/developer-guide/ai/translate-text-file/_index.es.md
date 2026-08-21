---
title: "Aspose.Cells Cloud Web API: Traduzca archivos de texto con conversión de idiomas impulsada por IA"
second title: "Documento"
ArticleTitle: "Cómo traducir archivos de texto utilizando la API de traducción de IA de Aspose.Cells Cloud"
linktype: "Traduzca archivo de texto"
type: docs
url: /es/translate-text-file/
keywords: "Aspose.Cells, API en la nube, traducción por IA, traducir archivo de texto, conversión multilingüe, REST PUT, código de idioma de destino, traducción con carga de archivos, traducción de texto sin formato, hojas de cálculo con IA"
description: "Aprenda a utilizar el punto de conexión AI TranslateTextFile de Aspose.Cells Cloud para convertir archivos de texto en cualquier idioma admitido. Admite tanto carga de archivos multipart como carga de texto sin formato, preserva el formato y devuelve un archivo traducido descargable."
weight: 100
---

El punto de conexión **TranslateTextFile** aprovecha los servicios de IA de Aspose.Cells Cloud para traducir el contenido de un archivo de texto a un idioma de destino especificado. Admite dos modos de operación: (1) **Modo de carga de archivos**: envíe un archivo de texto mediante multipart/form-data y reciba un archivo traducido; (2) **Modo de contenido directo**: envíe texto sin formato en el cuerpo de la solicitud y obtenga el texto traducido directamente. El servicio preserva los saltos de línea y el formato originales, agrega automáticamente el sufijo "\_translated" al nombre del archivo y devuelve el resultado como una secuencia descargable. Ideal para la traducción por lotes de documentos, su integración en flujos de trabajo multilingües o la traducción en tiempo real de contenido generado por usuarios.

## **API para traducir archivos de texto**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/translate/text-file
```

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                                                                                 |
| :------------------- | :----- | :-------- | :------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet          | Archivo | Obligatorio | FormData          | El archivo de texto de origen que se va a traducir. Debe ser un archivo de texto sin formato (.txt) o un formato de hoja de cálculo admitido. Ejemplo: cargue `document.txt` mediante el campo "file" de multipart/form-data. |
| targetLanguage       | Cadena | Obligatorio | Query             | Código de idioma ISO‑639‑1 del idioma deseado (por ejemplo, "es" para español, "fr" para francés, "de" para alemán). El código no distingue entre mayúsculas y minúsculas.                                     |
| region               | string | Opcional    | Query             | Identificador de región de la hoja de cálculo que influye en el formato específico de la configuración regional, como fechas, números y moneda. Valores comunes: "US", "EU", "CN". Si se omite, se utiliza la configuración de región original del libro. |
| password             | Cadena | Opcional    | Query             | Contraseña necesaria para abrir archivos de hoja de cálculo cifrados. No es necesaria para archivos de texto sin formato.                                                                                     |

### **Respuesta**

Respuesta correcta (200 OK)
Encabezados:
Content-Type: application/octet-stream // secuencia binaria del archivo traducido
Content-Disposition: attachment; filename="<nombre_original>\_translated.txt"
Content-Length: <tamaño en bytes>

Cuerpo: secuencia binaria que contiene el texto traducido, preservando los saltos de línea y el formato originales.

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                       |
| ------ | ----------------------- | ----------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene los detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o no válidos (por ejemplo, tipo de archivo no admitido).      |
| 401    | No autorizado           | Token JWT no válido o ausente.                                     |
| 413    | Carga demasiado grande   | El archivo cargado supera el límite de tamaño.                                 |
| 500    | Error interno del servidor | Error inesperado del servidor.                                          |

## ¿Dónde debemos utilizar la API para traducir archivos de texto?

- **Portales de documentación multilingües**: traduzca automáticamente manuales de usuario u archivos de ayuda cargados como documentos de texto, entregando versiones localizadas bajo demanda.
- **Sistemas de gestión de contenido (CMS)**: intégrelo en un flujo de trabajo de CMS para traducir publicaciones de blog o artículos antes de publicarlos para audiencias internacionales.
- **Tuberías de datos empresariales**: utilícelo en trabajos por lotes que procesen grandes volúmenes de informes CSV o TXT, convirtiéndolos al idioma de las oficinas regionales, al tiempo que se conserva el formato original.
- **Plataformas de atención al cliente**: traduzca tickets entrantes o registros de chat en texto sin formato en tiempo real para ayudar a los agentes de soporte que trabajan en distintos idiomas.

## ¿Por qué debería utilizar la API para traducir archivos de texto?

- **Precisión impulsada por IA**: aprovecha modelos avanzados de traducción neuronal para una salida natural y contextual.
- **Flexibilidad de entrada dual**: acepta tanto cargas de archivos como cargas útiles de texto sin formato, lo que simplifica la integración con diversas aplicaciones cliente.
- **Preservación del diseño original**: mantiene saltos de línea, sangrías y caracteres especiales, eliminando la necesidad de limpieza posterior.
- **Gestión de archivos sencilla**: devuelve un archivo listo para descargar con el sufijo "\_translated" generado automáticamente, reduciendo la complejidad del código del lado del cliente.

## Cómo utilizar la API para traducir archivos de texto con SDK

### Especificación de la API para traducir archivos de texto

La [especificación de la API para traducir archivos de texto](https://reference.aspose.cloud/cells/#/AIController/TranslateTextFile) proporciona una interfaz de programación públicamente accesible para realizar interacciones REST directamente desde un navegador web.

## SDK para API de Excel

### Utilice los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracta los detalles de bajo nivel, permitiéndole combinar una hoja de cálculo en otra mediante un código breve.
Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante varios SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_TranslateTextFile.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_TranslateTextFile.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_TranslateTextFile.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_TranslateTextFile.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_TranslateTextFile.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_TranslateTextFile.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_TranslateTextFile.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_TranslateTextFile.go" >}}
{{</tab>}}
{{< /tabs >}}

---