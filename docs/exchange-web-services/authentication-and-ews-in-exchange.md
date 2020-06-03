---
title: Autenticación y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: Obtenga información que le ayude a elegir el estándar de autenticación adecuado para su aplicación de EWS dirigida a Exchange.
localization_priority: Priority
ms.openlocfilehash: 69018b6f88fc80e1e18edd96ed0e16d52064572d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528485"
---
# <a name="authentication-and-ews-in-exchange"></a>Autenticación y EWS en Exchange

Obtenga información que le ayude a elegir el estándar de autenticación adecuado para su aplicación de EWS dirigida a Exchange.
  
La autenticación es una parte clave de la aplicación de servicios web Exchange (EWS). Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange que comienzan con Exchange Server 2013 admiten protocolos de autenticación Web estándar para ayudar a proteger la comunicación entre la aplicación y el servidor de Exchange.
  
Si su objetivo es Exchange Online, el método de autenticación que elija debe usar HTTPS para cifrar las solicitudes y respuestas que envía la aplicación. Aunque puede usar HTTP con servidores de Exchange locales, le recomendamos que use HTTPS para cualquier solicitud que la aplicación envíe a un extremo de EWS para ayudar a proteger la comunicación entre la aplicación y un servidor de Exchange.
  
Exchange proporciona las siguientes opciones de autenticación para que elija: 
  
- OAuth 2,0 (solo en Exchange Online)
    
- NTLM (solo Exchange local)
    
- Básico (ya no se recomienda)
    
El método de autenticación que elija dependerá de los requisitos de seguridad de su organización, independientemente de si usa Exchange online o Exchange local y si tiene acceso a un proveedor de terceros que pueda emitir tokens de OAuth. En este artículo se proporciona información que le ayudará a seleccionar el estándar de autenticación adecuado para su aplicación.
  
## <a name="oauth-authentication"></a>Autenticación OAuth

Se recomienda que todas las aplicaciones nuevas usen el estándar de OAuth para conectarse a los servicios de Exchange Online. La ventaja de la seguridad sobre la autenticación básica merece la pena el trabajo adicional necesario para implementar OAuth en la aplicación. Sin embargo, para el registro también hay algunas desventajas que debe tener en cuenta.
  
**Tabla 1. Ventajas y desventajas del uso de OAuth**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| OAuth es un protocolo de autenticación estándar del sector.<br/><br/>La autenticación la administra un proveedor de terceros. La aplicación no tiene que recopilar y almacenar las credenciales de Exchange.<br/><br/>Menos preocupaciones para usted, porque la aplicación solo recibe un token opaco del proveedor de autenticación; por lo tanto, una infracción de seguridad en la aplicación solo puede exponer el token, no las credenciales de Exchange del usuario.  <br/> | OAuth depende de un proveedor de autenticación de terceros. Esto puede imponer costos adicionales a su organización o a los clientes.<br/><br/>El estándar de OAuth es más difícil de implementar que la autenticación básica.<br/><br/>Para implementar OAuth, debe integrar la aplicación con el proveedor de autenticación y el servidor de Exchange.  <br/> |
   
Para minimizar las desventajas, puede usar la [biblioteca de autenticación de Microsoft Azure ad](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries) (Adal) para autenticar a los usuarios en los servicios de dominio de Active Directory (AD DS) en la nube o en el entorno local y, a continuación, obtener tokens de acceso para proteger las llamadas a un servidor de Exchange. Exchange Online requiere tokens emitidos por el servicio de Azure Active Directory, que es compatible con ADAL; sin embargo, puede usar cualquier biblioteca de terceros. 
  
Para obtener más información sobre el uso de la autenticación OAuth en la aplicación de EWS, vea los siguientes recursos:
  
- [Versión de prueba de Office 365](https://docs.microsoft.com/office/developer-program/office-365-developer-program)para configurar un servidor de Exchange y usarlo para probar la aplicación cliente.
    
- [Biblioteca de autenticación de Azure AD para .NET](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [Configurar Azure Active Directory](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx), para habilitar la aplicación para que use tokens de OAuth para la autenticación.
    
- Revise el código de ejemplo en [Authenticate a EWS Application by Using OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md) para obtener un código de ejemplo que puede estudiar. 
    
## <a name="ntlm-authentication"></a>Autenticación NTLM

La autenticación NTLM solo está disponible para los servidores de Exchange local. Para las aplicaciones que se ejecutan dentro del Firewall corporativo, la integración entre la autenticación NTLM y .NET Framework proporciona un medio integrado para autenticar la aplicación. 
  
**Tabla 2. Ventajas y desventajas del uso de la autenticación NTLM**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Funciona de una "vez en el equipo" con su servidor de Exchange. Puede configurar el acceso a los servicios de Exchange mediante un [cmdlet del shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Utiliza el objeto [CredentialCache](https://msdn2.microsoft.com/library/615e0wsd) de .NET Framework para obtener automáticamente las credenciales del usuario.<br/><br/>[Hay disponibles ejemplos de código](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que usan las credenciales del usuario que ha iniciado sesión para la autenticación en un servidor de Exchange local.  <br/> | Los usuarios deben iniciar sesión en un dominio para usar la autenticación NTLM.<br/><br/>Puede resultar difícil tener acceso a las cuentas de correo electrónico que no están asociadas a la cuenta de dominio del usuario.<br/><br/>Las aplicaciones de servicio deben tener una cuenta de dominio para aprovechar la autenticación NTLM.  <br/> |

   
## <a name="basic-authentication"></a>Autenticación básica

La autenticación básica proporciona un nivel de seguridad básico y básico para la aplicación cliente. Se recomienda que todas las aplicaciones nuevas usen el protocolo NTLM o OAuth para la autenticación; sin embargo, la autenticación básica puede ser la elección correcta para la aplicación en algunas circunstancias.
  
**Tabla 3. Ventajas y desventajas del uso de la autenticación básica**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Funciona de una "vez en el equipo" con su servidor de Exchange. Puede configurar el acceso a los servicios de Exchange mediante un [cmdlet del shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Las aplicaciones de Windows pueden usar las credenciales predeterminadas del usuario que ha iniciado sesión.<br/><br/>[Hay disponibles muchos ejemplos de código](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que muestran cómo llamar a EWS mediante la autenticación básica.  <br/> | Requiere que la aplicación recopile y almacene las credenciales del usuario.<br/><br/>Debe desactivar la autenticación NTLM si desea obligar a todos los usuarios a usar la autenticación básica.<br/><br/>Si se produce una infracción de seguridad en la aplicación, puede exponer la dirección de correo electrónico y la contraseña del usuario al atacante.  <br/> |
   
Debe decidir si la autenticación básica cumple con los requisitos de seguridad de la organización y los clientes. La autenticación básica puede ser la opción adecuada si desea evitar tareas de configuración extensivas, por ejemplo, para aplicaciones de prueba sencillas o de demostración.
  
## <a name="see-also"></a>Vea también

- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Adición de inicio de sesión a la aplicación Web mediante Microsoft Azure AD](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)    
- [Controlar el acceso de la aplicación cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)   
- [Tokens y tipos de notificación admitidos](https://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
 