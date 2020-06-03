---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: El elemento AlternateId describe un identificador que se va a convertir en una solicitud y los resultados de un identificador convertido en la respuesta.
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527456"
---
# <a name="alternateid"></a>AlternateId

El elemento **AlternateId** describe un identificador que se va a convertir en una solicitud y los resultados de un identificador convertido en la respuesta. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Describe el identificador de origen en una solicitud de [operación ConvertId](convertid-operation.md) y describe el identificador de destino en una respuesta de [operación ConvertId](convertid-operation.md) .  <br/> |
|Formato  <br/> |Describe el formato de origen en una solicitud de [operación ConvertId](convertid-operation.md) y describe el formato de destino en una respuesta de [operación ConvertId](convertid-operation.md) . El formato de destino se describe mediante el atributo **DestinationFormat** del elemento [ConvertId](convertid.md) en la solicitud. Este atributo es del tipo **IdFormatType**.  <br/> |
|Buzón de correo  <br/> |Describe la dirección del Protocolo simple de transferencia de correo (SMTP) principal del buzón que contiene los identificadores que se van a traducir.  <br/> |
|IsArchive  <br/> |Indica si el identificador representa un elemento o una carpeta archivados. Un valor de **true** indica que el identificador representa un elemento o una carpeta archivados. Este atributo es opcional.  <br/> |
   
#### <a name="format-attribute-values"></a>Valores de atributo de formato

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe los identificadores producidos por los servicios Web de Exchange en la versión de lanzamiento inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe los identificadores que crean los servicios Web de Exchange a partir de Exchange 2007 SP1.  <br/> |
|EntryId  <br/> |Describe los identificadores de MAPI, como en la propiedad **PR_ENTRYID** .  <br/> |
|HexEntryId  <br/> |Describe una representación codificada en hexadecimal de la propiedad **PR_ENTRYID** . Este es el formato de los identificadores de evento de calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe los identificadores de almacén de Exchange.  <br/> |
|OwaId  <br/> |Describe un identificador de Outlook Web App.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .  <br/> |
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen que se van a convertir.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El elemento **AlternateId** describe dos identificadores, el identificador de origen que se va a convertir en la solicitud de [operación ConvertId](convertid-operation.md) y el identificador convertido en el elemento [ConvertIdResponse](convertidresponse.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

||||
|:-----|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Convertir identificadores](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

