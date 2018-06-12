---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: El elemento ConvertId define una solicitud para convertir los identificadores de elemento y carpeta entre formatos compatibles con Exchange. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 956f6464fd9013f9e72d2915f21c3b011d0add5b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763883"
---
# <a name="convertid"></a>ConvertId

El elemento **ConvertId** define una solicitud para convertir los identificadores de elemento y carpeta entre formatos compatibles con Exchange. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**DestinationFormat** <br/> |Describe el formato de identificador que se devolverán para todos los identificadores de convertidos. Se describe la DestinationFormat por la IdFormatType.  <br/> |
   
#### <a name="destinationformat-attribute"></a>Atributo DestinationFormat

|**Valor**|**Descripción**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que se proporcionan en la versión inicial de Exchange 2007.  <br/> |
|**EwsId** <br/> |Representa el formato de identificador que se usa para los identificadores de los servicios Web Exchange empezando con Exchange Server 2007 SP1.  <br/> |
|**Propiedad EntryId** <br/> |Representa el identificador MAPI, como se muestra en la propiedad de entrada del objeto.  <br/> |
|**HexEntryId** <br/> |Representa el identificador de evento del calendario de disponibilidad. Ésta es una representación codificada en hexadecimal de la propiedad de entrada del objeto.  <br/> |
|**StoreId** <br/> |Representa el identificador de almacén de Exchange.  <br/> |
|**OwaId** <br/> |Representa el formato de identificador de Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen para convertir.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación ConvertId](convertid-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Convertir identificadores](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

