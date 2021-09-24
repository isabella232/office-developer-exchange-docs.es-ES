---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: El elemento ExtendedProperty especifica una propiedad extendida para el almacén de contactos unificado.
ms.openlocfilehash: 5cb320e15d3a01c542907048357d1ef0cc78f96a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530762"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty (PathToExtendedFieldType)

El **elemento ExtendedProperty** especifica una propiedad extendida para el almacén de contactos unificado. 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |Indica el identificador del conjunto de propiedades distintivo. Este atributo es opcional.  <br/> |
|PropertySetId  <br/> |Indica el identificador del conjunto de propiedades GUID. Este atributo es opcional.  <br/> |
|PropertyTag  <br/> | Representa la etiqueta de propiedad menos la parte de tipo.<br/><br/>Hay dos opciones para la representación:  <br/><br/>- Hexadecimal: 0x3fa4  <br/>- Decimal: 0-65535<br/><br/>  Este atributo es opcional.  <br/> |
|PropertyName  <br/> |Cadena que indica el nombre de la propiedad. Este atributo es opcional.  <br/> |
|PropertyId  <br/> |Integer que indica el identificador de la propiedad. Este atributo es opcional.  <br/> |
|PropertyType  <br/> |Indica el tipo de propiedad. Este atributo es obligatorio.  <br/> |
|FieldURI  <br/> |Indica el campo Identificador uniforme de recursos (URI). Este atributo es obligatorio. Para obtener los valores posibles, vea [el elemento FieldURI.](fielduri.md)  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Valor**|**Descripción**|
|:-----|:-----|
|Reunión  <br/> |Indica una reunión.  <br/> |
|Cita  <br/> |Indica una cita.  <br/> |
|Común  <br/> |Indica el conjunto de propiedades comunes.  <br/> |
|PublicStrings  <br/> |Indica cadenas públicas.  <br/> |
|Address  <br/> |Indica una dirección.  <br/> |
|InternetHeaders  <br/> |Indica encabezados de Internet.  <br/> |
|CalendarAssistant  <br/> |Indica el Asistente de calendario.  <br/> |
|UnifiedMessaging  <br/> |Indica mensajería unificada.  <br/> |
|Tarea  <br/> |Indica una tarea.  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**Valor**|**Descripción**|
|:-----|:-----|
|ApplicationTime  <br/> |Indica la hora de la aplicación.  <br/> |
|ApplicationTimeArray  <br/> |Indica una matriz de tiempos de aplicación.  <br/> |
|Binario  <br/> |Indica un valor binario.  <br/> |
|BinaryArray  <br/> |Indica una matriz de valores binarios.  <br/> |
|Booleano  <br/> |Indica un valor booleano.  <br/> |
|CLSID  <br/> |Indica un CLSID.  <br/> |
|CLSIDArray  <br/> |Indica una matriz de CLSID.  <br/> |
|Divisa  <br/> |Indica un valor de moneda.  <br/> |
|CurrencyArray  <br/> |Indica una matriz de valores de moneda.  <br/> |
|Doble  <br/> |Indica un **doble**.  <br/> |
|DoubleArray  <br/> |Indica una matriz de **valores** dobles.  <br/> |
|Error  <br/> |Indica un error. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Float  <br/> |Indica un **float**.  <br/> |
|FloatArray  <br/> |Indica una matriz de **valores float.**  <br/> |
|Entero  <br/> |Indica un número entero.  <br/> |
|IntegerArray  <br/> |Indica una matriz de enteros.  <br/> |
|Long  <br/> |Indica un **largo**.  <br/> |
|LongArray  <br/> |Indica una matriz de **valores largos.**  <br/> |
|Null  <br/> |Indica un valor nulo. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Objeto  <br/> |Indica un objeto. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|ObjectArray  <br/> |Indica una matriz de objetos. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Corta  <br/> |Indica un **breve**.  <br/> |
|ShortArray  <br/> |Indica una matriz de **valores cortos.**  <br/> |
|SystemTime  <br/> |Indica un valor de hora del sistema.  <br/> |
|SystemTimeArray  <br/> |Indica una matriz de valores de hora del sistema.  <br/> |
|Cadena  <br/> |Indica una cadena.  <br/> |
|StringArray  <br/> |Indica una matriz de cadenas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica una propiedad MAPI extendida.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

