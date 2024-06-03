---
title: Opción de guardar paginada
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/paginatedsaveoptions/
description: "Aspose.Cells Especificación del modelo de nube: PaginatedSaveOptions. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
kwords: Excel, Office, Hoja de cálculo, Cloud REST API, PaginatedSaveOptions
weight: 50
---
## **paginadoSaveOptions**

 Representa las opciones de paginación.

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| Fuente predeterminada| Cadena| Verdadero| FALSO|| Cuando los caracteres en Excel son Unicode y no están configurados con la fuente correcta en el estilo de celda, pueden aparecer como un bloque en pdf o imagen. Configure la fuente predeterminada, como MingLiu o MS Gothic, para mostrar estos caracteres. Si esta propiedad no está configurada, Aspose.Cells utilizará la fuente predeterminada del sistema para mostrar estos caracteres Unicode.|
| CheckWorkbookDefaultFont| Booleano| Verdadero| FALSO|| Cuando los caracteres en Excel son Unicode y no están configurados con la fuente correcta en el estilo de celda, pueden aparecer como un bloque en pdf, imagen. Establezca esto en verdadero para intentar usar la fuente predeterminada del libro para mostrar estos caracteres primero.|
| Comprobar compatibilidad de fuentes| Booleano| Verdadero| FALSO|| Indica si se debe verificar la compatibilidad de fuentes para cada carácter del texto.|
| IsFontSubstitutionCharGranularidad| Booleano| Verdadero| FALSO||Indica si solo se debe sustituir la fuente del carácter cuando la fuente de la celda no sea compatible con él.|
| Una página por hoja| Booleano| Verdadero| FALSO|| Si OnePagePerSheet es verdadero, todo el contenido de una hoja se imprimirá en una sola página. El tamaño del papel de configuración de página no será válido y las demás configuraciones de configuración de página seguirán teniendo efecto.|
| Todas las columnas en una página por hoja| Booleano| Verdadero| FALSO|| Si AllColumnsInOnePagePerSheet es verdadero, todo el contenido de las columnas de una hoja se generará en una sola página como resultado. Se ignorará el ancho del tamaño del papel de pagesetup y las demás configuraciones de pagesetup seguirán teniendo efecto.|
| Ignorar error| Booleano| Verdadero| FALSO|| Indica si necesita ocultar el error durante la representación. El error puede ser un error en la forma, la imagen, la representación del gráfico, etc.|
| Salida de página en blanco cuando no hay nada que imprimir| Booleano| Verdadero| FALSO|| Indica si se debe generar una página en blanco cuando no hay nada que imprimir.|
| Índice de página| Entero| Verdadero| FALSO|| Obtiene o establece el índice basado en 0 de la primera página que se guardará.|
| Número de páginas| Entero| Verdadero| FALSO|| Obtiene o establece el número de páginas que se guardarán.|
| Tipo de página de impresión| Cadena| Verdadero| FALSO|| Indica qué páginas no se imprimirán.|
| Tipo de línea de cuadrícula| Cadena| Verdadero| FALSO|| Obtiene o establece el tipo de línea de cuadrícula.|
| TextoCruzTipo| Cadena| Verdadero| FALSO|| Obtiene o establece la visualización del tipo de texto cuando el ancho del texto es mayor que el ancho de la celda.|
| Idioma de edición predeterminado| Cadena| Verdadero| FALSO|| Obtiene o establece el idioma de edición predeterminado.|
| EmfRenderConfiguración| Cadena| Verdadero| FALSO|||
| Fusionar áreas| Booleano| Verdadero| FALSO|||
| Ordenar nombres externos| Booleano| Verdadero| FALSO|||
| ActualizarSmartArt| Booleano| Verdadero| FALSO|||
| Guardar formato| Cadena| Verdadero| FALSO|||
| Carpeta de archivos en caché| Cadena| Verdadero| FALSO|||
| Borrar datos| Booleano| Verdadero| FALSO|||
| Crear directorio| Booleano| Verdadero| FALSO|||
| Habilitar compresión HTTP| Booleano| Verdadero| FALSO|||
| Actualizar caché de gráficos| Booleano| Verdadero| FALSO|||
| Ordenar nombres| Booleano| Verdadero| FALSO|||
| Validar áreas fusionadas| Booleano| Verdadero| FALSO|||

**Nombre del padre** : [Guardar Opciones](/specification/model/saveoptions)

**Nombre de los niños** : 
	-  [Opciones de DocxSave](docxsaveoptions) 
	-  [PptxGuardarOpciones](pptxsaveoptions) 
	-  [XpsGuardarOpciones](xpssaveoptions) 
