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
description: El elemento ResponseMessage proporciona información descriptiva sobre el estado de respuesta para una entidad única dentro de una solicitud.
ms.openlocfilehash: 69f1f6f12d10044045b72dd644536e742c479b9e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837191"
---
# <a name="responsemessage"></a>ResponseMessage

El elemento **ResponseMessage** proporciona información descriptiva sobre el estado de respuesta para una entidad única dentro de una solicitud. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ResponseClass** <br/> | Representa el estado de la respuesta. <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>-Éxito  <br/>-Advertencia  <br/>-Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo de ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Describe una solicitud que se cumplen los requisitos.  <br/> |
|Advertencia  <br/> | Describe una solicitud que no se procesó. Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes. <br/><br/>Las siguientes son algunas posibles causas de advertencias:  <br/><br/>-El almacén de Exchange está sin conexión durante el proceso por lotes.  <br/>-El servicio de directorio de Active Directory está sin conexión.  <br/>-Se mueven los buzones de correo.  <br/>-La base de datos de mensajes (MDB) está sin conexión.  <br/>-Una contraseña ha expirado.  <br/>-Se ha excedido una cuota.  <br/> |
|Error  <br/> | Describe una solicitud que no se cumplen los requisitos. <br/><br/>Las siguientes son algunas posibles causas de errores:  <br/><br/>-No válida Atributos o elementos  <br/>-Los atributos o elementos fuera del intervalo  <br/>-Etiqueta desconocida  <br/>-De atributo o elemento no es válido en el contexto  <br/>-Intento de acceso no autorizado por parte de cualquier cliente  <br/>-Error server-side en respuesta a una llamada de cliente válida  <br/> <br/> Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se utiliza y está reservado para uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información de la respuesta de error adicionales.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Contiene la información de disponibilidad para un usuario de buzón único. <br/> <br/> La siguiente es la expresión de XPath 2.0 para este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |Contiene los datos de información y sugerencia de respuesta para solicitado sugerencias de reunión.  <br/><br/> La siguiente es la expresión de XPath 2.0 para este elemento:<br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de fuera de la oficina de un usuario.  <br/><br/> La siguiente es la expresión de XPath 2.0 para este elemento:  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[SetUserOofSettingsResponse](setuseroofsettingsresponse.md) <br/> |Contiene el resultado de un mensaje de [SetUserOofSettingsRequest](setuseroofsettingsrequest.md) intentado. <br/> <br/> La siguiente es la expresión de XPath 2.0 para este elemento:  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El tipo **ResponseMessageType** es común a todas las respuestas de los servicios Web Exchange. El tipo de **ResponseMessageType** se extiende por los tipos complejos siguientes: 
  
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
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
### <a name="version-differences"></a>Diferencias de versión

Los tipos de **ApplyConversationActionResponseMessage** y **DeleteItemResponseMessageType** se introdujeron en Exchange compilación 15.00.0986.00. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)
- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Obtención de disponibilidad del usuario](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

