---
title: "Aspose.Cells Cloud – Cambiar la capitalización de palabras (Mayúsculas, minúsculas, Inicial Mayúscula, Oración)"
ArticleTitle: "Convertidor de mayúsculas y minúsculas para Excel – Mayúsculas, minúsculas, Inicial Mayúscula y Oración"
linktitle: "Capitalización de palabras"
type: docs
url: /es/change-word-case/
keywords: "API para cambiar la capitalización de palabras, Aspose.Cells, conversión de mayúsculas y minúsculas en Excel, mayúsculas, minúsculas, inicial mayúscula, oración, formato de texto"
description: "Convierta fácilmente la capitalización del texto en archivos de Excel utilizando la API de Aspose.Cells Cloud. Admite Mayúsculas, Minúsculas, Inicial Mayúscula y Oración. Incluye ejemplos de código en C#, Java, Python y más."
weight: 100
---

## **Cambiar la capitalización de palabras**

Utilice la API web de Aspose.Cells Cloud para convertir instantáneamente la capitalización del texto en su hoja de cálculo: cambie entre mayúsculas, minúsculas, inicial mayúscula (capitalizar cada palabra) u oración (capitalizar la primera letra de cada oración) en un rango seleccionado. Solo se ven afectadas las celdas que contienen cadenas; los números, valores booleanos, errores y celdas vacías se ignoran. Las fórmulas, el formato y la validación de datos permanecen intactos.

- **UpperCase (Mayúsculas)** – todos los caracteres se convierten a mayúsculas.
- **LowerCase (Minúsculas)** – todos los caracteres se convierten a minúsculas.
- **ProperCase (Inicial Mayúscula)** – la primera letra de cada palabra se convierte a mayúscula y el resto a minúsculas.
- **SentenceCase (Oración)** – la primera letra de cada oración se convierte a mayúscula y el resto a minúsculas.

<img src="images/result.png" alt="Captura de pantalla antes y después de la conversión de mayúsculas y minúsculas" width="800" height="450" />

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/content/wordcase
```


### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación mediante token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```
### Parámetros de solicitud para la API **UpdateWordCase**

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                           |
| :------------- | :----- | :------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| spreadsheet    | File   | FormData | El archivo de hoja de cálculo que se procesará. Los formatos admitidos incluyen XLSX, XLS, ODS, CSV, etc.                                                             |
| wordCaseType   | String | Query    | Especifica el tipo de conversión de mayúsculas y minúsculas: `UpperCase`, `LowerCase`, `ProperCase` o `SentenceCase`.                                                   |
| worksheet      | String | Query    | _(Opcional)_ El nombre de la hoja de cálculo en la que se aplicará la conversión de mayúsculas y minúsculas. Si se omite, la operación se aplica a la primera hoja del libro.               |
| range          | String | Query    | _(Opcional)_ El rango de celdas en el que se aplicará la conversión de mayúsculas y minúsculas (por ejemplo, `"A1:C10"`). Si se omite, la operación se aplica a todas las celdas utilizadas en la hoja especificada. |
| outPath        | String | Query    | _(Opcional)_ La ruta de la carpeta en el almacenamiento en la nube donde se guardará el libro procesado. Si se omite, el archivo se guarda en la carpeta de origen.                            |
| outStorageName | String | Query    | El nombre del almacenamiento en la nube donde se guardará el archivo de salida.                                                                                                   |
| region         | String | Query    | _(Opcional)_ Establece la configuración regional para las reglas de conversión de mayúsculas y minúsculas, especialmente relevante para la capitalización específica del idioma (por ejemplo, `"en-US"`, `"tr-TR"`).                 |
| password       | String | Query    | _(Opcional)_ Si la hoja de cálculo cargada está protegida con contraseña, proporcione la contraseña para abrir y procesar el archivo.                                                    |

### Respuesta

En caso de éxito, el servicio devuelve **200 OK** (o **202 Accepted**) junto con una carga útil JSON que contiene el flujo binario del libro procesado.

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
- **401 Unauthorized** – Token de acceso inválido o credenciales de cliente incorrectas.
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.
- **500 Server Error** – Se produjo una anomalia interna durante el procesamiento de la hoja de cálculo.

## ¿Dónde se debe utilizar la API para cambiar la capitalización de palabras?

### Limpieza y estandarización de datos

- **Gestión de datos de clientes** – Estandarizar la capitalización de nombres y direcciones de clientes (por ejemplo, `john doe` → `John Doe`).
- **Procesamiento de catálogos de productos** – Estandarizar títulos y descripciones de productos (por ejemplo, `IPHONE 15 PRO` → `iPhone 15 Pro`).
- **Generación de informes financieros** – Normalizar nombres de conceptos y campos descriptivos en estados financieros.

### Integración de datos de múltiples fuentes

- **ETL en almacenes de datos** – Estandarizar el formato del texto al cargar datos desde diversos sistemas.
- **Recepción de datos mediante API** – Manejar datos con capitalización inconsistente devueltos por APIs externas.
- **Fusión de datos entre departamentos** – Estandarizar el formato del texto en informes de Excel de distintos departamentos.

### Sistema de gestión de contenido

- **Difusión automática de comunicados de prensa** – Formatear automáticamente titulares y contenido (reglas de capitalización para títulos).
- **Generación de documentación de productos** – Garantizar la coherencia en el formato de términos técnicos en documentación.
- **Mantenimiento de base de conocimientos** – Estandarizar el formato del texto en preguntas frecuentes y documentos de ayuda.

### Integración de aplicaciones empresariales

- **Integración con sistemas CRM** – Formatear automáticamente nombres y datos de empresas durante la importación/exportación de información de clientes.
- **Procesamiento de datos ERP** – Estandarizar campos clave como descripciones de materiales y nombres de proveedores.
- **Sistema de gestión de recursos humanos** – Estandarizar información de empleados y títulos de puestos.

### Procesamiento por lotes de documentos

- **Preparación de documentos legales** – Procesamiento por lotes de formatos de cláusulas en contratos y acuerdos.
- **Generación de materiales de marketing** – Estandarizar formatos de textos publicitarios y plantillas de correos electrónicos.
- **Formato de artículos académicos** – Estandarizar requisitos de formato para referencias y títulos.

### Procesamiento en tiempo real

- **Validación de entradas de usuario** – Formatear en tiempo real los datos de formularios enviados por usuarios.
- **Respuestas de chatbots** – Estandarizar el formato del texto en respuestas generadas automáticamente.
- **Generación instantánea de informes** – Crear dinámicamente informes comerciales con formato uniforme.

### Internacionalización y localización

- **Procesamiento de datos multilingües** – Manejar diferencias en las reglas de capitalización para textos en distintos idiomas.
- **Preparación de contenido localizado** – Preparar contenido localizado formateado para distintas regiones.
- **Gestión de proyectos de traducción** – Garantizar la coherencia del formato del texto antes y después de la traducción.

## ¿Por qué debería utilizar la API para cambiar la capitalización de palabras?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido y cuenta con documentación completa. En comparación con la creación de soluciones personalizadas, esto reduce significativamente la carga de trabajo de desarrollo.
- ** rentable** – Puede cambiar la capitalización de palabras sin necesidad de cargar previamente el libro, lo que ahorra espacio de almacenamiento y reduce costos.

## Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/TextProcessing/UpdateWordCase) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

### Utilice los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor manera de acelerar el desarrollo. El SDK maneja los detalles subyacentes, lo que le permite implementar simplemente **UpdateWordCase** para celdas con un código mínimo. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener la lista completa de SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_UpdateWordCase.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_UpdateWordCase.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_UpdateWordCase.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_UpdateWordCase.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_UpdateWordCase.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_UpdateWordCase.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_UpdateWordCase.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_UpdateWordCase.go" >}}
{{</tab>}}
{{< /tabs >}}
---