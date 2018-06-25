---
title: Tratamiento de errores relacionados con la delegación en EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 631d364f-e324-4838-a92c-820286f771f8
description: Encuentre información acerca de cómo tratar los errores relacionados con la delegación en las aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
ms.openlocfilehash: 3851709888e3a1087df02eea5d4d58888ad168e3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763006"
---
# <a name="handling-delegation-related-errors-in-ews-in-exchange"></a>Tratamiento de errores relacionados con la delegación en EWS en Exchange

Encuentre información acerca de cómo tratar los errores relacionados con la delegación en las aplicaciones que desarrollar mediante el uso de la API administrada de EWS o EWS en Exchange.
  
Si la aplicación utiliza la delegación o agrega o quita a los delegados, debe controlar los errores relacionados con la delegación. Puede controlar estos errores en tiempo de ejecución, o mientras está desarrollando su aplicación de EWS. Estos errores se definen mediante la enumeración de la API administrada de EWS [depuracuión puede contener](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) y el elemento EWS [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) . 
  
## <a name="delegation-related-errors"></a>Errores relacionados con la delegación

|**Error**|**Se produce al intentar...**|**Controlarla por...**|
|:-----|:-----|:-----|
|ErrorItemNotFound  <br/> ErrorFolderNotFound  <br/> |Realizar una operación en un buzón, carpeta o elemento que no tienen acceso a.  <br/> |Actualización de los permisos del delegado para que puedan tener acceso a la carpeta o elemento llamando el método de la API administrada de EWS [UpdateDelegates](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservice.updatedelegates%28v=exchg.80%29.aspx) o la operación de EWS [UpdateDelegate](http://msdn.microsoft.com/library/03f618ac-ad1a-4772-9b81-c5bb0f12d6ab%28Office.15%29.aspx) y, a continuación, volver a intentar la solicitud.  <br/> |
|ErrorAccessDenied  <br/> |Modificar un elemento que no tiene privilegios suficientes para modificar.  <br/> |Actualizar los permisos de delegado llamando el método de la API administrada de EWS **UpdateDelegate** o la operación de EWS **UpdateDelegate** y, a continuación, volver a intentar la solicitud.  <br/> |
|ErrorDelegateCannotAddOwner  <br/> |Intente agregar el propietario del buzón como delegado a su propio buzón.  <br/> |[Adición de un usuario diferente como delegado](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md), no el propietario del buzón.  <br/> |
|ErrorDelegateAlreadyExists  <br/> |Agregue al delegado cuando el delegado ya existe.  <br/> |No hace nada, porque ya existe el delegado para el propietario del buzón. O bien, si está intentando cambiar los permisos de un delegado existente, a continuación, use el método **UpdateDelegates** o la operación **UpdateDelegate** .  <br/> |
|ErrorNotDelegate  <br/> |Modificar permisos de delegado para un usuario que no tiene ningún permiso de delegado para el buzón de correo.  <br/> |[Agregar el usuario como un delegado](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) para el buzón de correo antes de intentar actualizar o quitar sus permisos.  <br/> |
|ErrorDelegateNoUser  <br/> |Modificar permisos de delegado para un usuario que no está en los servicios de dominio de Active Directory (AD DS).  <br/> |Crear el usuario en AD DS o corregir la información de delegado en la solicitud.  <br/> |
|ErrorSubscriptionDelegateAccessNotSupported  <br/> |Utilice a un delegado para suscribirse a las notificaciones en nombre del propietario del buzón de correo.  <br/> |Suscribirse a notificaciones como propietario del buzón.  <br/> |
|ErrorWrongServerVersionDelegate  <br/> |Realizar una solicitud de un delegado que tiene una versión de servidor diferente que el servidor de buzón de correo de la entidad de seguridad.  <br/> |Uso de un delegado o adición de un delegado cuyo buzón de correo tiene la misma versión de servidor que el propietario del buzón.  <br/> |
|ErrorMissingEmailAddress  <br/> |Realizar una solicitud con una cuenta de delegado que no tiene un buzón de correo.  <br/> |Adición de un buzón de correo a la cuenta del delegado.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

