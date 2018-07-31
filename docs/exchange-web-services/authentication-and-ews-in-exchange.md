---
title: Autenticación y EWS en Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9a83df96-aca0-42b3-b8f5-2b414f0363f1
description: Obtenga información que le ayudarán a elegir el estándar de autenticación correcto para la aplicación de EWS dirigido a Exchange.
ms.openlocfilehash: a4aae4678f1d6ffa5c08350f0bcccce5a4885f20
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353668"
---
# <a name="authentication-and-ews-in-exchange"></a>Autenticación y EWS en Exchange

Obtenga información que le ayudarán a elegir el estándar de autenticación correcto para la aplicación de EWS dirigido a Exchange.
  
La autenticación es una parte clave de la aplicación de servicios Web de Exchange (EWS). Exchange Online como parte de Office 365 y las versiones locales de Exchange a partir de Exchange Server 2013, Exchange Online admite los protocolos de autenticación web estándar para ayudar a proteger la comunicación entre la aplicación y el servidor de Exchange.
  
Si posea Exchange Online, el método de autenticación que elija debe usar HTTPS para cifrar las solicitudes y las respuestas que envía la aplicación. Aunque puede usar HTTP con los servidores locales de Exchange, se recomienda usar HTTPS para cualquier solicitud de que la aplicación se envía a un extremo EWS para ayudar a una comunicación segura entre la aplicación y un servidor de Exchange.
  
Exchange proporciona las siguientes opciones de autenticación para elegir entre: 
  
- OAuth 2.0 (sólo para Exchange Online)
    
- NTLM (Exchange sólo locales)
    
- Basic (ya no se recomienda)
    
El método de autenticación que elija depende de los requisitos de seguridad de la organización, si está utilizando Exchange Online o Exchange local y, si tiene acceso a un proveedor de terceros que puede emitir tokens de OAuth. En este artículo se proporciona información que le ayudarán a seleccionar el estándar de autenticación es el adecuado para su aplicación.
  
## <a name="oauth-authentication"></a>Autenticación de OAuth

Se recomienda que todas las nuevas aplicaciones de usan el estándar OAuth para conectarse a servicios de Exchange Online. La ventaja de la seguridad a través de la autenticación básica es vale la pena el trabajo adicional necesario para implementar OAuth en su aplicación. Para el registro, sin embargo, también existen algunas desventajas que se deben tener en cuenta.
  
**La tabla 1. Ventajas y desventajas del uso de OAuth**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| OAuth es un protocolo de autenticación estándar del sector.<br/><br/>La autenticación está administrada por un proveedor de terceros. La aplicación no tiene que recopilar y almacenar las credenciales de Exchange.<br/><br/>Menos preocupaciones para usted, debido a que la aplicación sólo recibe un token opaco desde el proveedor de autenticación; por lo tanto, una infracción de seguridad de la aplicación sólo puede exponer el token, no las credenciales del usuario Exchange.  <br/> | OAuth se basa en un proveedor de autenticación de otros fabricantes. Esto puede suponer costes adicionales en su organización o a sus clientes.<br/><br/>El estándar OAuth es más difícil de implementar que la autenticación básica.<br/><br/>Para implementar OAuth, debe integrar la aplicación con el proveedor de autenticación y el servidor de Exchange.  <br/> |
   
Para ayudar a minimizar las desventajas, puede usar la [Biblioteca de autenticación de AD de Microsoft Azure](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries) (ADAL) para autenticar a los usuarios a los servicios de dominio de Active Directory (AD DS) en la nube o local y, a continuación, obtener tokens de acceso para proteger las llamadas a un Servidor de Exchange. Exchange Online requiere tokens emitidos por el servicio de Azure Active Directory, que es compatible con la ADAL; Sin embargo, puede utilizar cualquier biblioteca de otro fabricante. 
  
Para obtener más información acerca del uso de la autenticación de OAuth en la aplicación de EWS, vea los siguientes recursos:
  
- [Versión de evaluación de office 365](https://docs.microsoft.com/en-us/office/developer-program/office-365-developer-program), para configurar un servidor de Exchange para usar para probar la aplicación cliente.
    
- [Biblioteca de autenticación de Azure AD para .NET](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-authentication-libraries)
    
- [Configurar Azure Active Directory](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx), para habilitar la aplicación para usar los tokens de OAuth para la autenticación.
    
- Revise el código de ejemplo en [una aplicación de EWS mediante el uso de OAuth de autenticar](how-to-authenticate-an-ews-application-by-using-oauth.md) por ejemplo de código que puede estudiar. 
    
## <a name="ntlm-authentication"></a>Autenticación NTLM

La autenticación NTLM sólo está disponible para los servidores locales de Exchange. Para las aplicaciones que se ejecutan dentro del firewall corporativo, la integración entre la autenticación NTLM y .NET Framework proporciona que significa un integrada para autenticar su aplicación. 
  
**Tabla 2. Ventajas y desventajas del uso de la autenticación NTLM**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Works "fuera de la casilla" con el servidor de Exchange. Puede configurar el acceso a los servicios de Exchange mediante el uso de un [cmdlet del Shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Utiliza el objeto de .NET Framework [CredentialCache](http://msdn2.microsoft.com/EN-US/library/615e0wsd) para obtener automáticamente las credenciales del usuario.<br/><br/>[Ejemplos de código están disponibles](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que usan el inicio de sesión en las credenciales del usuario para la autenticación a un servidor de Exchange local.  <br/> | Los usuarios se deben iniciar sesión en un dominio para usar la autenticación NTLM.<br/><br/>Puede ser difícil tener acceso a las cuentas de correo electrónico que no estén asociadas con la cuenta de dominio del usuario.<br/><br/>Aplicaciones de servicio deben tener una cuenta de dominio para aprovechar las ventajas de la autenticación NTLM.  <br/> |
   
## <a name="basic-authentication"></a>Autenticación básica

La autenticación básica proporciona un, bueno, nivel básico de seguridad para la aplicación cliente. Se recomienda que todas las nuevas aplicaciones usan NTLM o el protocolo OAuth para la autenticación; Sin embargo, la autenticación básica puede ser la opción correcta para la aplicación en algunas circunstancias.
  
**Tabla 3. Ventajas y desventajas del uso de la autenticación básica**

|**Ventajas**|**Desventajas**|
|:-----|:-----|
| Works "fuera de la casilla" con el servidor de Exchange. Puede configurar el acceso a los servicios de Exchange mediante el uso de un [cmdlet del Shell de administración de Exchange](how-to-control-access-to-ews-in-exchange.md).<br/><br/>Las aplicaciones de Windows pueden usar credenciales predeterminadas de usuario ha iniciado la sesión.<br/><br/>Muchos [ejemplos de código están disponibles](http://code.msdn.microsoft.com/office/Exchange-2013-101-Code-3c38582c) que se muestra cómo llamar a EWS mediante la autenticación básica.  <br/> | Requiere la aplicación para recopilar y almacenar las credenciales del usuario.<br/><br/>Se debe desactivar la autenticación NTLM para todos los usuarios usar la autenticación básica.<br/><br/>Si se produce una infracción de seguridad en la aplicación, puede exponer dirección de correo electrónico del usuario y la contraseña que el atacante.  <br/> |
   
Debe decidir si la autenticación básica cumpla los requisitos de seguridad de la organización y los clientes. La autenticación básica puede ser la opción más adecuada si desea evitar tareas de configuración amplia, por ejemplo para prueba simple o aplicaciones de demostración.
  
## <a name="see-also"></a>Vea también

- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Adición de inicio de sesión para la aplicación Web utilizando Microsoft Azure AD](http://msdn.microsoft.com/library/055e1155-2d4d-4c85-b44e-d406872ba595%28Office.15%29.aspx)    
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md)    
- [Controlar el acceso de la aplicación de cliente para EWS en Exchange](controlling-client-application-access-to-ews-in-exchange.md)    
- [Símbolo (token) compatible y los tipos de notificación](http://msdn.microsoft.com/library/9d35e4bc-7b72-49d1-b723-5464eee6be2c%28Office.15%29.aspx)
    

