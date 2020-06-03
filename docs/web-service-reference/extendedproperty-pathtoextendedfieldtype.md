---
title: Las extendedproperty (PathToExtendedFieldType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa620b48-2ce3-437d-b51e-541247eea1d9
description: El elemento las extendedproperty especifica una propiedad extendida para el almacén de contactos unificados.
ms.openlocfilehash: f6c283d5cce3bc927662ad0d9c796c0589e7054c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460144"
---
# <a name="extendedproperty-pathtoextendedfieldtype"></a>Las extendedproperty (PathToExtendedFieldType)

El elemento **las extendedproperty** especifica una propiedad extendida para el almacén de contactos unificados. 
  
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
|DistinguishedPropertySetId  <br/> |Indica el identificador del conjunto de propiedades distinguido. Este atributo es opcional.  <br/> |
|PropertySetId  <br/> |Indica el identificador del conjunto de propiedades GUID. Este atributo es opcional.  <br/> |
|PropertyTag  <br/> | Representa la etiqueta de propiedad menos la parte de tipo.<br/><br/>Hay dos opciones para la representación:  <br/><br/>-Hexadecimal: 0x3fa4  <br/>-Decimal: 0-65535<br/><br/>  Este atributo es opcional.  <br/> |
|PropertyName  <br/> |Cadena que indica el nombre de la propiedad. Este atributo es opcional.  <br/> |
|PropertyId  <br/> |Número entero que indica el identificador de la propiedad. Este atributo es opcional.  <br/> |
|PropertyType  <br/> |Indica el tipo de propiedad. Este atributo es obligatorio.  <br/> |
|FieldURI  <br/> |Indica el identificador uniforme de recursos (URI) del campo. Este atributo es obligatorio. Para obtener los valores posibles, vea el elemento [FieldURI](fielduri.md) .  <br/> |
   
#### <a name="distinguishedpropertysetid"></a>DistinguishedPropertySetId

|**Valor**|**Descripción**|
|:-----|:-----|
|Misma  <br/> |Indica una reunión.  <br/> |
|Cita  <br/> |Indica una cita.  <br/> |
|Común  <br/> |Indica el conjunto de propiedades comunes.  <br/> |
|PublicStrings  <br/> |Indica las cadenas públicas.  <br/> |
|Address  <br/> |Indica una dirección.  <br/> |
|InternetHeaders  <br/> |Indica los encabezados de Internet.  <br/> |
|CalendarAssistant  <br/> |Indica el Asistente de calendario.  <br/> |
|UnifiedMessaging  <br/> |Indica la mensajería unificada.  <br/> |
|Tarea  <br/> |Indica una tarea.  <br/> |
   
#### <a name="propertytype"></a>PropertyType

|**Valor**|**Descripción**|
|:-----|:-----|
|ApplicationTime  <br/> |Indica la hora de la aplicación.  <br/> |
|ApplicationTimeArray  <br/> |Indica una matriz de tiempos de aplicación.  <br/> |
|Binario  <br/> |Indica un valor binario.  <br/> |
|BinaryArray  <br/> |Indica una matriz de valores binarios.  <br/> |
|Boolean  <br/> |Indica un valor booleano.  <br/> |
|CLSID  <br/> |Indica un CLSID.  <br/> |
|CLSIDArray  <br/> |Indica una matriz de CLSID.  <br/> |
|Moneda  <br/> |Indica un valor de moneda.  <br/> |
|CurrencyArray  <br/> |Indica una matriz de valores de moneda.  <br/> |
|Doble  <br/> |Indica un **doble**.  <br/> |
|DoubleArray  <br/> |Indica una matriz de valores de **tipo Double** .  <br/> |
|Error  <br/> |Indica un error. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Float  <br/> |Indica un **punto flotante**.  <br/> |
|FloatArray  <br/> |Indica una matriz de valores **float** .  <br/> |
|Entero  <br/> |Indica un número entero.  <br/> |
|IntegerArray  <br/> |Indica una matriz de enteros.  <br/> |
|Long  <br/> |Indica un **Long**.  <br/> |
|LongArray  <br/> |Indica una matriz de valores **Long** .  <br/> |
|Null  <br/> |Indica un valor null. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Objeto  <br/> |Indica un objeto. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|ObjectArray  <br/> |Indica una matriz de objetos. Esto es para fines de informes de errores. No se puede usar en restricciones ni para obtener o establecer valores.  <br/> |
|Corta  <br/> |Indica un **Short**.  <br/> |
|ShortArray  <br/> |Indica una matriz de valores **Short** .  <br/> |
|Compatibilidad  <br/> |Indica un valor de hora del sistema.  <br/> |
|SystemTimeArray  <br/> |Indica una matriz de valores de tiempo del sistema.  <br/> |
|Cadena  <br/> |Indica una cadena.  <br/> |
|StringArray  <br/> |Indica una matriz de cadenas.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
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
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

