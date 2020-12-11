---
title: Autenticación y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: Encuentre información que le ayude a elegir el estándar de autenticación adecuado para su aplicación EWS que dirigida a Exchange.
localization_priority: Priority
ms.openlocfilehash: 0b35921f33b935f9a5a490e15d4e76d1a3e3c9dc
ms.sourcegitcommit: 843a2e030a94b12aec70c553ca4e06e39ac02d82
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/09/2020
ms.locfileid: "49603837"
---
# <a name="authentication-and-ews-in-exchange"></a>Autenticación y EWS en Exchange

Encuentre información que le ayude a elegir el estándar de autenticación adecuado para su aplicación EWS que dirigida a Exchange.
  
La autenticación es una parte clave de la aplicación de servicios Web Exchange (EWS). Exchange Online, Exchange Online como parte de Office 365 y las versiones locales de Exchange a partir de Exchange Server 2013 admiten protocolos de autenticación web estándar para ayudar a proteger la comunicación entre la aplicación y el servidor de Exchange.
  
Si está dirigido a Exchange Online, el método de autenticación que elija debe usar HTTPS para cifrar las solicitudes y respuestas que envía la aplicación. Aunque se puede usar HTTP con servidores locales de Exchange, se recomienda usar HTTPS para cualquier solicitud que la aplicación envíe a un punto de conexión de EWS para ayudar a proteger la comunicación entre la aplicación y un servidor de Exchange.
  
Exchange ofrece las siguientes opciones de autenticación entre las que elegir: 
  
- OAuth 2.0 (solo Exchange Online)
    
- NTLM (solo Exchange local)
    
- Básica (ya no se recomienda)
    
El método de autenticación que elija dependerá de los requisitos de seguridad de su organización, si usa Exchange Online o Exchange local, y si tiene acceso a un proveedor de terceros que pueda emitir tokens de OAuth. Este artículo proporciona información que le ayudará a seleccionar el estándar de autenticación adecuado para su aplicación.
  
## <a name="oauth-authentication"></a>Autenticación OAuth

Se recomienda que todas las aplicaciones nuevas usen el estándar de OAuth para conectarse a los servicios de Exchange Online. La ventaja de la seguridad sobre la autenticación básica compensa el trabajo adicional que se necesita para implementar OAuth en la aplicación. No obstante, en el caso de los registros también se deben tener en cuenta algunas desventajas.
  
**Tabla 1. Ventajas y desventajas del uso de OAuth**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| OAuth es un protocolo de autenticación estándar de la industria.<br/><br/>La autenticación la administra un proveedor de terceros. La aplicación no tiene que recopilar ni almacenar las credenciales de Exchange.<br/><br/>Menos preocupaciones para usted, ya que la aplicación solo recibe un token opaco del proveedor de autenticación. Por lo tanto, una vulneración de seguridad de la aplicación solo puede revelar el token, no las credenciales de Exchange del usuario.  <br/> | OAuth se basa en un proveedor de autenticación de terceros. Esto puede suponer un coste adicional a su organización o a sus clientes.<br/><br/>El estándar OAuth es más difícil de implementar que la autenticación básica.<br/><br/>Para implementar OAuth, debe integrar la aplicación tanto con el proveedor de autenticación como con el servidor de Exchange.  <br/> |
   
Para ayudar a minimizar las desventajas, puede usar la [Biblioteca de autenticación de Microsoft Azure AD](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) para autenticar a los usuarios en Active Directory Domain Services (AD DS) en la nube o localmente y luego obtener tokens de acceso para proteger llamadas a un servidor Exchange. Exchange Online requiere tokens emitidos por el servicio Azure Active Directory, que es compatible con ADAL; sin embargo, puede utilizar cualquier biblioteca de terceros. 
  
Para más información sobre el uso de la autenticación OAuth en la aplicación EWS, vea los recursos siguientes:
  
- [Prueba de Office 365](https://docs.microsoft.com/office/developer-program/office-365-developer-program), para configurar un servidor de Exchange y usarlo para probar la aplicación cliente.
    
- [Biblioteca de Autenticación de Azure AD para .NET](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [Configure Azure Active Directory](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx), para permitir que la aplicación use los tokens de OAuth para la autenticación.
    
- Revise el código de ejemplo en [Autenticar una aplicación EWS utilizando OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md) como ejemplo de código que puede estudiar. 
    
## <a name="ntlm-authentication"></a>Autenticación NTLM

La autenticación NTLM solo está disponible para los servidores de Exchange local. En el caso de las aplicaciones que se ejecutan en el firewall corporativo, la integración entre la autenticación NTLM y .NET Framework proporciona un medio integrado para autenticar su aplicación. 
  
**Tabla 2. Ventajas y desventajas del uso de la autenticación NTLM**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Está preparado para funcionar con su servidor Exchange. Puede configurar el acceso a los servicios de Exchange con un [cmdlet del Shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Usa el objeto [CredentialCache](https://msdn2.microsoft.com/library/615e0wsd) de .NET Framework para obtener automáticamente las credenciales del usuario.<br/><br/>Hay [ejemplos de código disponibles](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que utilizan las credenciales del usuario que inició sesión para la autenticación en un servidor de Exchange local.  <br/> | Los usuarios tienen que haber iniciado sesión en un dominio para usar la autenticación NTLM.<br/><br/>Puede resultar difícil acceder a las cuentas de correo electrónico que no están asociadas a la cuenta de dominio del usuario.<br/><br/>Las aplicaciones de servicio deben tener una cuenta de dominio para poder aprovechar la autenticación NTLM.  <br/> |

   
## <a name="basic-authentication"></a>Autenticación básica

La autenticación básica proporciona un nivel de seguridad bueno y básico para la aplicación cliente. Se recomienda que todas las aplicaciones nuevas usen el protocolo NTLM o el protocolo OAuth para la autenticación; sin embargo, la autenticación básica puede ser la elección adecuada para la aplicación en algunas circunstancias.
  
**Tabla 3. Ventajas y desventajas del uso de la autenticación básica**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Está preparado para funcionar con su servidor Exchange. Puede configurar el acceso a los servicios de Exchange con un [cmdlet del Shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Las aplicaciones de Windows pueden usar las credenciales predeterminadas del usuario que ha iniciado sesión.<br/><br/>Hay [disponibles varios ejemplos de código](https://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que muestran cómo se llama a EWS con la autenticación básica.  <br/> | Requiere que la aplicación recopile y almacene las credenciales del usuario.<br/><br/>Debe desactivar la autenticación NTLM si quiere obligar a todos los usuarios a usar la autenticación básica.<br/><br/>Si se produce una vulneración en la seguridad de la aplicación, puede mostrar la dirección de correo electrónico y la contraseña del usuario al atacante.  <br/> |
   
Debe decidir si la autenticación básica cumple con los requisitos de seguridad de su organización y clientes. La autenticación básica puede ser la opción adecuada si quiere evitar tareas de configuración extensas, por ejemplo, para aplicaciones de demostración o de pruebas simples.

> [!NOTE]
> La autenticación básica ya no es compatible con EWS para conectarse a Exchange Online. Use la autenticación OAuth en todas las aplicaciones de EWS nuevas o existentes para conectarse a Exchange Online. La autenticación OAuth para EWS solo está disponible en Exchange como parte de Microsoft 365. Las aplicaciones de EWS que usan OAuth deben registrarse primero con Azure Active Directory.
  
## <a name="see-also"></a>Consulte también
- [Autenticar una aplicación EWS mediante OAuth](how-to-authenticate-an-ews-application-by-using-oauth.md)
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Agregar el inicio de sesión a la aplicación web con Microsoft Azure AD](https://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)    
- [Controlar el acceso de la aplicación de cliente a EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md).   
- [Tipos de notificaciones y token admitidos](https://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
 
