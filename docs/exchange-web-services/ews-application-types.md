---
title: Tipos de aplicación de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: Obtenga información sobre los tipos de aplicaciones más comunes que puede crear con EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 02bbe039adaec1054ab33f642f3bf14a7ba22b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455432"
---
# <a name="ews-application-types"></a>Tipos de aplicación de EWS

Obtenga información sobre los tipos de aplicaciones más comunes que puede crear con EWS en Exchange.
  
La [arquitectura de EWS y Exchange](ews-applications-and-the-exchange-architecture.md) proporciona un modelo de desarrollo uniforme que puede usar para crear los tipos de aplicaciones más comunes de manera coherente, entre los que se incluyen los siguientes: 
  
- [Aplicaciones cliente](#bk_clientapps) : aplicaciones independientes que usan EWS para tener acceso a los datos de Exchange. Outlook y Outlook Web App son ejemplos de aplicaciones cliente. 
    
- [Aplicaciones de portal](#bk_portalapps) : aplicaciones que extienden una página web existente mediante la inclusión de información recuperada de Exchange, como la disponibilidad o la información de contacto. Un elemento Web de SharePoint que recupera datos de Exchange es un ejemplo de una aplicación de portal. 
    
- [Aplicaciones de servicio](#bk_serviceapps) : trabajos en segundo plano que se usan para integrar o sincronizar datos de Exchange en un sistema existente. Por ejemplo, una aplicación que sincroniza la información de contacto de Exchange en una aplicación de CRM. 
    
Cada uno de estos modelos de aplicación puede usar una base de código común para recuperar información de Exchange, por lo que no es necesario cambiar el código EWS usado para recuperar información de elementos entre un cliente, un portal o una aplicación de servicio. Lo que puede cambiar de una aplicación a la siguiente es el acceso al buzón y el mecanismo de autenticación. Por ejemplo, las aplicaciones cliente suelen usar el acceso de usuario directo y la autenticación básica o NTLM, mientras que una aplicación de servicio probablemente use la suplantación para el acceso al buzón y la autenticación de OAuth.
  
## <a name="client-applications"></a>Aplicaciones cliente
<a name="bk_clientapps"> </a>

Una aplicación cliente de EWS es cualquier aplicación independiente que usa EWS para recuperar información del almacén de Exchange. Las aplicaciones cliente de EWS usan acceso de cliente directo o acceso delegado para recuperar datos del almacén de buzones. A continuación se muestran algunos ejemplos de aplicaciones cliente que usan EWS:
  
- Outlook, en características como sugerencias de correo, disponibilidad y estado OOF de usuario
    
- OWA para dispositivos
    
- Outlook para Mac 2011
    
- Lync, para obtener información de disponibilidad
    
Las aplicaciones cliente suelen usar el acceso directo y la autenticación básica o NTLM, de modo que los usuarios se limitan a obtener acceso a la información de su propio buzón con sus propias credenciales de inicio de sesión. Las aplicaciones cliente también deben admitir el acceso delegado a los usuarios a los que se les haya concedido permiso para acceder al buzón de otro usuario.
  
## <a name="portal-applications"></a>Aplicaciones de portal
<a name="bk_portalapps"> </a>

Una aplicación de portal amplía una página web o un portal existente para incluir la información del buzón de Exchange como un componente personalizado de la página. Los elementos Web de SharePoint son las aplicaciones de portal más comunes y proporcionan a los usuarios una experiencia personalizada al proporcionar vistas en datos de buzones de Exchange, como mensajes no leídos, mensajes más recientes y eventos de calendario, junto con la página de portal de SharePoint que se ha visto habitualmente. Las aplicaciones de portal EWS pueden usar el acceso de cliente directo, el acceso delegado o la suplantación para recuperar datos del almacén de buzones. Como Exchange 2013 y SharePoint 2013 admiten el protocolo de autorización OAuth para la autenticación de servidor a servidor, OAuth proporciona el método de autenticación más seguro y sin problemas.
  
## <a name="service-applications"></a>Aplicaciones de servicio
<a name="bk_serviceapps"> </a>

Una aplicación de servicio suele ser un trabajo en segundo plano integrado en una aplicación existente que se extiende a Exchange para correlacionar los datos entre el sistema y el almacén de Exchange. Normalmente, las aplicaciones de servicio no tienen una interfaz de usuario y usan la suplantación o OAuth para la autenticación y el acceso. La creación de una cuenta de servicio para suplantar a los usuarios es común en las aplicaciones de servicio de EWS porque puede conceder a un único permiso de cuenta para suplantar a un conjunto de usuarios y realizar operaciones de buzón para esas cuentas. Por ejemplo, una aplicación de servicio EWS puede sincronizar datos entre listas de marketing en una solución CRM y intercambiar grupos de distribución con una cuenta de servicio y una suplantación.
  
## <a name="see-also"></a>Vea también


- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Aplicaciones de EWS y la arquitectura de Exchange](ews-applications-and-the-exchange-architecture.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    

