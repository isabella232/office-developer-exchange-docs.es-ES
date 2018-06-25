---
title: Operación GetUserPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Busque información sobre la EWS GetUserPhoto operación.
ms.openlocfilehash: 4465ac7115d96f5b6ef39e467663c9bf1c70e99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835694"
---
# <a name="getuserphoto-operation"></a>Operación GetUserPhoto

Obtenga información acerca de la operación de EWS **GetUserPhoto** . 
  
La operación **GetUserPhoto** Obtiene una foto de usuario de servicios de dominio de Active Directory (AD DS). 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getuserphoto-operation"></a>Mediante la operación GetUserPhoto

La operación de **RemoveContactFromImList** es una operación sencilla que acepta la dirección de correo electrónico de un usuario y el tamaño de la foto solicitado y devuelve la secuencia de fotografías en la respuesta. 
  
> [!NOTE]
> EWS tiene un SOAP y una operación basada en REST para obtener fotos de usuario. Para obtener información acerca de la interfaz REST, vea [obtener fotos de usuario mediante el uso de EWS en Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx). 
  
### <a name="getuserphoto-operation-soap-headers"></a>Encabezados SOAP de operación de GetUserPhoto

La operación de **GetUserPhoto** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a>Ejemplo de solicitud de operación de GetUserPhoto: obtener fotos de un usuario

El siguiente ejemplo de una solicitud de operación **GetUserPhoto** muestra cómo obtener la foto de un usuario. En este ejemplo se solicita una foto de usuario que es de 48 x 48 píxeles. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013"/>
   </soap:Header>
   <soap:Body>
      <m:GetUserPhoto>
         <m:Email>user1@contoso.com</m:Email>
         <m:SizeRequested>HR48x48</m:SizeRequested>
      </m:GetUserPhoto>
   </soap:Body>
</soap:Envelope>
```

En la solicitud SOAP body, se usan los siguientes elementos:
  
- [GetUserPhoto](getuserphoto.md)
    
- [Correo electrónico (cadena)](email-string.md)
    
- [SizeRequested](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a>Respuesta es correcta de operación GetUserPhoto

En el ejemplo siguiente se muestra una respuesta correcta a una operación de **GetUserPhoto** para obtener fotos de un usuario. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

En la respuesta SOAP body, se usan los siguientes elementos:
  
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [HasChanged](haschanged.md)
    
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a>Respuesta de error de la operación de GetUserPhoto

El elemento envelope de SOAP no devolverá un código de error si intenta obtener una foto de usuario para una dirección de correo electrónico que no existe en la organización. Se devuelve un código de estado HTTP 500 en la respuesta para indicar que la solicitud se ha realizado correctamente. 
  
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)   
- [Obtener fotografías de usuario mediante el uso de EWS en Exchange](http://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

