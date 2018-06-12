---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información sobre cómo y cuándo utilizar la representación en las aplicaciones de servicio de Exchange.
ms.openlocfilehash: f8a215874475034f0d147b80a05cae414e6438f9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763189"
---
# <a name="impersonation-and-ews-in-exchange"></a>Suplantación y EWS en Exchange

Obtenga información sobre cómo y cuándo utilizar la representación en las [aplicaciones de servicio](ews-application-types.md)de Exchange.
  
Puede habilitar a los usuarios tener acceso a los buzones de otros usuarios en uno de tres maneras:
  
- Adición de delegados y especificando los permisos para cada delegado.
    
- Mediante la modificación de permisos de carpeta directamente.
    
- Mediante el uso de suplantación.
    
¿Cuándo debería elegir suplantación a través de los permisos de delegación o carpeta? Las siguientes instrucciones le ayudará a decidir:
  
- Use los permisos de carpeta cuando desee proporcionar un acceso de usuario a una carpeta, pero no desea que el usuario tenga permisos "enviar en nombre de". 
    
- Usar acceso de delegado al que desea conceder permiso a un usuario para llevar a cabo el trabajo en nombre de otro usuario. Normalmente, se trata de un permiso de uno a uno o uno a algunos - por ejemplo, un auxiliar administrativo único administrar el calendario de un administrador o un programador de habitación individual administrar los calendarios para un grupo de las salas de reuniones.
    
- Usar suplantación cuando tiene una aplicación de servicio que necesita tener acceso a varios buzones de correo y "actuar como" propietario del buzón.
    
Suplantación de es la mejor opción cuando se trata con varios buzones porque fácilmente puede otorgar un acceso de cuenta de servicio para cada buzón de correo en una base de datos. Permisos de delegación y carpeta están mejor cuando solo va a conceder acceso a unos pocos usuarios, debido a que se debe agregar permisos individualmente a cada buzón de correo. La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.
  
**En la figura 1. Formas de acceso a los buzones de otros usuarios**

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
Suplantación es ideal para aplicaciones que se conectan a Exchange Online, Exchange Online como parte de Office 365, y las versiones de Exchange local y realiza operaciones, como el archivado de correo electrónico, configuración OOF automáticamente para los usuarios de vacaciones o cualquier otra tarea que requiere que la aplicación que actúe como el propietario de un buzón de correo. Cuando una aplicación utiliza la suplantación para enviar un mensaje, aparece el correo electrónico que se envíen desde el propietario del buzón. No hay ninguna forma para el destinatario que debe conocer que el correo se ha enviado por la cuenta de servicio. La delegación, por otro lado, da a otro permiso de cuenta de buzón de correo para que actúe en nombre de un propietario del buzón. Cuando se envía un mensaje de correo electrónico por parte de un delegado, el valor "desde" identifica el propietario del buzón y el valor de "sender" identifica al delegado que envía el correo. 
  
## <a name="security-considerations-for-impersonation"></a>Consideraciones de seguridad para la suplantación

Suplantación permite a un autor de la llamada suplantar una cuenta de usuario determinado. Esto permite que el autor de la llamada realizar operaciones con los permisos que están asociados con la cuenta suplantada, en lugar de los permisos que están asociados con la cuenta del llamador. Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:
  
- Sólo las cuentas que se han concedido la función **ApplicationImpersonation** por un administrador de Exchange server pueden utilizar suplantación. 
    
- Debe crear un ámbito de administración que limita la suplantación de un grupo de cuentas especificado. Si no se crea un ámbito de administración, se concede a la función **ApplicationImpersonation** a todas las cuentas de una organización. 
    
- Normalmente, la función **ApplicationImpersonation** se concede a una cuenta de servicio dedicada a una aplicación en particular o el grupo de aplicaciones, en lugar de una cuenta de usuario. Puede crear tantas o tan solo cuentas de servicio que necesite. 
    
Puede leer más información acerca de la [configuración de suplantación](how-to-configure-impersonation.md), pero se debe trabajar con el Administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se crean con el [acceso y los permisos](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx) que cumplen los requisitos de seguridad de su organización. 
  
## <a name="in-this-section"></a>En esta sección

- [Configurar la suplantación](how-to-configure-impersonation.md)
    
- [Identificación de la cuenta para suplantar a](how-to-identify-the-account-to-impersonate.md)
    
- [Agregar citas mediante el uso de la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a>Ver también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Permisos de Exchange 2013](http://technet.microsoft.com/en-us/library/dd351175%28v=exchg.150%29.aspx)
    

