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
description: El elemento AlternateId describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta.
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763428"
---
# <a name="alternateid"></a>AlternateId

El elemento **AlternateId** describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta. 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 **AlternateIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Describe el identificador de origen en una solicitud de [operación de ConvertId](convertid-operation.md) y el identificador de destino en una respuesta de la [operación de ConvertId](convertid-operation.md) .  <br/> |
|Format  <br/> |Describe el formato de origen en una solicitud de [operación de ConvertId](convertid-operation.md) y se describe el formato de destino en una respuesta de la [operación de ConvertId](convertid-operation.md) . Se describe el formato de destino mediante el atributo **DestinationFormat** del elemento [ConvertId](convertid.md) en la solicitud. Este atributo es del tipo **IdFormatType**.  <br/> |
|Buz?n de correo  <br/> |Describe la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de buzón de correo que contiene los identificadores para traducir.  <br/> |
|IsArchive  <br/> |Indica si el identificador representa una carpeta o elemento archivado. Un valor de **true** indica que el identificador representa una carpeta o elemento archivado. Este atributo es opcional.  <br/> |
   
#### <a name="format-attribute-values"></a>Valores de atributos de formato

|**Valor**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |Describe identificadores producidos por servicios Web de Exchange en la versión inicial de Exchange 2007.  <br/> |
|EwsId  <br/> |Describe identificadores producidos por los servicios Web Exchange comenzando con Exchange 2007 SP1.  <br/> |
|Propiedad EntryId  <br/> |Describe identificadores de MAPI, como se muestra en la propiedad de **entrada del objeto** .  <br/> |
|HexEntryId  <br/> |Describe una representación codificada en hexadecimal de la propiedad de **entrada del objeto** . Éste es el formato de los identificadores de eventos de calendario de disponibilidad.  <br/> |
|StoreId  <br/> |Describe identificadores de almacén de Exchange.  <br/> |
|OwaId  <br/> |Se describe un identificador de Outlook Web App.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ConvertIdResponseMessage](convertidresponsemessage.md) <br/> |Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .  <br/> |
|[SourceIds](sourceids.md) <br/> |Contiene los identificadores de origen para convertir.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Observaciones

El elemento **AlternateId** describe dos identificadores, el identificador de origen que se convierte en la solicitud de la [operación de ConvertId](convertid-operation.md) y el identificador convertido en el elemento [ConvertIdResponse](convertidresponse.md) . 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

||||
|:-----|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación ConvertId](convertid-operation.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
- [Convertir identificadores](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

