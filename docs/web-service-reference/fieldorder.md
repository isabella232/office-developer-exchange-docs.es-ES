---
title: FieldOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FieldOrder
api_type:
- schema
ms.assetid: b9364842-bbe2-4221-afef-bf5022bc89ec
description: El elemento FieldOrder representa un solo campo por el que se va a ordenar los resultados e indica la dirección para la ordenación.
ms.openlocfilehash: 320a7b821cc593e7dd60a8f8adb23bcd600f71f8
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353304"
---
# <a name="fieldorder"></a>FieldOrder

El elemento **FieldOrder** representa un solo campo por el que se va a ordenar los resultados e indica la dirección para la ordenación. 
  
```xml
<FieldOrder Order="">
   <FieldURI/>
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <ExtendedFieldURI/> 
</FieldOrder>
```

```xml
<FieldOrder Order="">
   <IndexedFieldURI/>
</FieldOrder>
```

**FieldOrderType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**Order** <br/> | Describe la dirección del criterio de ordenación.<br/><br/> Los valores posibles son: <br/> <br/>-Ascendente  <br/>-Descendente  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifica las propiedades con frecuencia que se hace referencia mediante un identificador URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifica a los miembros individuales de un diccionario.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifica las propiedades MAPI.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[SortOrder](sortorder.md) <br/> |Define cómo se ordenan los elementos en una solicitud FindItem.  <br/> La siguiente es la expresión de XPath para este elemento:`/FindItem/SortOrder` <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

