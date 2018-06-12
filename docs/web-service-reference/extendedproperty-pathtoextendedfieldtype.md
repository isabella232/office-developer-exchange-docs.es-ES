---
title: ExtendedProperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: El elemento ExtendedProperty especifica una propiedad extendida para el almacén de contactos unificados.
ms.openlocfilehash: 7541fa6330ee96f7791febfabc672dbcf0e95b54
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764535"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>ExtendedProperty (PathToExtendedFieldType)

El elemento **ExtendedProperty** especifica una propiedad extendida para el almacén de contactos unificados. 
  
```xml
<ExtendedProperty DistinguishedPropertySetId="" PropertySetId="" PropertyTag="" PropertyName="" PropertyId="" PropertyType="" FieldURI="">
</ExtendedProperty>
```

**PathToExtendedFieldType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|DistinguishedPropertySetId  <br/> |Indica el identificador del conjunto de propiedad distintivo. Este atributo es opcional.  <br/> |
|PropertySetId  <br/> |Indica el identificador de conjunto GUID (propiedad). Este atributo es opcional.  <br/> |
|PropertyTag  <br/> | Representa la etiqueta de propiedad menos el elemento de tipo.<br/><br/>Hay dos opciones para la representación:  <br/><br/>-Hexadecimal: 0x3fa4  <br/>-Decimal: 0-65535<br/><br/>  Este atributo es opcional.  <br/> |
|PropertyName  <br/> |Cadena que indica el nombre de la propiedad. Este atributo es opcional.  <br/> |
|PropertyId  <br/> |Número entero que indica el identificador de la propiedad. Este atributo es opcional.  <br/> |
|PropertyType  <br/> |Indica el tipo de propiedad. Este atributo es necesario.  <br/> |
|FieldURI  <br/> |Indica el identificador uniforme de recursos (URI) del campo. Este atributo es necesario. Para los valores posibles, vea el elemento [FieldURI](fielduri.md) .  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Valor**|**Descripción**|
|:-----|:-----|
|Reunión  <br/> |Indica una reunión.  <br/> |
|Cita  <br/> |Indica una cita.  <br/> |
|Common  <br/> |Indica el conjunto de propiedades común.  <br/> |
|PublicStrings  <br/> |Indica las cadenas públicas.  <br/> |
|Address  <br/> |Indica una dirección.  <br/> |
|InternetHeaders  <br/> |Indica los encabezados de Internet.  <br/> |
|CalendarAssistant  <br/> |Indica al Ayudante de calendario.  <br/> |
|Ésta  <br/> |Indica la mensajería unificada.  <br/> |
|Tarea  <br/> |Indica una tarea.  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**Valor**|**Descripción**|
|:-----|:-----|
|ApplicationTime  <br/> |Indica la hora de la aplicación.  <br/> |
|ApplicationTimeArray  <br/> |Indica una matriz de veces que la aplicación.  <br/> |
|Binario  <br/> |Indica un valor binario.  <br/> |
|BinaryArray  <br/> |Indica una matriz de valores binarios.  <br/> |
|Boolean  <br/> |Indica un valor de tipo Boolean.  <br/> |
|CLSID  <br/> |Indica un CLSID.  <br/> |
|CLSIDArray  <br/> |Indica una matriz de CLSID.  <br/> |
|Moneda  <br/> |Indica un valor de moneda.  <br/> |
|CurrencyArray  <br/> |Indica una matriz de valores de moneda.  <br/> |
|Doble  <br/> |Indica un **tipo double**.  <br/> |
|DoubleArray  <br/> |Indica una matriz de valores de **tipo double** .  <br/> |
|Error  <br/> |Indica un error. Esto es para fines de presentación de informes de error. No se puede usar en las restricciones, o para obtener o establecer valores.  <br/> |
|Flotante  <br/> |Indica un **float**.  <br/> |
|FloatArray  <br/> |Indica una matriz de valores **float** .  <br/> |
|Entero  <br/> |Indica un entero.  <br/> |
|IntegerArray  <br/> |Indica una matriz de números enteros.  <br/> |
|Long  <br/> |Indica un **tipo long**.  <br/> |
|LongArray  <br/> |Indica una matriz de valores de **tipo long** .  <br/> |
|Null  <br/> |Indica un valor null. Esto es para fines de presentación de informes de error. No se puede usar en las restricciones, o para obtener o establecer valores.  <br/> |
|Objeto  <br/> |Indica un objeto. Esto es para fines de presentación de informes de error. No se puede usar en las restricciones, o para obtener o establecer valores.  <br/> |
|ObjectArray  <br/> |Indica una matriz de objetos. Esto es para fines de presentación de informes de error. No se puede usar en las restricciones, o para obtener o establecer valores.  <br/> |
|Corta  <br/> |Indica un **breve**.  <br/> |
|ShortArray  <br/> |Indica una matriz de valores **cortos** .  <br/> |
|SystemTime  <br/> |Indica un valor de hora del sistema.  <br/> |
|SystemTimeArray  <br/> |Indica una matriz de valores de hora del sistema.  <br/> |
|Cadena  <br/> |Indica una cadena.  <br/> |
|StringArray  <br/> |Indica una matriz de cadenas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica una propiedad MAPI extendida.  <br/> |
   
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

