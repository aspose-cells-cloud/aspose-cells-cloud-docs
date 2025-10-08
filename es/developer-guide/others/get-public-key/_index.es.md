---
title: Aspose.Cells Cloud WEb API - Obtener clave pública
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Obtener clave pública
type: docs
url: /es/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Recupere una clave pública asimétrica para el cifrado seguro de datos
weight: 100
kwords: cifrado asimétrico, clave pública, REST API, Excel API, seguridad, cifrado de datos, integración API, JSON, documentación API
---
Recupera la clave pública de un algoritmo de cifrado asimétrico.

## **Obtener la clave pública API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Parámetros de la solicitud:**

| Nombre del parámetro| Tipo| Ruta/Cadena de consulta/Cuerpo HTTP| Descripción|
|:- |:- |:- |:- |
|||||

### **Respuesta**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## Cómo usar la clave pública API con SDK

### Especificación OpenAPI

 El[Especificación OpenAPI](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) define una interfaz de programación de acceso público que le permite realizar interacciones REST directamente desde su navegador web.

### Utilice los SDK de la nube Aspose.Cells

Usar el SDK es la mejor manera de acelerar el desarrollo. El SDK gestiona los detalles subyacentes, lo que permite implementar fácilmente la obtención de la clave pública para las celdas con un mínimo de código.
 Por favor, consulte el[Repositorio de GitHub](https://github.com/aspose-cells-cloud) para obtener una lista completa de Aspose.Cells SDK en la nube.

Los siguientes ejemplos de código ilustran cómo interactuar con los servicios web Aspose.Cells utilizando varios SDK:
