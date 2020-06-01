---
title: Control de errores relacionados con la delegación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Descubra cómo controlar los errores relacionados con la delegación en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 145783c4e7f49ed6e2aa3a2dbe0d10909e06d7e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455355"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Control de errores relacionados con la delegación en EWS en Exchange

Descubra cómo controlar los errores relacionados con la delegación en las aplicaciones que desarrolle mediante la API administrada de EWS o EWS en Exchange.
  
Si la aplicación usa la delegación o agrega o quita delegados, es posible que deba controlar los errores relacionados con la delegación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. Estos errores los define la enumeración [ServiceError](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) de la API administrada de EWS y el elemento [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) de EWS. 
  
## <a name="delegation-related-errors"></a>Errores relacionados con la delegación

|**Error**|**Se produce cuando se intenta...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Realizar una operación en un buzón, carpeta o elemento a los que no tiene acceso.  <br/> |Actualizar los permisos del delegado para permitirles tener acceso a la carpeta o al elemento mediante una llamada al método de la API administrada de EWS de [UpdateDelegates](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) o a la operación de EWS [UpdateDelegate](https://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) y, a continuación, volver a intentar la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Modifique un elemento que no tenga suficientes privilegios para modificar.  <br/> |Para actualizar los permisos de delegado, llame al método de la API administrada de EWS de **UpdateDelegate** o a la operación de EWS **UpdateDelegate** y, a continuación, vuelva a intentar la solicitud.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Se intentó agregar el propietario del buzón como delegado a su propio buzón.  <br/> |[Agregar un usuario diferente como delegado](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md), no el propietario del buzón.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Agregue el delegado cuando ya exista el delegado.  <br/> |No hace nada, porque el delegado ya existe para el propietario del buzón. O bien, si está intentando cambiar los permisos de un delegado existente, use el método **UpdateDelegates** o la operación **UpdateDelegate** .  <br/> |
|ErrorNotDelegate  <br/> |Modificar permisos de delegado para un usuario que no tiene permisos de delegado para el buzón.  <br/> |[Agregar el usuario como delegado](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) del buzón antes de intentar actualizar o quitar sus permisos.  <br/> |
|ErrorDelegateNoUser  <br/> |Modificar permisos de delegado para un usuario que no está en el servicio de dominio de Active Directory (AD DS).  <br/> |Crear el usuario en AD DS o corregir la información de delegado en la solicitud.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Use un delegado para suscribirse a las notificaciones en nombre del propietario del buzón.  <br/> |Suscripción a notificaciones como propietario del buzón.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Realice una solicitud a partir de un delegado que tenga una versión de servidor distinta a la del servidor de buzones de correo de la entidad de identidad.  <br/> |Uso de un delegado o adición de un delegado cuyo buzón tiene la misma versión de servidor que el propietario del buzón.  <br/> |
|ErrorMissingEmailAddress  <br/> |Realice una solicitud con una cuenta de delegado que no tenga un buzón de correo.  <br/> |Adición de un buzón a la cuenta del delegado.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

