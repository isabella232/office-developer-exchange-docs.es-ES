---
title: Suplantación y EWS en Exchange
manager: sethgros
ms.date: 08/24/2020
ms.audience: Developer
ms.assetid: 7e1ea63c-eb29-43d2-827f-2f2b1846483b
description: Obtenga información acerca de cómo y cuándo usar la suplantación en las aplicaciones de servicio de Exchange.
localization_priority: Priority
ms.openlocfilehash: da35fb04f316c21a1c85c71b789b7f1485653466
ms.sourcegitcommit: 636c05a929279812c6ef87d75b01c166a4a05584
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2020
ms.locfileid: "47254975"
---
# <a name="impersonation-and-ews-in-exchange"></a>Suplantación y EWS en Exchange

Obtenga información acerca de cómo y cuándo usar la suplantación en las [aplicaciones de servicio de Exchange](ews-application-types.md).
  
Para permitir a los usuarios acceder a los buzones de otros usuarios, puede hacer lo siguiente:
  
- Agregar delegados y especificar permisos para cada uno.
    
- Modificar los permisos de carpeta directamente.
    
- Utilizar la suplantación.
    
¿Cuándo debería elegir la suplantación en lugar de la delegación o de modificar los permisos de carpeta? Las siguientes instrucciones le ayudarán a decidir:
  
- Utilice los permisos de carpeta cuando quiera proporcionar a un usuario acceso a una carpeta sin que dicho usuario tenga permisos para "Enviar en nombre de". 
    
- Use el acceso delegado cuando quiera conceder permiso a un usuario para realizar trabajo en nombre de otro usuario. Por lo general, se trata de un permiso que se da a uno o a pocos usuarios; por ejemplo, un único asistente administrativo que administra el calendario en nombre de un administrador o un único programador de sala que administra los calendarios de un grupo de salas de reuniones.
    
- Emplee la suplantación cuando tenga una aplicación de servicio que necesite tener acceso a varios buzones de correo y "actuar como" el propietario del buzón.
    
La suplantación es la mejor opción cuando se utilizan varios buzones, ya que permite conceder fácilmente acceso de cuenta de servicio a cada buzón de una base de datos. Los permisos de carpeta y delegación son óptimos cuando solo concede acceso a unos pocos usuarios, porque tiene que agregar permisos de forma individual para cada buzón. En la figura 1 se muestran algunas de las diferencias entre cada tipo de acceso.
  
**Ilustración 1. Formas de acceder a los buzones de otros usuarios**

![Un diagrama que muestra los tipos de acceso a los buzones, la relación entre los propietarios de los buzones y el delegado de cada tipo, y el tipo de permiso. Enviar en nombre de los permisos para delegación y/o permisos de carpeta. Enviar como permisos para suplantación.](media/Ex15_Delegate_Overview.png)
  
La suplantación es ideal para aplicaciones que se conectan a Exchange Online, Exchange Online como parte de Office 365 y a las versiones locales de Exchange y que realizan operaciones como archivar correo electrónico, establecer automáticamente acciones de fuera de la oficina para los usuarios de vacaciones, o realizar cualquier otra tarea que requiera que la aplicación actúe como propietario de un buzón. Cuando una aplicación usa la suplantación para enviar un mensaje, el correo electrónico aparece como si se hubiera enviado desde el propietario del buzón. Al destinatario le resulta imposible saber que el correo lo envió la cuenta de servicio. Por otra parte, la delegación concede a otra cuenta de buzón permiso para actuar en nombre del propietario del buzón. Cuando un delegado envía un mensaje de correo electrónico, el valor "de" identifica al propietario del buzón y el valor "remitente" identifica al delegado que envió el correo. 
  
## <a name="security-considerations-for-impersonation"></a>Consideraciones de seguridad para la suplantación

La suplantación permite a un autor de llamada suplantar una cuenta de usuario determinada. Esto permite al autor de llamada realizar operaciones mediante los permisos asociados a la cuenta suplantada, en lugar de los permisos asociados con la cuenta del autor de llamada. Por este motivo, debe tener en cuenta las siguientes consideraciones de seguridad:
  
- Solo las cuentas a las que un administrador de Exchange Server ha concedido el rol **ApplicationImpersonation** pueden usar la suplantación. 
    
- Debe crear un ámbito de administración que limite la suplantación a un grupo específico de cuentas. Si no crea un ámbito de administración, el rol **ApplicationImpersonation** se concederá a todas las cuentas de la organización. 
    
- Por lo general, el rol **ApplicationImpersonation** se otorga a una cuenta de servicio dedicada a una aplicación o a un grupo de aplicaciones en particular, en lugar de a una cuenta de usuario. Puede crear todas las cuentas de servicio que necesite. 
    
Puede obtener más información acerca de la [configuración de la suplantación](how-to-configure-impersonation.md), pero debe trabajar con su administrador de Exchange para asegurarse de que las cuentas de servicio que necesita se creen con los [permisos y el acceso](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx) que cumplan los requisitos de seguridad de su organización. 
  
## <a name="in-this-section"></a>En esta sección

- [Configurar la suplantación](how-to-configure-impersonation.md)
    
- [Identificar la cuenta a suplantar](how-to-identify-the-account-to-impersonate.md)
    
- [Agregar citas mediante la suplantación de Exchange](how-to-add-appointments-by-using-exchange-impersonation.md)

## <a name="performance-considerations-for-ews-impersonation"></a>Consideraciones de rendimiento para la suplantación de EWS

Cuando se usa la suplantación de EWS, X-AnchorMailbox siempre debe establecerse correctamente.  De lo contrario, es posible que reciba los mensajes de error 500 o 503 en ocasiones. Resulta fundamental para el rendimiento y las notificaciones de Exchange Online y Exchange 2013.  Si no lo establece, puede que se tarde el doble o más en completar la llamada. En algunos casos, puede recibir también tiempos de espera. 
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Acceso delegado y EWS en Exchange](delegate-access-and-ews-in-exchange.md)
    
- [Permisos de Exchange 2013](https://technet.microsoft.com/library/dd351175%28v=exchg.150%29.aspx)
    

