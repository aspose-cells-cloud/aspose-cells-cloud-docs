---
title: "Aspose.Cells Cloud AI – API de descomposición de tareas de usuario (v4.0) | Planificación inteligente de tareas (SMART)"
second_title: "Documento"
ArticleTitle: "Cómo convertir objetivos de usuario en planes secuenciales de acciones con la API de descomposición de tareas de Aspose.Cells Cloud AI"
linktitle: "Descomponer tarea de usuario"
type: docs
url: /es/decompose-user-task/
keywords: "Aspose.Cells AI, API de descomposición de tareas, planificación inteligente de tareas (SMART), importación Redmine, automatización de proyectos"
description: "Transforme objetivos en formato libre en listas de tareas SMART con estimaciones de tiempo, utilizando Aspose.Cells Cloud AI. Obtenga salida en CSV/XLSX para Redmine, Jira o Azure DevOps en una única solicitud PUT."
weight: 100
---

El endpoint **DecomposeUserTask** proporciona una API REST para convertir una descripción de tarea en formato libre en un plan de acciones detallado y secuencial que cumple con los criterios SMART. Asigna automáticamente estimaciones de tiempo en horas, formatea la salida para importación compatible con Redmine y crea nodos de hitos del proyecto. Al proporcionar únicamente la lista de tareas en bruto y estimaciones de tiempo opcionales, la API devuelve un archivo listo para usar (CSV, XLSX, etc.) que puede importarse directamente en herramientas de gestión de proyectos, automatizando la descomposición de tareas y reduciendo el esfuerzo manual.

## **API de descomposición de tareas de usuario**

### API web

```http
PUT https://api.aspose.cloud/v4.0/cells/ai/task/decompose
```

### **Seguridad y autenticación**

Las API de Aspose.Cells Cloud son seguras y requieren <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">autenticación basada en token JWT</a>.

### **Parámetros de solicitud:**

| Nombre del parámetro | Tipo   | Ubicación | Obligatorio/Opcional | Descripción                                                                                                                                                                                                                              |
| :------------------- | :----- | :-------- | :------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| TaskDescription      | string | Cuerpo    | Obligatorio          | Descripción en texto plano del objetivo general del usuario. El servicio analiza la descripción y genera tareas individuales. Ejemplo: “Lanzar campaña de marketing para el T3, incluyendo creación de contenido, envío masivo de correos y anuncios en redes sociales.” |

### **Respuesta**

Respuesta correcta (200 OK)  
Content‑Type: `application/octet-stream` (flujo binario de archivo)

Encabezados:

- `Content-Disposition: attachment; filename="DecomposedTaskPlan.xlsx"`
- `Content-Length: <tamaño en bytes>`

La misma estructura se utiliza para formatos XLSX/ODS, con las columnas colocadas en la primera hoja de cálculo.

**Códigos de estado HTTP**

| Código | Significado             | Descripción                                                     |
| ------ | ----------------------- | --------------------------------------------------------------- |
| 200    | OK                      | Filtro aplicado correctamente; la respuesta contiene detalles de la operación. |
| 400    | Solicitud incorrecta    | Parámetros ausentes o inválidos (por ejemplo, tipo de archivo no admitido). |
| 401    | No autorizado           | Token JWT inválido o ausente.                                   |
| 413    | Carga demasiado grande   | El archivo cargado supera el límite de tamaño.                 |
| 500    | Error interno del servidor | Error inesperado en el servidor.                               |

**Ejemplo de respuesta de error (400 Solicitud incorrecta)**

```json
{
  "code": "InvalidParameter",
  "message": "El campo 'TaskDescription' es obligatorio y no puede estar vacío."
}
```

**Ejemplo de cuerpo de solicitud (JSON)**

```json
{
  "TaskDescription": "Desarrollar una API web para una funcionalidad de división de tareas en el sistema existente."
}
```

**Ejemplo de respuesta**  
La API devuelve un flujo binario que contiene el archivo generado. Para previsualizar las primeras filas de una respuesta en CSV, decodifique el flujo y visualice la fila de encabezados, por ejemplo:

```
ID,Subject,Trucker,Estimated Duration,Description
1	Recolección de requisitos para la API de división de tareas	Analista de negocio	8	Recopilar requisitos funcionales y no funcionales, historias de usuario y criterios de aceptación para el nuevo endpoint de división de tareas.
2	Especificación de la API (OpenAPI)	Analista de negocio	6	Definir el contrato OpenAPI para POST /tasks/split, incluyendo esquema de solicitud, formatos de respuesta, códigos de error y requisitos de seguridad.
3	Diseño del algoritmo de división y del modelo de datos	Arquitecto de soluciones	5	Diseñar el algoritmo central que divide una tarea principal en subtareas, y ampliar el modelo de datos (tablas/entidades de base de datos) para almacenar la jerarquía y los metadatos.
4	Revisión de integración de arquitectura	Arquitecto de soluciones	4	Analizar el impacto en los servicios existentes, flujos de eventos y migraciones de base de datos; producir el plan de integración.
...
```

## ¿Dónde debemos utilizar la API de descomposición de tareas de usuario?

- **Inicio de proyectos**: Convertir un resumen de proyecto de alto nivel en una lista de tareas compatible con Redmine que incluya estimaciones de tiempo, permitiendo una planificación inmediata de sprints.
- **Automatización de marketing**: Descomponer objetivos de campañas en pasos ejecutables, exportar como CSV e importar en herramientas de gestión de tareas para coordinación entre equipos.
- **Asignación de recursos**: Generar estimaciones basadas en horas para cada subtarea, permitiendo a los gerentes equilibrar la carga de trabajo entre miembros del equipo antes del inicio del proyecto.
- **Seguimiento de hitos**: Crear automáticamente nodos de hitos que puedan sincronizarse con herramientas de diagramas de Gantt, garantizando que cada fase tenga un entregable claro.

## ¿Por qué debería utilizar la API de descomposición de tareas de usuario?

- **Salida conforme a SMART** asegura que cada tarea generada cumpla con los criterios Específica, Medible, Alcanzable, Relevante y Temporal.
- **Estimación de tiempo basada en horas integrada** elimina la necesidad de cálculos manuales y mejora la precisión de las proyecciones.
- **Formatos de archivo listos para importar** (CSV, XLSX, etc.) facilitan la integración con Redmine, Jira, Azure DevOps y otras plataformas de gestión de proyectos.
- **Automatización en una sola solicitud** permite la descomposición de tareas mediante una única solicitud, acelerando el inicio del proyecto y minimizando el esfuerzo manual.

## Cómo utilizar la API de descomposición de tareas de usuario con SDK

### Especificación de la API de descomposición de tareas de usuario

La <a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/AI/DecomposeUserTask" target="_blank" rel="noopener noreferrer">Especificación de la API de descomposición de tareas de usuario</a> proporciona una interfaz de programación accesible públicamente para ejecutar interacciones REST directamente desde un navegador web.

## SDK para API de Excel

### Uso de los SDK de Aspose.Cells Cloud

Utilizar el SDK es la forma más rápida de desarrollar, ya que abstracte los detalles de bajo nivel y permite invocar el endpoint DecomposeUserTask con código conciso.  
Consulte el <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">repositorio de GitHub</a> para obtener una lista completa de los SDK de Aspose.Cells Cloud.  
Los siguientes ejemplos de código muestran cómo interactuar con los servicios web de Aspose.Cells mediante diversos SDK:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_v4.0_DecomposeUserTask.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_v4.0_DecomposeUserTask.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_v4.0_DecomposeUserTask.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_v4.0_DecomposeUserTask.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_v4.0_DecomposeUserTask.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_v4.0_DecomposeUserTask.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_v4.0_DecomposeUserTask.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_v4.0_DecomposeUserTask.go" >}}
{{</tab>}}
{{< /tabs >}}

---