---
title: "Trabajo con tablas dinámicas mediante la tarea CellsObjectOperate"
type: docs
url: /es/tasks/cells-object-operate/pivottable/
aliases: [  /es/working-with-pivot-table-using-cellsobjectoperate-task/ ]
keywords: "API de tabla dinámica de Aspose Cells, CellsObjectOperate, API REST de Excel"
description: "Aprenda a generar una tabla dinámica en Excel utilizando la tarea CellsObjectOperate de Aspose.Cells Cloud. Incluye un ejemplo en cURL, guía de parámetros y referencias a SDK."
weight: 10
---

Esta **API REST** **crea** una tabla dinámica utilizando la tarea **CellsObjectOperate**.

**PivotTableOperateParameter**

| Nombre del parámetro  | Tipo          | Descripción                                                                 |
|-----------------------|---------------|-----------------------------------------------------------------------------|
| DestCellName          | string        | Celda superior izquierda de la tabla dinámica (por ejemplo, `C1`).         |
| SourceData            | string        | Rango que contiene los datos de origen (por ejemplo, `Sheet2!A1:E8`).      |
| TableName             | string        | Nombre asignado a la nueva tabla dinámica.                                 |
| UseSameSource         | string        | `true` / `false` – indica si la tabla dinámica utiliza el mismo libro de origen. |
| PivotTableIndex       | integer       | Índice de la tabla dinámica cuando existen varias tablas en la hoja de cálculo. |
| PivotFieldRows        | integer[]     | Índices de base cero de los campos que se colocarán en el área de filas.    |
| PivotFieldColumns     | integer[]     | Índices de base cero de los campos que se colocarán en el área de columnas. |
| PivotFieldData        | integer[]     | Índices de base cero de los campos que se agruparán como datos.             |

## API REST

| **API**               | **Type** | **Descripción** | **Enlace al recurso** |
|-----------------------|----------|-----------------|-----------------------|
| /cells/task/runtask   | POST     | Ejecutar tarea    | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

La [Especificación OpenAPI](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) define una interfaz de programación públicamente accesible y permite realizar interacciones REST directamente desde un navegador web.

### Requisitos previos
Antes de invocar la API, debe:

1. Registrarse en una cuenta de Aspose.Cloud y crear una aplicación para obtener un **client ID** y un **client secret**.  
2. Solicitar un **token JWT** desde el endpoint `/connect/token` utilizando las credenciales del cliente.  
3. Incluir el token en el encabezado `Authorization: Bearer <jwt token>` de cada solicitud.  

Ahora puede utilizar la herramienta de línea de comandos **cURL** para acceder a los servicios web de Aspose.Cells.

{{< tabs tabTotal="2" tabID="1" tabName1="Solicitud" tabName2="Respuesta" >}}

{{< tab tabNum="1" >}}

```bash
# Ejemplo en cURL – importar datos (paso 1)
curl -v "https://api.aspose.cloud/v3.0/cells/task/runtask" \
  -X POST \
  -H "accept: application/xml" \
  -H "Content-Type: application/xml" \
  -H "Authorization: Bearer <jwt token>" \
  -d '
<TaskData>
  <Tasks>
    <TaskDescription>
      <TaskType>ImportData</TaskType>
      <ImportDataTaskParameter>
        <Workbook>
          <FileSourceType>CloudFileSystem</FileSourceType>
          <FilePath>Book1.xlsx</FilePath>
        </Workbook>
        <ImportBatchDataOption>
          <DestinationWorksheet>Sheet2</DestinationWorksheet>
          <IsInsert>true</IsInsert>
          <BatchData>
            <!-- Filas de ejemplo – solo se muestran algunas para brevedad -->
            <CellValue><rowIndex>0</rowIndex><columnIndex>0</columnIndex><type>String</type><value>Deporte</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>1</columnIndex><type>String</type><value>Año</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>2</columnIndex><type>String</type><value>Trimestre</value></CellValue>
            <CellValue><rowIndex>0</rowIndex><columnIndex>3</columnIndex><type>String</type><value>Ventas</value></CellValue>
            <!-- …filas adicionales omitidas por claridad… -->
          </BatchData>
        </ImportBatchDataOption>
      </ImportDataTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>CellsObjectOperate</TaskType>
      <CellsObjectOperateTaskParameter>
        <OperateObject>
          <OperateObjectType>ListObject</OperateObjectType>
          <Position>
            <Workbook>
              <FileSourceType>InMemoryFiles</FileSourceType>
              <FilePath>Book1.xlsx</FilePath>
            </Workbook>
            <SheetName>Sheet1</SheetName>
            <ListObjectIndex>0</ListObjectIndex>
          </Position>
        </OperateObject>

        <PivotTableOperateParameter>
          <OperateType>Add</OperateType>
          <SourceData>=Sheet2!A1:E8</SourceData>
          <DestCellName>C1</DestCellName>
          <TableName>TestPivot</TableName>
          <UseSameSource>true</UseSameSource>
          <PivotTableIndex>0</PivotTableIndex>
          <PivotFieldRows><int>0</int><int>1</int></PivotFieldRows>
          <PivotFieldColumns><int>2</int></PivotFieldColumns>
          <PivotFieldData><int>3</int><int>4</int></PivotFieldData>
        </PivotTableOperateParameter>

        <DestinationWorkbook>
          <FileSourceType>InMemoryFiles</FileSourceType>
          <FilePath>Book001.xlsx</FilePath>
        </DestinationWorkbook>
      </CellsObjectOperateTaskParameter>
    </TaskDescription>

    <TaskDescription>
      <TaskType>SaveResult</TaskType>
      <SaveResultTaskParameter>
        <ResultSource>InMemoryFiles</ResultSource>
        <ResultDestination>
          <DestinationType>OutputStream</DestinationType>
          <InputFile>Book001.xlsx</InputFile>
          <OutputFile>Output/ReportS004.xlsx</OutputFile>
        </ResultDestination>
      </SaveResultTaskParameter>
    </TaskDescription>
  </Tasks>
</TaskData>'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
Códigos de estado HTTP posibles:
- **200 OK** – Tabla dinámica creada correctamente. El cuerpo de la respuesta contiene un `TaskId` que puede utilizarse para consultar el estado de la operación.
- **400 Bad Request** – Payload XML no válido o parámetros obligatorios ausentes.
- **401 Unauthorized** – Token JWT ausente o inválido.
- **500 Internal Server Error** – Error inesperado del lado del servidor.

Ejemplo de respuesta correcta (XML):

<?xml version="1.0" encoding="UTF-8"?>
<TaskResponse>
  <TaskId>12345</TaskId>
  <Status>Completed</Status>
  <Result>
    <ResultSource>InMemoryFiles</ResultSource>
    <ResultDestination>Output/ReportS004.xlsx</ResultDestination>
  </Result>
</TaskResponse>
```

{{< /tab >}}

{{< /tabs >}}

## Familia de SDK en la nube

Utilizar un SDK es la mejor forma de acelerar el desarrollo. Un SDK se encarga de los detalles de bajo nivel y le permite centrarse en las tareas de su proyecto. Consulte el [repositorio de GitHub](https://github.com/aspose-cells-cloud) para ver una lista completa de los SDK de Aspose.Cells Cloud.

Los siguientes ejemplos de código muestran cómo realizar llamadas a los servicios web de Aspose.Cells mediante diversos SDK: