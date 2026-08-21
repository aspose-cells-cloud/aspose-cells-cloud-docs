---
title: "API Web de Aspose.Cells Cloud para eliminar caracteres – Eliminar caracteres personalizados y subcadenas de Excel (código corto en línea)"
second_title: "Documento"
ArticleTitle: "Limpiador de texto de Excel – Eliminar caracteres y subcadenas de un rango seleccionado"
linktitle: "Eliminar caracteres"
type: docs
url: /es/remove-characters/
keywords: "Aspose.Cells, eliminar caracteres, API de Excel, limpieza de texto, hoja de cálculo"
description: "Elimine caracteres personalizados, conjuntos de caracteres y subcadenas de celdas de Excel en un rango seleccionado. Elimine texto en posiciones específicas utilizando la API de Aspose.Cells para una limpieza precisa de datos."
weight: 100
---

Limpie datos de Excel eliminando caracteres personalizados, conjuntos de caracteres o subcadenas de un rango de celdas seleccionado. Elimine texto en posiciones específicas con la API de Aspose.Cells para un formateo preciso de datos.

## Introducción

Limpie y estandarice fácilmente sus datos de Excel eliminando caracteres específicos no deseados. Nuestra extensión ofrece múltiples métodos dirigidos para limpiar sus celdas:

- **Eliminar caracteres personalizados**  
  Elimine cualquier símbolo específico que defina. Simplemente ingrese cada carácter en el campo, y la extensión eliminará instantáneamente todas sus apariciones en las celdas seleccionadas. Ideal para eliminar delimitadores únicos, errores tipográficos u otros símbolos especiales.

- **Eliminar conjuntos de caracteres (limpieza en masa)**
  - **Caracteres no imprimibles** – Elimine caracteres invisibles que interfieren con el análisis y el formateo (saltos de línea, retorno de carro, tabulaciones y otros caracteres de control como ASCII 0‑31, 127, 129, 141, 143, 144, 157).
  - **Caracteres de texto (todas las letras)** – Aisle números y símbolos eliminando todas las letras (A‑Z, a‑z) del rango seleccionado.
  - **Caracteres numéricos (todos los dígitos)** – Extraiga texto puro eliminando todos los dígitos (0‑9), ideal para limpiar nombres de productos o descripciones textuales.
  - **Símbolos** – Elimine una amplia variedad de símbolos innecesarios, incluyendo símbolos matemáticos (por ejemplo, ±, √), geométricos (por ejemplo, ∆, °), técnicos, monetarios (por ejemplo, £, ¢) y símbolos similares a letras (por ejemplo, ™, ®, ©).
  - **Signos de puntuación** – Obtenga texto limpio y sin puntuación eliminando todos los signos de puntuación, como puntos, comas, comillas y guiones.

- **Eliminar una subcadena específica**  
  Vaya más allá de los caracteres individuales y elimine palabras completas o secuencias específicas de caracteres. Elimine fácilmente prefijos, sufijos comunes o cualquier frase redundante de sus conjuntos de datos.

**Versión 4.0 – Actualizado el 2024‑11‑15**

## API RemoveCharacters

### API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/remove/characters
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación           | Descripción                                                                                                                                                                                                                      |
| --------------------- | ------ | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Spreadsheet           | File   | FormData            | Archivo de hoja de cálculo que se procesará. Los formatos compatibles incluyen XLSX, XLS, ODS, CSV, etc.                                                                                                                        |
| removeTextMethod      | String | Query               | Especifica el método de eliminación de texto. Opciones: `None`, `RemoveCustomCharacter`, `RemoveCharacterSets`, `RemoveSubString`. El valor predeterminado es `None`.                                                        |
| characterSets         | String | Query               | Conjunto(s) predefinido(s) de caracteres a eliminar cuando se selecciona `RemoveCharacterSets`. Opciones: `NonPrintingCharacters`, `TextCharacters`, `NumericCharacters`, `Symbols`, `PunctuationMarks`. Se pueden combinar varios conjuntos separándolos por comas. |
| removeCustomValue     | String | Query               | Carácter(es) o subcadena(s) personalizada(s) a eliminar al usar `RemoveCustomCharacter` o `RemoveSubString`.                                                                                                                   |
| worksheet             | String | Query _(opcional)_  | Nombre de la hoja de cálculo donde se aplicará la eliminación de texto. **Si se omite, la API procesa la primera hoja del libro.**                                                                                             |
| range                 | String | Query _(opcional)_  | Rango de celdas donde se aplicará la eliminación de texto (por ejemplo, `"A1:C10"`). **Si se omite, la operación se aplica a todas las celdas utilizadas en la hoja especificada.**                                              |
| outPath               | String | Query _(opcional)_  | Ruta de carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen.                                                                               |
| outStorageName        | String | Query _(opcional)_  | Nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                                                                                   |
| region                | String | Query _(opcional)_  | Establece la configuración regional para las definiciones de conjuntos de caracteres (por ejemplo, `"en-US"`, `"ja-JP"`).                                                                                                       |
| password              | String | Query _(opcional)_  | Contraseña para un libro protegido, si es necesario.                                                                                                                                                                            |

### Respuesta

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

### Códigos de error

- **400 Bad Request** – URI inválido de la API de Aspose.Cells Cloud.
- **401 Unauthorized** – Token de acceso inválido, o ID de cliente y secreto incorrectos.
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.
- **500 Server Error** – El libro de cálculo encontró una anomalia al obtener los datos de cálculo.

## ¿Dónde debería usar la API Remove Characters?

- **Importación/Exportación de datos** – Limpiar CSV/datos importados eliminando caracteres invisibles y errores de formateo.
- **Gestión de bases de datos** – Estandarizar códigos de producto, IDs y nombres eliminando símbolos o signos de puntuación no deseados.
- **Análisis financiero** – Extraer números puros eliminando símbolos monetarios y caracteres de texto.
- **Procesamiento de texto** – Eliminar saltos de línea y tabulaciones para un análisis y reporte limpio de texto.
- **Gestión de inventario** – Limpiar nombres de productos eliminando prefijos o sufijos redundantes.

## ¿Por qué usar la API Remove Characters?

- **Ahorre tiempo** – Elimine múltiples tipos de caracteres en masa de inmediato, en lugar de limpiar manualmente.
- **Garantice precisión** – Elimine caracteres ocultos que causen errores en el análisis y problemas de formateo.
- **Estandardice datos** – Consiga formateo consistente en conjuntos de datos y sistemas.
- **Mejore el análisis** – Obtenga datos limpios y listos para análisis, aislando números o texto según sea necesario.
- **Corrija errores de importación** – Elimine caracteres problemáticos que rompan bases de datos y fórmulas.
- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa. Comparado con la creación de soluciones personalizadas, esto reduce significativamente la carga de desarrollo.
- **Rentable** – Elimine caracteres sin necesidad de cargar primero el libro, ahorrando espacio de almacenamiento y reduciendo costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/RemoveCharacters) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar los SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, permitiéndole implementar **Remove Characters** para celdas con código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RemoveCharactersWithFirstNCharacters.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RemoveCharactersWithFirstNCharacters.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RemoveCharactersWithFirstNCharacters.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RemoveCharactersWithFirstNCharacters.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RemoveCharactersWithFirstNCharacters.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RemoveCharactersWithFirstNCharacters.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RemoveCharactersWithFirstNCharacters.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RemoveCharactersWithFirstNCharacters.go" >}}
{{</tab>}}
{{< /tabs >}}