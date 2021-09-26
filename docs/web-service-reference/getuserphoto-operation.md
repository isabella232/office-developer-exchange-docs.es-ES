---
title: Operación GetUserPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f6e8143d-4235-428e-8f9c-ab6e9b1cfa6e
description: Busque información sobre la operación EWS GetUserPhoto.
ms.openlocfilehash: 6dd1ce73d6291e60ce188b98b917a4c79ce792b5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59547487"
---
# <a name="getuserphoto-operation"></a>Operación GetUserPhoto

Busque información sobre la **operación EWS GetUserPhoto.** 
  
La **operación GetUserPhoto** obtiene una foto de usuario de Servicios de dominio de Active Directory (AD DS). 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getuserphoto-operation"></a>Uso de la operación GetUserPhoto

La **operación RemoveContactFromImList** es una operación sencilla que acepta la dirección de correo electrónico de un usuario y el tamaño de foto solicitado y devuelve la secuencia de fotos en la respuesta. 
  
> [!NOTE]
> EWS tiene un SOAP y una operación basada en REST para obtener fotos de usuario. Para obtener información sobre la interfaz REST, vea [Get user photos by using EWS in Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx). 
  
### <a name="getuserphoto-operation-soap-headers"></a>Encabezados SOAP de operación GetUserPhoto

La **operación GetUserPhoto** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getuserphoto-operation-request-example-get-a-users-photo"></a>Ejemplo de solicitud de operación GetUserPhoto: Obtener la foto de un usuario

En el siguiente ejemplo de una **solicitud de operación GetUserPhoto** se muestra cómo obtener la foto de un usuario. En este ejemplo se solicita una foto de usuario de 48 x 48 píxeles. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Los siguientes elementos se usan en el cuerpo SOAP de la solicitud:
  
- [GetUserPhoto](getuserphoto.md)
    
- [Email (Cadena)](email-string.md)
    
- [SizeRequested](sizerequested.md)
    
## <a name="successful-getuserphoto-operation-response"></a>Respuesta correcta de la operación GetUserPhoto

En el ejemplo siguiente se muestra una respuesta correcta a una **operación GetUserPhoto** para obtener la foto de un usuario. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserPhotoResponse ResponseClass="Success" 
                            xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <HasChanged>true</HasChanged>
         <PictureData>/9j/4AAQSkZJRgABAQEAYABgAAD/02</PictureData>
      </GetUserPhotoResponse>
   </s:Body>
</s:Envelope>

```

Los siguientes elementos se usan en el cuerpo SOAP de la respuesta:
  
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [HasChanged](haschanged.md)
    
- [GetUserPhotoResponse](getuserphotoresponse.md)
    
## <a name="getuserphoto-operation-error-response"></a>Respuesta de error de operación GetUserPhoto

El sobre SOAP no devolverá un código de error si se intenta obtener una foto de usuario para una dirección de correo electrónico que no existe en la organización. Se devolverá un código de estado HTTP 500 en la respuesta para indicar que la solicitud no se ha hecho correctamente. 
  
## <a name="see-also"></a>Consulte también

- [Operaciones ews en Exchange](ews-operations-in-exchange.md)   
- [Obtener fotos de usuario mediante EWS en Exchange](https://msdn.microsoft.com/library/f86d1099-1f57-47dc-abf2-4d5ae4e900a9%28Office.15%29.aspx)
    

