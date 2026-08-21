---
title: "Aspose.Cells Cloud – Detectar enlaces rotos en un rango de Excel (API)"
second_title: "Documento"
ArticleTitle: "Buscar y solucionar enlaces rotos en un rango remoto de Excel – Comprobador de enlaces de hojas de cálculo en la nube"
linktitle: "Buscar enlaces rotos en un rango remoto"
type: docs
url: /search-broken-links-in-remote-range/
keywords: "Aspose, Cells, enlaces rotos, API, rango de Excel, validación, nube, hoja de cálculo, referencia externa, comprobador"
description: "Utilice la API de Aspose.Cells Cloud para escanear un rango específico de Excel en busca de enlaces externos rotos, fórmulas no válidas o fuentes de datos ausentes. Segura, rápida y basada en la nube."
weight: 100
---

## **Buscar enlaces rotos en el rango remoto mediante la API**

Detecte automáticamente enlaces rotos en los datos de rango de archivos de Excel almacenados en el almacenamiento en la nube. Nuestra API escanea rangos especificados en busca de referencias externas rotas, fórmulas no válidas y fuentes de datos ausentes. Admite auditoría de hojas de cálculo remotas, comprobaciones automáticas de calidad e integración con proveedores de almacenamiento en la nube. API RESTful para automatización de flujos de trabajo empresariales.

### **API Web**

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/ranges/{cellArea}/search/broken-links
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### Parámetros de solicitud

| Nombre del parámetro | Tipo   | Ubicación | Descripción                                                                                                                                                           |
|----------------------|--------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                 | String | Ruta      | **Obligatorio.** El nombre del archivo de libro de Excel (por ejemplo, `informe_financiero.xlsx`) almacenado en el almacenamiento en la nube que desea escanear en busca de enlaces rotos. |
| worksheet            | String | Ruta      | **Obligatorio.** El nombre de la hoja de cálculo específica (por ejemplo, `Hoja1`, `Datos_Q4`) dentro del libro donde se debe realizar la búsqueda de enlaces rotos. |
| cellArea             | String | Ruta      | **Obligatorio.** La dirección del rango de celdas objetivo (por ejemplo, `A1:F100`) dentro de la hoja de cálculo especificada que se escaneará en busca de referencias externas rotas, fórmulas o enlaces. |
| folder               | String | Consulta  | **Opcional.** La ruta del directorio en su almacenamiento en la nube donde se encuentra el libro objetivo. Si se omite, se asume el directorio raíz.                 |
| storageName          | String | Consulta  | **Opcional.** El nombre del servicio de almacenamiento en la nube configurado (por ejemplo, `DropboxBusiness`, `S3Bucket`). Si no se especifica, la API utiliza el almacenamiento predeterminado de la cuenta. |
| region               | String | Consulta  | **Opcional.** La configuración regional (por ejemplo, `es-ES`, `en-GB`) para aplicar durante el escaneo en la interpretación de datos específicos de región.         |
| password             | String | Consulta  | **Opcional.** La contraseña de descifrado necesaria para acceder a un libro protegido por contraseña. Déjelo vacío si el archivo no está cifrado.                     |

**Ejemplo de cuerpo de solicitud**

```json
{
  "name": "informe_financiero.xlsx",
  "worksheet": "Hoja1",
  "cellArea": "A1:F100",
  "folder": "informes/2024",
  "storageName": "MiDropbox",
  "region": "es-ES",
  "password": ""
}
```

### Respuesta

```json
{
  "Name": "BrokenLinksResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "Properties": [
    {
      "Name": "BrokenLinks",
      "DataType": {
        "Identifier": "Container",
        "Reference": "BrokenLink",
        "ElementDataType": {
          "Identifier": "Class",
          "Reference": "BrokenLink"
        }
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer"
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String"
      }
    }
  ]
}
```

La colección `BrokenLinks` contiene objetos del tipo **BrokenLink**. Cada objeto proporciona las siguientes propiedades:

- **CellName** – La dirección de la celda que contiene la referencia rota (por ejemplo, `B12`).
- **LinkType** – El tipo de enlace roto (por ejemplo, `ExternalReference`, `Formula`).
- **ErrorMessage** – Una descripción del motivo por el que se considera roto el enlace.

**Nota**: La API está sujeta a límites de tasa. Consulte la página [Precios y límites de tasa](https://www.aspose.cloud/pricing) para obtener más detalles.

### Códigos de error

- **400 Bad Request** – URI de la API de Aspose.Cells Cloud no válido.
- **401 Unauthorized** – Token de acceso, ID de cliente o secreto de cliente no válidos.
- **404 Not Found** – El archivo de hoja de cálculo no es accesible.
- **500 Server Error** – La hoja de cálculo encontró una anomalía al obtener los datos de cálculo.

## ¿Dónde debemos utilizar la API de búsqueda de enlaces rotos en el rango de la hoja de cálculo?

- **Auditoría regular de modelos financieros grandes** – Antes de publicar informes mensuales o trimestrales, escanee automáticamente las áreas clave de cálculo (por ejemplo, `Panel!B5:K50`) que contienen muchas referencias a datos externos para asegurarse de que todos los enlaces apunten a archivos de origen válidos.
- **Integración de datos en fusiones y adquisiciones** – Al fusionar varios archivos de hojas de cálculo que representan unidades de negocio, escanee la hoja "Resumen" tras la integración para identificar enlaces que hayan quedado inválidos debido a cambios en las rutas de archivo o problemas de permisos.
- **Preparación de paquetes de datos para inversores** – Antes de finalizar materiales de presentación que contengan gráficos y tablas vinculados a bases de datos externas o fuentes de datos de mercado, verifique la validez de todos los enlaces.

## ¿Por qué debería utilizar la API de búsqueda de enlaces rotos en el rango de la hoja de cálculo?

- **Amigable para desarrolladores** – Aspose.Cells Cloud ofrece bibliotecas SDK en múltiples lenguajes, lo que permite un desarrollo rápido con documentación completa. En comparación con la construcción de una solución personalizada, esto reduce significativamente el esfuerzo de desarrollo.
- **Reducción de costos de mano de obra** – Elimina la necesidad de personal dedicado para consolidar documentos manualmente.
- **Pago por uso** – Sin inversión inicial; solo paga por las llamadas a la API que realmente realiza.
- **Cero costos de mantenimiento** – Sin servidores que mantener, sin actualizaciones de software y sin preocupaciones por compatibilidad.
- **Preserva el formato complejo de Excel** – Los resultados pueden exportarse al formato PDF universalmente accesible sin perder el estilo.

## Cómo utilizar la API de búsqueda de enlaces rotos en el rango de la hoja de cálculo con SDK

### Especificación OpenAPI

La [Especificación OpenAPI](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Search/SearchBrokenLinksInRemoteRange) define una interfaz de programación públicamente accesible y le permite realizar interacciones REST directamente desde un navegador web.

### Uso de los SDK de Aspose.Cells Cloud

Utilizar el SDK es la mejor forma de acelerar el desarrollo. El SDK maneja los detalles subyacentes, lo que le permite implementar la funcionalidad de "buscar enlaces rotos en un rango" con un código mínimo. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código demuestran cómo realizar llamadas a los servicios web de Aspose.Cells utilizando diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_SearchBrokenLinksInRemoteRange.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_SearchBrokenLinksInRemoteRange.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_SearchBrokenLinksInRemoteRange.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_SearchBrokenLinksInRemoteRange.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_SearchBrokenLinksInRemoteRange.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_SearchBrokenLinksInRemoteRange.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_SearchBrokenLinksInRemoteRange.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_SearchBrokenLinksInRemoteRange.go" >}}
{{</tab>}}
{{< /tabs >}}

---