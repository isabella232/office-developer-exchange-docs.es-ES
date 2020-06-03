---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información sobre cómo y Cuándo usar la suplantación en las aplicaciones de servicio de Exchange.
localization_priority: Priority
ms.openlocfilehash: 8151b3d83421786d99ee0c82eaf4f7a5c0721f25
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466615"
---
# <a name="impersonation-and-ews-in-exchange"></a>Suplantación y EWS en Exchange

Obtenga información sobre cómo y Cuándo usar la suplantación en [las aplicaciones de servicio](ews-application-types.md)de Exchange.
  
Puede habilitar a los usuarios para que tengan acceso a los buzones de otros usuarios de una de estas tres maneras:
  
- Mediante la adición de delegados y la especificación de permisos para cada delegado.
    
- Modificando los permisos de carpeta directamente.
    
- Mediante la suplantación.
    
¿Cuándo debe elegir la suplantación a través de la delegación o los permisos de carpeta? Las siguientes instrucciones le ayudarán a decidir:
  
- Use permisos de carpeta cuando desee proporcionar a un usuario acceso a una carpeta pero no desea que el usuario tenga permisos "enviar en nombre de". 
    
- Use el acceso delegado cuando desee conceder a un usuario permiso para realizar el trabajo en nombre de otro usuario. Normalmente se trata de un permiso de uno a uno o de uno a uno reducido, por ejemplo, un único asistente administrativo que administra el calendario de un administrador o un único programador de salas que administra los calendarios de un grupo de salas de reuniones.
    
- Use la suplantación cuando tiene una aplicación de servicio que necesita tener acceso a varios buzones de correo y "actuar como" el propietario del buzón.
    
La suplantación es la mejor opción cuando se trabaja con varios buzones, ya que se puede conceder fácilmente un acceso de cuenta de servicio a todos los buzones de una base de datos. La delegación y los permisos de carpeta son los mejores cuando solo concede acceso a algunos usuarios, porque tiene que agregar permisos individualmente a cada buzón. La figura 1 muestra algunas de las diferencias entre cada tipo de acceso.
  
**Figura 1. Formas de tener acceso a los buzones de otros usuarios**

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
La suplantación es ideal para las aplicaciones que se conectan a Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange, y realizan operaciones, como el archivado de correo electrónico, la configuración automática del OOF para los usuarios de vacaciones o cualquier otra tarea que requiera que la aplicación actúe como propietario de un buzón de correo. Cuando una aplicación utiliza la suplantación para enviar un mensaje, parece que el correo electrónico se envía desde el propietario del buzón. No hay forma de que el destinatario sepa que el correo se envió mediante la cuenta de servicio. Por otra parte, la delegación da a otro permiso de cuenta de buzón de correo que actúe en nombre de un propietario del buzón. Cuando un delegado envía un mensaje de correo electrónico, el valor "de" identifica al propietario del buzón y el valor "Sender" identifica al delegado que envió el correo. 
  
## <a name="security-considerations-for-impersonation"></a>Consideraciones de seguridad para la suplantación

La suplantación permite al autor de la llamada suplantar a una cuenta de usuario determinada. Esto permite al autor de la llamada realizar operaciones con los permisos asociados con la cuenta suplantada, en lugar de los permisos asociados con la cuenta del autor de la llamada. Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:
  
- Solo las cuentas a las que un administrador de Exchange Server ha concedido el rol **ApplicationImpersonation** puede usar la suplantación. 
    
- Debe crear un ámbito de administración que limite la suplantación a un grupo de cuentas especificado. Si no crea un ámbito de administración, el rol **ApplicationImpersonation** se concede a todas las cuentas de una organización. 
    
- Normalmente, el rol **ApplicationImpersonation** se concede a una cuenta de servicio dedicada a una aplicación o grupo de aplicaciones en particular, en lugar de una cuenta de usuario. Puede crear tantas o tan pocas cuentas de servicio como necesite. 
    
Puede obtener más información acerca de la configuración de la [suplantación](how-to-configure-impersonation.md), pero debe colaborar con el administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se crean con los [permisos y el acceso](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) que cumplen los requisitos de seguridad de su organización. 
  
## <a name="in-this-section"></a>En esta sección

- [Configurar la suplantación](how-to-configure-impersonation.md)
    
- [Identificación de la cuenta que se va a suplantar](how-to-identify-the-account-to-impersonate.md)
    
- [Adición de citas mediante la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Permisos de Exchange 2013](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

