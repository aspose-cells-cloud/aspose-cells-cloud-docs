---
title: Configuración del libro de trabajo
second_title: Aspose.Cells Cloud Documen
type: docs
url: /es/specification/model/workbooksettings/
description: "Aspose.Cells Especificación del modelo de nube: WorkbookSettings. Maneje sin esfuerzo Excel y otros documentos de hoja de cálculo con funciones como abrir, generar, editar, dividir, fusionar, comparar y convertir."
weight: 50
---
## **libro de trabajoConfiguración**

 

| Nombre de la propiedad| tipo de propiedad| Anulable| Solo lectura| Valor por defecto| Descripción|
|:- |:- |:- |:- |:- |:- |
| AutoComprimirImágenes| Booleano| Verdadero| FALSO|| Especifica un valor booleano que indica que la aplicación comprime automáticamente las imágenes en el libro.|
| Autorrecuperación| Booleano| Verdadero| FALSO|| Indica si el archivo está marcado para recuperación automática.|
| Versión de compilación| Cadena| Verdadero| FALSO|| Especifica la versión pública incremental de la aplicación.|
| ModoCalc| Cadena| Verdadero| FALSO||Especifica si se deben calcular fórmulas de forma manual, automática o automática, excepto para operaciones de tablas múltiples.|
| ID de cálculo| Cadena| Verdadero| FALSO|| Especifica la versión del motor de cálculo utilizado para calcular los valores en el libro.|
| Comprobar compatibilidad| Booleano| Verdadero| FALSO|| Indica si se verifica la compatibilidad al guardar el libro de trabajo. Observaciones: El valor predeterminado es verdadero.|
| ComprobarExcelRestricción| Booleano| Verdadero| FALSO||Si se verifica la restricción del archivo de Excel cuando el usuario modifica los objetos relacionados con las celdas. Por ejemplo, Excel no permite ingresar un valor de cadena de más de 32 K. Cuando ingresa un valor de más de 32 K, como Cell.PutValue (cadena), si esta propiedad es verdadera, obtendrá una excepción. Si esta propiedad es falsa, aceptaremos el valor de la cadena de entrada como el valor de la celda para que luego pueda generar el valor de la cadena completa para otros formatos de archivo como CSV. Sin embargo, si ha establecido un tipo de valor que no es válido para el formato de archivo Excel, no debe guardar el libro como formato de archivo Excel más adelante. De lo contrario, puede haber un error inesperado en el archivo Excel generado.|
| CrashGuardar| Booleano| Verdadero| FALSO|| indica si la aplicación guardó por última vez el archivo del libro después de un bloqueo.|
| CrearCalcChain| Booleano| Verdadero| FALSO|| Si crea una cadena de fórmulas calculadas. El valor predeterminado es falso.|
| Carga de extracción de datos| Booleano| Verdadero| FALSO||indica si la aplicación abrió por última vez el libro para la recuperación de datos.|
| Fecha1904| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que representa si el libro utiliza el sistema de fechas 1904.|
| Mostrar objetos de dibujo| Cadena| Verdadero| FALSO|| Indica si se deben mostrar objetos en el libro y cómo hacerlo.|
| Habilitar macros| Booleano| Verdadero| FALSO|| Habilitar macros;|
| Primera pestaña visible| Entero| Verdadero| FALSO|| Obtiene o establece la primera pestaña visible de la hoja de cálculo.|
| Ocultar lista de campos dinámicos| Booleano| Verdadero| FALSO|| Obtiene y establece si se oculta la lista de campos de la tabla dinámica.|
| Está cifrado por defecto| Booleano| Verdadero| FALSO|| Indica si se cifra el libro con la contraseña predeterminada si la Estructura y Windows del libro están bloqueados.|
| Está oculto| Booleano| Verdadero| FALSO|| Indica si este libro está oculto.|
| IsHScrollBarVisible| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si la hoja de cálculo generada contendrá una barra de desplazamiento horizontal.|
| Está minimizado| Booleano| Verdadero| FALSO|| Representa si la hoja de cálculo generada se abrirá Minimizada.|
| IsVScrollBarVisible| Booleano| Verdadero| FALSO||Obtiene o establece un valor que indica si la hoja de cálculo generada contendrá una barra de desplazamiento vertical.|
| Iteración| Booleano| Verdadero| FALSO|| Indica si habilitar el cálculo iterativo para resolver referencias circulares.|
| Código de lenguaje| Cadena| Verdadero| FALSO|| Obtiene o establece el idioma de la interfaz de usuario de la versión del libro de trabajo según el código de país que guardó el archivo.|
| Cambio máximo| Flotante| Verdadero| FALSO|| Devuelve o establece el número máximo de cambios para resolver una referencia circular.|
| MaxIteración| Entero| Verdadero| FALSO|| Devuelve o establece el número máximo de iteraciones para resolver una referencia circular.|
| Configuración de memoria| Cadena| Verdadero| FALSO|| Obtiene o establece las opciones de uso de memoria. La nueva opción se tomará como la opción predeterminada para las hojas de trabajo recién creadas, pero no tendrá efecto para las hojas de trabajo existentes.|
| NúmeroDecimalSeparador| Cadena| Verdadero| FALSO|| Obtiene o establece el separador decimal para formatear o analizar valores numéricos. El valor predeterminado es el separador decimal de la región actual.|
| NúmeroGrupoSeparador| Cadena| Verdadero| FALSO|| Obtiene o establece el carácter que separa grupos de dígitos a la izquierda del decimal en valores numéricos. El valor predeterminado es el separador de grupo de la región actual.|
| Análisis de fórmula en apertura| Booleano| Verdadero| FALSO||Indica si se analiza la fórmula al leer el archivo.|
| Precisión como se muestra| Booleano| Verdadero| FALSO|| Verdadero si los cálculos de este libro se realizarán utilizando solo la precisión de los números tal como se muestran|
| Recalcular antes de guardar| Booleano| Verdadero| FALSO|| Indica si se debe volver a calcular antes de guardar el documento.|
| Recalcular al abrir| Booleano| Verdadero| FALSO|| Indica si se vuelven a calcular todas las fórmulas al abrir el archivo.|
| RecomendarSolo lectura| Booleano| Verdadero| FALSO|| Indica si la opción Recomendada de solo lectura está seleccionada.|
| Región| Cadena| Verdadero| FALSO|| Obtiene o establece la configuración regional del libro.|
| Eliminar información personal| Booleano| Verdadero| FALSO|| Verdadero si la información personal se puede eliminar del libro especificado.|
| ReparaciónCarga| Booleano| Verdadero| FALSO|| Indica si la aplicación abrió el libro por última vez en modo seguro o de reparación.|
| Compartido| Booleano| Verdadero| FALSO|| Obtiene o establece un valor que indica si el libro está compartido.|
| HojaTabBarAncho| Entero| Verdadero| FALSO|| Ancho de la barra de pestañas de la hoja de trabajo (en 1/1000 del ancho de la ventana).|
| Mostrar pestañas| Booleano| Verdadero| FALSO||Obtiene o establece un valor si se muestran las pestañas del Libro de trabajo.|
| Actualizar borde de celdas adyacentes| Booleano| Verdadero| FALSO|| Indica si se actualiza el borde de las celdas adyacentes.|
| Tipo de enlaces de actualización| Cadena| Verdadero| FALSO|| Obtiene y establece cómo se actualizan los vínculos externos cuando se abre el libro.|
| Altura de la ventana| Flotante| Verdadero| FALSO|| La altura de la ventana, en unidad de punto.|
| VentanaIzquierda| Flotante| Verdadero| FALSO|| La distancia desde el borde izquierdo del área del cliente hasta el borde izquierdo de la ventana, en unidades de punto.|
| ventanaarriba| Flotante| Verdadero| FALSO|| La distancia desde el borde superior del área del cliente hasta el borde superior de la ventana, en unidades de punto.|
| Ancho de ventana| Flotante| Verdadero| FALSO|| El ancho de la ventana, en unidad de punto.|
| Autor| Cadena| Verdadero| FALSO|| Obtiene y establece el autor del archivo.|
| Comprobar formato de número personalizado| Booleano| Verdadero| FALSO|| Indica si se comprueba el formato de número personalizado al configurar Style.Custom.|
| Tipo de protección| Cadena| Verdadero| FALSO|| Obtiene el tipo de protección del libro.|
| GlobalizaciónConfiguración| Clase:Configuración de globalización| Verdadero| FALSO|| Obtiene y establece la configuración de globalización.|
| Contraseña| Cadena| Verdadero| FALSO||Representa la contraseña de cifrado del archivo de Workbook.|
| Protección de escritura| Clase:Protección contra escritura| Verdadero| FALSO|| Proporciona acceso a las opciones de protección contra escritura del libro.|
| Está cifrado| Booleano| Verdadero| FALSO|| Obtiene un valor que indica si se requiere una contraseña para abrir este libro.|
| Esta protegido| Booleano| Verdadero| FALSO|| Obtiene un valor que indica si la estructura o ventana del libro está protegida.|
| fila máxima| Entero| Verdadero| FALSO|| Obtiene el índice de fila máximo, de base cero.|
| Columna máxima| Entero| Verdadero| FALSO|| Obtiene el índice máximo de columna, de base cero.|
| Dígitos significantes| Entero| Verdadero| FALSO|| Obtiene y establece el número de dígitos significativos. El valor predeterminado es .|
| Comprobar compatibilidad| Booleano| Verdadero| FALSO|| Indica si se verifica la compatibilidad con versiones anteriores al guardar el libro.|
| Tamaño de papel| Cadena| Verdadero| FALSO|| Obtiene y establece el tamaño de papel de impresión predeterminado.|
| MaxRowsOfSharedFormula| Entero| Verdadero| FALSO|| Obtiene y establece el número máximo de filas de la fórmula compartida.|
| Cumplimiento| Cadena| Verdadero| FALSO|| Especifica la versión OOXML para el documento de salida. El valor predeterminado es Ecma376_2006.|
| QuotePrefixToStyle| Booleano| Verdadero| FALSO||Indica si se establece la propiedad al ingresar el valor de cadena (que comienza con comillas simples) en la celda|
| Configuración de fórmula| Clase:Configuración de fórmula| Verdadero| FALSO|| Obtiene la configuración de las características relacionadas con fórmulas.|
| FuerzaCompletaCalcular| Booleano| Verdadero| FALSO|| Calcula completamente cada vez que se activa un cálculo.|

