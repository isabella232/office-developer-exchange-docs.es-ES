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
description: El elemento ConvertId define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos de Exchange admitidos. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: d421baf1f29fb59a8c6eb2b09e1fa0e8a38ffaa4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44452541"
---
# <a name="convertid"></a>ConvertId

El elemento **ConvertId** define una solicitud para convertir los identificadores de elemento y carpeta entre los formatos de Exchange admitidos. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ConvertId DestinationFormat="">
   <SourceIds/>
</ConvertId>
```

 **ConvertIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**DestinationFormat** <br/> |Describe el formato de identificador que se devolverá para todos los identificadores convertidos. La DestinationFormat se describe mediante el IdFormatType.  <br/> |
   
#### <a name="destinationformat-attribute"></a>Atributo DestinationFormat

|**Valor**|**Descripción**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que se proporcionan en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|**EwsId** <br/> |Representa el formato de identificador que se usa para los identificadores de servicios Web de Exchange que comienzan con Exchange Server 2007 SP1.  <br/> |
|**EntryId** <br/> |Representa el identificador de MAPI, como en la propiedad PR_ENTRYID.  <br/> |
|**HexEntryId** <br/> |Representa el identificador de evento del calendario de disponibilidad. Se trata de una representación codificada en hexadecimal de la propiedad PR_ENTRYID.  <br/> |
|**StoreId** <br/> |Representa el identificador del almacén de Exchange.  <br/> |
|**OwaId** <br/> |Representa el formato de identificador de Outlook Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se van a convertir.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación ConvertId](convertid-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Convertir identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

