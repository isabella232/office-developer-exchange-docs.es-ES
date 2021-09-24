---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: El elemento AlternateId describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta.
ms.openlocfilehash: 6346a45b48eb811cac705d8da85dc77e6c18262c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520944"
---
# <a name="alternateid"></a>AlternateId

El **elemento AlternateId** describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Describe el identificador de origen en una [solicitud de operación ConvertId](convertid-operation.md) y describe el identificador de destino en una respuesta de operación [ConvertId.](convertid-operation.md)  <br/> |
|Formato  <br/> |Describe el formato de origen en una solicitud de [operación ConvertId](convertid-operation.md) y describe el formato de destino en una respuesta de [operación ConvertId.](convertid-operation.md) El atributo **DestinationFormat** del [elemento ConvertId](convertid.md) de la solicitud describe el formato de destino. Este atributo es de tipo **IdFormatType**.  <br/> |
|Buzón de correo  <br/> |Describe la dirección SMTP (Protocolo simple de transferencia de correo) principal del buzón que contiene los identificadores que se traducirán.  <br/> |
|IsArchive  <br/> |Indica si el identificador representa un elemento o carpeta archivados. Un valor de **true** indica que el identificador representa un elemento o carpeta archivados. Este atributo es opcional.  <br/> |
   
#### <a name="format-attribute-values"></a>Valores de atributo Format

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe los identificadores generados por Exchange Web Services en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe los identificadores generados por Exchange Web Services a partir Exchange 2007 SP1.  <br/> |
|EntryID  <br/> |Describe los identificadores MAPI, como en la **PR_ENTRYID** propiedad.  <br/> |
|HexEntryId  <br/> |Describe una representación con codificación hexadecimal de la **PR_ENTRYID** propiedad. Este es el formato de los identificadores de eventos del calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe Exchange identificadores de almacén.  <br/> |
|OwaId  <br/> |Describe un identificador Outlook Web App.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una [solicitud de operación ConvertId.](convertid-operation.md)  <br/> |
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se convertirán.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El **elemento AlternateId** describe dos identificadores, el identificador de origen que se va a convertir en la solicitud de operación [ConvertId](convertid-operation.md) y el identificador convertido en el [elemento ConvertIdResponse.](convertidresponse.md) 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

||||
|:-----|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Conversión de identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

