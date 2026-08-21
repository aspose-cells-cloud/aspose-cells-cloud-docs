---
title: "Procesamiento por lotes de archivos Excel: Convertir, Bloquear, Proteger, Dividir y Desbloquear"
second_title: "Documentos"
linktype: "documentación"
type: docs
url: /es/batch/
keywords: "Procesamiento por lotes, Excel, conversión, bloqueo, protección, división, desbloqueo, Aspose.Cells Cloud API, referencia de API, operaciones por lotes"
description: "La API de Aspose.Cells Cloud permite el procesamiento por lotes de múltiples archivos Excel para conversión, bloqueo, protección, división y desbloqueo. Incluye especificaciones detalladas de la API y soporte para SDK en Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby y Swift."
weight: 35
ArticleTitle: "Procesamiento por lotes de archivos Excel – Convertir, Bloquear, Proteger, Dividir y Desbloquear con la API de Aspose.Cells Cloud"
---

La API de Aspose.Cells Cloud proporciona puntos finales para procesamiento por lotes que le permiten realizar operaciones comunes sobre múltiples archivos Excel en una única solicitud. A continuación se presenta una descripción general rápida de las operaciones por lotes disponibles, junto con especificaciones concisas de la API para cada una.

- **["Convertir archivos Excel por lotes"](https://docs.aspose.cloud/cells/batch/convert "Convertir archivos Excel por lotes")**  
  *Convierta múltiples archivos Excel a un formato de salida elegido en una sola solicitud.*  

  **Detalles de la API**  
  ```http
  POST /cells/batch/convert
  Content-Type: multipart/form-data
  Authorization: Bearer {access_token}
  ```  

  **Parámetros**  

  | Nombre        | Tipo     | Descripción                                     |
  |---------------|----------|-------------------------------------------------|
  | files         | file[]   | Uno o más archivos Excel que se convertirán.   |
  | outputFormat  | string   | Formato de salida deseado (por ejemplo, pdf, csv, html). |
  | storage       | string   | (Opcional) Nombre del almacenamiento en la nube. |

  **Respuestas**  

  | Código | Descripción                                      |
  |--------|--------------------------------------------------|
  | 200    | Conversión exitosa; devuelve los archivos.      |
  | 400    | Parámetros inválidos proporcionados.             |
  | 401    | No autorizado: token ausente o inválido.         |
  | 500    | Error interno del servidor.                      |

- **["Bloquear archivos Excel por lotes"](https://docs.aspose.cloud/cells/batch/lock "Bloquear archivos Excel por lotes")**  
  *Aplicar un bloqueo por contraseña a múltiples archivos Excel simultáneamente.*  

  **Detalles de la API**  
  ```http
  POST /cells/batch/lock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parámetros**  

  | Nombre     | Tipo   | Descripción                               |
  |------------|--------|-------------------------------------------|
  | files      | array  | Lista de identificadores de archivos o URLs. |
  | password   | string | Contraseña para bloquear los libros.      |
  | storage    | string | (Opcional) Nombre del almacenamiento en la nube. |

  **Respuestas**  

  | Código | Descripción                                      |
  |--------|--------------------------------------------------|
  | 200    | Archivos bloqueados con éxito.                   |
  | 400    | Parámetros ausentes o inválidos.                 |
  | 401    | Acceso no autorizado.                            |
  | 500    | Error del servidor.                              |

- **["Proteger archivos Excel por lotes"](https://docs.aspose.cloud/cells/batch/protect "Proteger archivos Excel por lotes")**  
  *Aplicar configuraciones de protección (por ejemplo, solo lectura, estructura) a múltiples libros.*  

  **Detalles de la API**  
  ```http
  POST /cells/batch/protect
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parámetros**  

  | Nombre        | Tipo   | Descripción                                           |
  |---------------|--------|-------------------------------------------------------|
  | files         | array  | Lista de identificadores de archivos o URLs.         |
  | protection    | object | Opciones de protección (por ejemplo, readOnly, structure). |
  | storage       | string | (Opcional) Nombre del almacenamiento en la nube.     |

  **Respuestas**  

  | Código | Descripción                                      |
  |--------|--------------------------------------------------|
  | 200    | Protección aplicada con éxito.                    |
  | 400    | Datos de solicitud inválidos.                     |
  | 401    | Autenticación fallida.                            |
  | 500    | Error inesperado del servidor.                    |

- **["Dividir por lotes"](https://docs.aspose.cloud/cells/batch/split "Dividir por lotes")**  
  *Dividir libros Excel grandes en archivos más pequeños según hojas de cálculo o rangos de filas.*  

  **Detalles de la API**  
  ```http
  POST /cells/batch/split
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parámetros**  

  | Nombre      | Tipo   | Descripción                                       |
  |-------------|--------|---------------------------------------------------|
  | files       | array  | Archivos que se dividirán.                        |
  | splitBy     | string | Criterio: "worksheet" (hoja de cálculo) o "rowRange" (rango de filas). |
  | criteria    | object | Detalles del método de división elegido.         |
  | storage     | string | (Opcional) Nombre del almacenamiento en la nube. |

  **Respuestas**  

  | Código | Descripción                                      |
  |--------|--------------------------------------------------|
  | 200    | Operación de división completada; devuelve las partes. |
  | 400    | Parámetros de división incorrectos.              |
  | 401    | Solicitud no autorizada.                         |
  | 500    | Error durante el procesamiento.                  |

- **["Desbloquear por lotes"](https://docs.aspose.cloud/cells/batch/unlock "Desbloquear por lotes")**  
  *Eliminar la protección por contraseña de múltiples archivos Excel en una sola llamada.*  

  **Detalles de la API**  
  ```http
  POST /cells/batch/unlock
  Content-Type: application/json
  Authorization: Bearer {access_token}
  ```  

  **Parámetros**  

  | Nombre     | Tipo   | Descripción                                  |
  |------------|--------|----------------------------------------------|
  | files      | array  | Lista de identificadores o URLs de archivos bloqueados. |
  | password   | string | Contraseña actual de los archivos.          |
  | storage    | string | (Opcional) Nombre del almacenamiento en la nube. |

  **Respuestas**  

  | Código | Descripción                                      |
  |--------|--------------------------------------------------|
  | 200    | Archivos desbloqueados con éxito.                |
  | 400    | Contraseña incorrecta o archivos ausentes.       |
  | 401    | Acceso no autorizado.                            |
  | 500    | Fallo en el lado del servidor.                   |
---