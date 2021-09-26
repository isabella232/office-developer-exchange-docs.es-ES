---
title: ConvertId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ConvertId
api_type:
- schema
ms.assetid: 9684c22c-29d4-4f7f-befc-8cd41da56d38
description: El elemento ConvertId define una solicitud para convertir identificadores de elementos y carpetas entre los formatos Exchange compatibles. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: fe7d46697ba72ba6458136541488f5cd498169f4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545562"
---
# <a name="convertid"></a>ConvertId

El **elemento ConvertId** define una solicitud para convertir identificadores de elementos y carpetas entre formatos Exchange admitidos. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
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
|**DestinationFormat** <br/> |Describe el formato de identificador que se devolverá para todos los identificadores convertidos. El IdFormatType describe DestinationFormat.  <br/> |
   
#### <a name="destinationformat-attribute"></a>Atributo DestinationFormat

|**Valor**|**Descripción**|
|:-----|:-----|
|**EwsLegacyId** <br/> |Representa el formato de identificador que se usa para Exchange de servicios web que se proporcionan en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|**EwsId** <br/> |Representa el formato de identificador que se usa para Exchange de servicios web a partir Exchange Server 2007 SP1.  <br/> |
|**EntryId** <br/> |Representa el identificador MAPI, como en la PR_ENTRYID propiedad.  <br/> |
|**HexEntryId** <br/> |Representa el identificador de evento del calendario de disponibilidad. Se trata de una representación con codificación hexadecimal de la PR_ENTRYID propiedad.  <br/> |
|**StoreId** <br/> |Representa el identificador Exchange almacén.  <br/> |
|**OwaId** <br/> |Representa el Outlook de identificador de Web Access.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se convertirán.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación ConvertId](convertid-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Conversión de identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

