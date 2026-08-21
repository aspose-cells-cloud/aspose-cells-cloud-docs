---
title: "Convertir Rango a CSV"
ArticleTitle: "Convertir Rango a CSV – Aspose.Cells Cloud API"
second_title: "Documento"
linktitle: "Convertir Rango a CSV"
type: docs
url: /es/cells/convert/range/csv
aliases: []
keywords: "convertir, csv, rango, Aspose.Cells"
description: "Convierte un rango de hoja de cálculo ubicado en un disco local a un archivo CSV."
weight: 1
---

## Conversión de Rango a CSV mediante Aspose.Cells Cloud Web Services

Esta operación lee un archivo de hoja de cálculo desde el sistema de archivos local, convierte un rango especificado al formato CSV y devuelve directamente el resultado convertido. Funciona completamente en el servidor en la nube, por lo que no se requiere carga intermedia hacia el almacenamiento en la nube. La API admite parámetros opcionales como fuentes personalizadas, ajuste automático de filas/columnas, configuraciones regionales y libros protegidos con contraseña.

### Punto de conexión de la API Web

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/csv
```

### **Seguridad y Autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### Parámetros de Solicitud

| Nombre del Parámetro | Tipo    | Ruta/Cadena de Consulta/Cuerpo HTTP | Descripción                                                                                                                            |
|----------------------|---------|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet          | Archivo | FormData                            | Cargar archivo de hoja de cálculo.                                                                                                     |
| worksheet            | Cadena  | Consulta                            | Nombre de la hoja de cálculo. **Obligatorio**.                                                                                         |
| range                | Cadena  | Consulta                            | Área de celdas, por ejemplo `A1:C10`. **Obligatorio**.                                                                                 |
| outPath              | Cadena  | Consulta                            | (Opcional) Ruta de carpeta donde se almacena el libro. El valor predeterminado es null.                                                |
| outStorageName       | Cadena  | Consulta                            | Nombre del Almacenamiento para el archivo de salida.                                                                                  |
| fontsLocation        | Cadena  | Consulta                            | Utilizar fuentes personalizadas.                                                                                                       |
| AutoRowsFit          | Booleano| Consulta                            | (Opcional) Ajusta automáticamente todas las filas en las hojas de cálculo.                                                            |
| AutoColumnsFit       | Booleano| Consulta                            | (Opcional) Ajusta automáticamente todas las columnas en las hojas de cálculo.                                                         |
| region               | Cadena  | Consulta                            | Configuración regional/idioma de la hoja de cálculo (por ejemplo, `es-ES`, `fr-FR`). Afecta el formato de números, análisis de fechas y comportamiento específico de la configuración regional. |
| password             | Cadena  | Consulta                            | Contraseña para abrir el archivo de hoja de cálculo.                                                                                  |

### Parámetro del Cuerpo de Solicitud

| Nombre del Parámetro | Tipo | Descripción |
| --------------------- | ---- | ----------- |
| None                  | N/A  | No hay parámetros en el cuerpo de la solicitud. |

### **Respuesta**

```json
{
  "ResponseFile": "flujo binario de archivo (contenido CSV)"
}
```

**Códigos de Estado de Respuesta**

| Código | Significado | Descripción |
|--------|-------------|-------------|
| 200    | Correcto    | El rango se convirtió correctamente y el archivo CSV se devuelve en el cuerpo de la respuesta. |
| 400    | Solicitud Incorrecta | URL inválida o parámetros obligatorios faltantes. |
| 401    | No Autorizado | La autenticación falló o no se proporcionaron credenciales. |
| 413    | Carga de Datos Demasiado Grande | El cuerpo de la solicitud excede el límite de tamaño permitido. |
| 500    | Error Interno del Servidor | La hoja de cálculo encontró una anomalia al obtener los datos de conversión. |

## Cómo Usar la Conversión de Rango a CSV con SDKs

### Especificación de Conversión de Rango a CSV

La [Especificación de la API Conversión de Rango a CSV](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToCsv) define una interfaz de programación accesible públicamente y le permite realizar interacciones REST directamente desde un navegador web.

Puede utilizar la herramienta de línea de comandos cURL para acceder fácilmente a los servicios web de Aspose.Cells. El siguiente ejemplo muestra cómo realizar llamadas a la API en la nube mediante cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Utilizar HTTPS para una conexión segura
curl -v "https://api.aspose.cloud/v4.0/cells/convert/range/csv?worksheet=Hoja1&range=A1:C10&outPath=carpetaSalida&outStorageName=MiAlmacenamiento&fontsLocation=/fuentes/personalizadas&AutoRowsFit=true&AutoColumnsFit=true&region=es-ES&password=MiContraseña" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <token jwt>" \
  -F 'Spreadsheet=@ejemplo.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "ResponseFile": "ContenidoCsvCodificadoEnBase64"
}
```

{{< /tab >}}

{{< /tabs >}}

### Utilizar los SDKs de Aspose Cells Cloud

Utilizar un SDK es la forma más rápida de acelerar el desarrollo. Un SDK abstracta los detalles de bajo nivel, permitiéndole centrarse en las tareas de su proyecto. Consulte el <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDKs de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo llamar a los servicios web de Aspose Cells Cloud mediante diversos SDKs:
`[TBD]`
---