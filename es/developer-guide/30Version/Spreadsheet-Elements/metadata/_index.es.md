---
title: "Trabajo con metadatos y propiedades de Excel"
second_title: "Documento"
linktitle: "Metadatos y propiedades"
type: docs
url: /metadata/
aliases:
  - /document-properties/
  - /working-with-document-properties/
keywords: "Aspose.Cells Cloud, metadatos de Excel, API de propiedades de documentos, API REST, obtener metadatos, actualizar propiedades de Excel, eliminar metadatos de Excel"
description: "Aprenda cómo leer, agregar, actualizar y eliminar metadatos de archivos de Excel utilizando la API REST de Aspose.Cells Cloud. Incluye ejemplos para cURL y SDKs en Java, .NET, Python, Node.js y más."
ArticleTitle: "Trabajo con metadatos de Excel y propiedades de documentos – Aspose.Cells Cloud"
weight: 100
---

Los archivos de Excel pueden almacenar diversos metadatos que ayudan a identificar, organizar y gestionar los documentos. Aspose.Cells Cloud ofrece una API REST sencilla para leer, agregar, actualizar y eliminar estos metadatos, permitiendo a los desarrolladores integrar la gestión de propiedades de documentos en sus aplicaciones. Esta guía cubre las dos categorías principales de propiedades: estándar y personalizadas, explica cómo trabajar con ellas y proporciona enlaces directos a los puntos finales de la API correspondientes. También encontrará una tabla concisa de referencia de la API con los detalles de las solicitudes para acelerar la implementación.

**Última actualización:** 8 de julio de 2026  

**Tipos de propiedades de documentos**

Antes de aprender a utilizar las APIs de Aspose.Cells Cloud para ver, modificar y eliminar propiedades de documentos (metadatos) en Excel, aclaremos los tipos de propiedades que puede tener un documento de Excel.

- **Propiedades estándar**: son comunes en Excel. Contienen información básica como Título, Asunto, Autor, Categoría, etc. Puede asignar valores de texto personalizados a estas propiedades para facilitar la localización del archivo.

- **Propiedades personalizadas**: son definidas por el usuario. Le permiten agregar metadatos adicionales al documento de Excel.

**Cómo trabajar con propiedades de documentos en un archivo de Excel**

- [Cómo obtener una propiedad de documento específica utilizando almacenamiento](/cells/document-properties/get/)
- [Cómo obtener propiedades de documento sin utilizar almacenamiento](/cells/metadata/get/)
- [Cómo obtener todas las propiedades de documento utilizando almacenamiento](/cells/document-properties/get-all/)
- [Cómo actualizar una propiedad de documento específica utilizando almacenamiento](/cells/document-properties/update/)
- [Cómo actualizar una propiedad de documento específica sin utilizar almacenamiento](/cells/metadata/update/)
- [Cómo eliminar una propiedad de documento específica utilizando almacenamiento](/cells/document-properties/delete/)
- [Cómo eliminar propiedades de documento sin utilizar almacenamiento](/cells/metadata/delete/)
- [Cómo eliminar todas las propiedades de documento utilizando almacenamiento](/cells/document-properties/clear/)

**Referencia de la API (sin almacenamiento)**  

| Método | Punto final | Descripción |
|--------|-------------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Recupera todas las propiedades del documento del libro almacenado en la nube. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Recupera el valor de una propiedad específica (estándar o personalizada) identificada por `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Actualiza el valor de una propiedad existente. El cuerpo de la solicitud contiene el nuevo valor en formato JSON. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Elimina una propiedad específica del libro. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Borra todas las propiedades personalizadas y estándar del libro. |

*Todas las solicitudes requieren un token de acceso OAuth 2.0 y pueden incluir parámetros de consulta opcionales como `storage` y `folder` cuando se utiliza una ubicación de almacenamiento específica.*