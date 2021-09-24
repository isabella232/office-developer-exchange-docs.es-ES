---
title: ResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseMessage
api_type:
- schema
ms.assetid: bf57265a-d354-4cd7-bbfc-d93e19cbede6
description: El elemento ResponseMessage proporciona información descriptiva sobre el estado de la respuesta de una sola entidad dentro de una solicitud.
ms.openlocfilehash: 21db84698b693fc97c67285c8ca89da028b4e59b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516380"
---
# <a name="responsemessage"></a>ResponseMessage

El **elemento ResponseMessage** proporciona información descriptiva sobre el estado de la respuesta de una sola entidad dentro de una solicitud. 
  
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
|**ResponseClass** <br/> | Representa el estado de la respuesta. <br/><br/>Los siguientes valores son válidos para este atributo:  <br/><br/>- Éxito  <br/>- Advertencia  <br/>- Error  <br/> |
   
#### <a name="responseclass-attribute-values"></a>Valores de atributo ResponseClass

|**Valor**|**Descripción**|
|:-----|:-----|
|Correcto  <br/> |Describe una solicitud que se ha cumplido.  <br/> |
|Advertencia  <br/> | Describe una solicitud que no se ha procesado. Se puede devolver una advertencia si se produjo un error mientras se procesaba un elemento de la solicitud y no se pudieron procesar los elementos posteriores. <br/><br/>Las siguientes son algunas causas posibles para las advertencias:  <br/><br/>- El Exchange está sin conexión durante el lote.  <br/>- El servicio de directorio de Active Directory está sin conexión.  <br/>- Los buzones se mueven.  <br/>- La base de datos de mensajes (MDB) está sin conexión.  <br/>- Una contraseña ha expirado.  <br/>- Se supera una cuota.  <br/> |
|Error  <br/> | Describe una solicitud que no se puede cumplir. <br/><br/>Las siguientes son algunas causas posibles de errores:  <br/><br/>- Atributos o elementos no válidos  <br/>- Atributos o elementos fuera del intervalo  <br/>- Etiqueta desconocida  <br/>- Atributo o elemento no válido en el contexto  <br/>- Intento de acceso no autorizado por cualquier cliente  <br/>- Error del lado servidor en respuesta a una llamada válida del lado cliente  <br/> <br/> Encontrará información sobre el error en los [elementos ResponseCode](responsecode.md) y [MessageText.](messagetext.md)  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MessageText](messagetext.md) <br/> |Proporciona una descripción de texto del estado de la respuesta.  <br/> |
|[ResponseCode](responsecode.md) <br/> |Proporciona un código de error que identifica el error específico que encontró la solicitud.  <br/> |
|[DescriptiveLinkKey](descriptivelinkkey.md) <br/> |Actualmente no se usa y está reservado para su uso futuro. Contiene un valor de 0.  <br/> |
|[MessageXml](messagexml.md) <br/> |Proporciona información adicional de respuesta a errores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FreeBusyResponse](freebusyresponse.md) <br/> |Contiene la información de disponibilidad de un único usuario de buzón. <br/> <br/> A continuación se muestra la expresión XPath 2.0 para este elemento: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray[i]/FreeBusyResponse` <br/> |
|[SuggestionsResponse](suggestionsresponse.md) <br/> |Contiene información de respuesta y datos de sugerencias para sugerencias de reunión solicitadas.  <br/><br/> A continuación se muestra la expresión XPath 2.0 para este elemento:<br/>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse` <br/> |
|[GetUserOofSettingsResponse](getuseroofsettingsresponse.md) <br/> |Contiene los resultados de la respuesta y la configuración de OOF de un usuario.  <br/><br/> A continuación se muestra la expresión XPath 2.0 para este elemento:  <br/><br/>  `/GetUserOofSettingsResponse` <br/> |
|[SetUserOofSettingsResponse](setuseroofsettingsresponse.md) <br/> |Contiene el resultado de un intento [de mensaje SetUserOofSettingsRequest.](setuseroofsettingsrequest.md) <br/> <br/> A continuación se muestra la expresión XPath 2.0 para este elemento:  <br/><br/>  `/SetUserOofSettingsResponse` <br/> |
   
## <a name="remarks"></a>Comentarios

El **tipo ResponseMessageType** es común a todas Exchange respuestas de servicios web. El **tipo ResponseMessageType** se amplía con los siguientes tipos complejos: 
  
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
    
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
### <a name="version-differences"></a>Diferencias de versión

Los **tipos ApplyConversationActionResponseMessage** y **DeleteItemResponseMessageType** se introdujeron en Exchange compilación 15.00.0986.00. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserAvailability](getuseravailability-operation.md)
- [Operación SetUserOofSettings](setuseroofsettings-operation.md)
- [Operación GetUserOofSettings](getuseroofsettings-operation.md)
- [Obtener disponibilidad del usuario](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

