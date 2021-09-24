---
title: Controlar errores relacionados con la delegación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Descubra cómo controlar errores relacionados con la delegación en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
ms.openlocfilehash: 17e4e7898f5cbed7a6dc524a84db6ba4080eab88
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512299"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Controlar errores relacionados con la delegación en EWS en Exchange

Descubra cómo controlar errores relacionados con la delegación en aplicaciones que desarrolle mediante la API administrada ews o EWS en Exchange.
  
Si la aplicación usa la delegación o agrega o quita delegados, es posible que tenga que controlar los errores relacionados con la delegación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. Estos errores se definen mediante la enumeración [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) de la API administrada ews y el [elemento ResponseCode de](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) EWS. 
  
## <a name="delegation-related-errors"></a>Errores relacionados con la delegación

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Realice una operación en un buzón, carpeta o elemento al que no tenga acceso.  <br/> |Actualizar los permisos del delegado para permitirles tener acceso a la carpeta o elemento mediante una llamada al método de API administrada ews [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) o a la operación [EWS UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) y, a continuación, reintentar la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Modifique un elemento que no tenga privilegios suficientes para modificar.  <br/> |Actualice los permisos de delegado mediante una llamada al método **updateDelegate** EWS Managed API o a la **operación Ews UpdateDelegate** y, a continuación, vuelva a intentar la solicitud.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Intente agregar el propietario del buzón como delegado a su propio buzón.  <br/> |[Agregar un usuario diferente como delegado,](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)no el propietario del buzón.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Agregue el delegado cuando el delegado ya exista.  <br/> |No hacer nada, porque el delegado ya existe para el propietario del buzón. O bien, si está intentando cambiar los permisos de un delegado existente, use el método **UpdateDelegates** o la **operación UpdateDelegate.**  <br/> |
|ErrorNotDelegate  <br/> |Modificar los permisos de delegado para un usuario que no tiene permisos delegados para el buzón.  <br/> |[Agregar al usuario como delegado para](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) el buzón antes de intentar actualizar o quitar sus permisos.  <br/> |
|ErrorDelegateNoUser  <br/> |Modificar permisos de delegado para un usuario que no está en el servicio de dominio de Active Directory (AD DS).  <br/> |Crear el usuario en AD DS o corregir la información de delegado en la solicitud.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Use un delegado para suscribirse a las notificaciones en nombre del propietario del buzón.  <br/> |Suscribirse a las notificaciones como propietario del buzón.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Realice una solicitud de un delegado que tenga una versión de servidor diferente a la del servidor de buzones de correo de la entidad de seguridad.  <br/> |Usar un delegado o agregar un delegado cuyo buzón tiene la misma versión del servidor que el propietario del buzón.  <br/> |
|ErrorMissingEmailAddress  <br/> |Realice una solicitud con una cuenta de delegado que no tenga un buzón.  <br/> |Agregar un buzón a la cuenta del delegado.  <br/> |
   
## <a name="see-also"></a>Ver también


- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Herramientas y recursos para solucionar problemas de aplicaciones EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

