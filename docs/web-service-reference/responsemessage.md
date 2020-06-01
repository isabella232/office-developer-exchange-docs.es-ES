---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: El elemento ResponseMessage proporciona información descriptiva sobre el estado de respuesta para una única entidad dentro de una solicitud.
ms.openlocfilehash: a7f4240b1e988cb69d67118c6db58db0d7babba5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467161"
---
# <a name="responsemessage"></a>ResponseMessage

El elemento **ResponseMessage** proporciona información descriptiva sobre el estado de respuesta para una única entidad dentro de una solicitud. 
  
```xml
<ResponseMessage ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
</ResponseMessage>
```

 **ResponseMessageType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Representa el estado de la respuesta. <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>-Correcto  <br/>-ADVERTENCIA  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores del atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Describe una solicitud que se ha completado.  <br/> |
|Advertencia  <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos. <br/><br/>Las siguientes son algunas causas posibles de las advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el lote.  <br/>-El servicio de directorio de Active Directory está sin conexión.  <br/>-Se mueven los buzones.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha superado la cuota.  <br/> |
|Error  <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>Las siguientes son algunas causas posibles de errores:  <br/><br/>-Atributos o elementos no válidos  <br/>-Atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-Atributo o elemento no válido en el contexto  <br/>-Intento de acceso no autorizado por parte de un cliente  <br/>-Error del servidor en respuesta a una llamada válida del lado cliente  <br/> <br/> La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso en el futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de respuesta de error adicional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Contiene la información de disponibilidad de un único usuario de buzón de correo. <br/> <br/> La siguiente es la expresión XPath 2,0 a este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |Contiene información de respuesta y datos de sugerencias para las sugerencias de reunión solicitadas.  <br/><br/> La siguiente es la expresión XPath 2,0 a este elemento:<br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de OOF para un usuario.  <br/><br/> La siguiente es la expresión XPath 2,0 a este elemento:  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[SetUserOofSettingsResponse](setuseroofsettingsresponse.md) <br/> |Contiene el resultado de un mensaje [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) intentó. <br/> <br/> La siguiente es la expresión XPath 2,0 a este elemento:  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo **ResponseMessageType** es común a todas las respuestas de servicios Web de Exchange. El tipo **ResponseMessageType** se extiende mediante los tipos complejos siguientes: 
  
- **ApplyConversationActionResponseMessageType**
    
- **AttachmentInfoResponseMessageType**
    
- **DeleteAttachmentResponseMessageType**
    
- **DeleteItemResponseMessageType**
    
- **ExpandDLResponseMessageType**
    
- **FindFolderResponseMessageType**
    
- **FindItemResponseMessageType**
    
- **FolderInfoResponseMessageType**
    
- **GetEventsResponseMessageType**
    
- **ItemInfoResponseMessageType**
    
- **ResolveNamesResponseMessageType**
    
- **SubscribeResponseMessageType**
    
- **SendNotificationResponseMessageType**
    
- **SyncFolderHierarchyResponseMessageType**
    
- **SyncFolderItemsResponseMessageType**
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
### <a name="version-differences"></a>Diferencias de versión

Los tipos **ApplyConversationActionResponseMessage** y **DeleteItemResponseMessageType** se introdujeron en Exchange Build 15.00.0986.00. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)
- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

