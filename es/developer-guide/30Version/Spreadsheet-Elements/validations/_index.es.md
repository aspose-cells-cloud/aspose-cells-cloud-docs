---
title: "Trabajo con la validación de datos en Excel"
second_title: "Documentos"
linktype: "Validaciones"
type: docs
url: /validations/
keywords: "validación de datos en Excel, Aspose.Cells Cloud, API REST, hoja de cálculo, nube ofimática"
description: "Aprenda a agregar, recuperar, actualizar, eliminar y borrar reglas de validación de datos en Excel mediante la API REST de Aspose.Cells Cloud. Incluye ejemplos para .NET, Java, Python y PHP."
weight: 100
ArticleTitle: "Trabajo con la validación de datos en Excel — Documentación de la API de Aspose.Cells Cloud"
---

La validación de datos en Excel es una funcionalidad de Microsoft Excel que permite controlar lo que un usuario puede introducir en una celda de una hoja de cálculo. Puede restringir las entradas a un rango de fechas específico, solo números enteros, e incluso crear listas desplegables que ahorran espacio y muestran valores en una sola celda. Asimismo, puede definir un mensaje personalizado que aparezca cuando un usuario introduzca un valor incorrecto o un formato no válido.

Por ejemplo, un usuario puede especificar una reunión programada entre las 9:00 y las 18:00 horas.

La validación de datos puede utilizarse para garantizar que un valor sea un número positivo, una fecha comprendida entre el día 15 y el día 30 de un mes, una fecha dentro de los próximos 30 días, o una entrada de texto que contenga menos de 25 caracteres, entre otras posibilidades.

### Resumen de la API

| Operación | Método HTTP | Punto de conexión | Descripción |
|-----------|-------------|-------------------|-------------|
| Agregar | POST | `/cells/{file}/worksheets/{sheet}/validations` | Crear una regla de validación |
| Obtener | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Recuperar una regla específica |
| Obtener todas | GET | `/cells/{file}/worksheets/{sheet}/validations` | Listar todas las reglas |
| Actualizar | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Modificar una regla |
| Eliminar | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Eliminar una regla |
| Borrar | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Eliminar todas las reglas |

## Trabajo con validaciones en un archivo de Excel

- [Cómo agregar una regla de validación a una hoja de cálculo de Excel](/cells/validations/add/)
- [Cómo obtener una regla de validación de una hoja de cálculo de Excel](/cells/validations/get/)
- [Cómo obtener todas las reglas de validación de una hoja de cálculo de Excel](/cells/validations/get-all/)
- [Cómo eliminar una regla de validación de una hoja de cálculo de Excel](/cells/validations/delete/)
- [Cómo borrar todas las reglas de validación de una hoja de cálculo de Excel](/cells/validations/clear/)
- [Cómo actualizar una regla de validación en una hoja de cálculo de Excel](/cells/validations/update/)
---