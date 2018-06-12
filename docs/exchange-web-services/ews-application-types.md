---
title: Tipos de aplicación de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ca4e8b90-d0d8-4d55-aa92-19e21659d4f5
description: Obtenga información acerca de los tipos más comunes de aplicaciones que se pueden crear mediante el uso de EWS en Exchange.
ms.openlocfilehash: 1ce739f453ba1bc6f1b5d38edae3776daa562ffb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763001"
---
# <a name="ews-application-types"></a>Tipos de aplicación de EWS

Obtenga información acerca de los tipos más comunes de aplicaciones que se pueden crear mediante el uso de EWS en Exchange.
  
La [arquitectura EWS y Exchange](ews-applications-and-the-exchange-architecture.md) proporciona un modelo de desarrollo uniforme que puede usar para crear los tipos más comunes de aplicaciones de una manera coherente, incluido lo siguiente: 
  
- [Las aplicaciones cliente](#bk_clientapps) , las aplicaciones independientes que usan EWS para obtener acceso a datos de Exchange. Outlook y Outlook Web App son ejemplos de aplicaciones cliente. 
    
- [Aplicaciones de portal](#bk_portalapps) : aplicaciones que amplían una página web existente mediante la inclusión de información recuperan de Exchange, como la información de libre/ocupado o contacto. Un elemento web de SharePoint que recupera datos de Exchange es un ejemplo de una aplicación de portal. 
    
- [Aplicaciones de servicio](#bk_serviceapps) : utilizados para integrar o sincronizar los datos de Exchange en un sistema existente de trabajos en segundo plano. Por ejemplo, una aplicación que sincroniza la información de contacto de Exchange en una aplicación de CRM. 
    
Cada uno de estos modelos de aplicaciones puede usar una base de código comunes para recuperar información de Exchange - por lo que no es necesario cambiar el código EWS usado para recuperar información de elemento entre un cliente, un portal o una aplicación de servicio. Lo que puede cambiar de una aplicación a la siguiente es el mecanismo de autenticación y acceso de buzón de correo. Por ejemplo, las aplicaciones cliente con frecuencia usan el acceso directo de los usuarios y básica o la autenticación NTLM, mientras que una aplicación de servicio es probable que emplea la suplantación para la autenticación de OAuth y el acceso al buzón.
  
## <a name="client-applications"></a>Aplicaciones cliente
<a name="bk_clientapps"> </a>

Una aplicación de cliente de EWS es cualquier aplicación independiente que usa EWS para recuperar información desde el almacén de Exchange. Las aplicaciones cliente EWS usan acceso de cliente directo o acceso de delegado a recuperar datos desde el almacén de buzón de correo. Los siguientes son algunos ejemplos de aplicaciones cliente que utilizan EWS:
  
- Outlook, en características como el estado de fuera de la oficina de sugerencias de correo electrónico, la disponibilidad y el usuario
    
- OWA para dispositivos
    
- Outlook para Mac 2011
    
- Lync, la información de disponibilidad
    
Las aplicaciones de cliente suelen utilizar acceso directo y básica o la autenticación NTLM, para que los usuarios están limitados a obtener acceso a información en su propio buzón con sus propias credenciales de inicio de sesión. Las aplicaciones cliente deberían admitir también delegación de acceso para los usuarios que se ha concedido permiso de acceso a buzón de otro usuario.
  
## <a name="portal-applications"></a>Aplicaciones de portal
<a name="bk_portalapps"> </a>

Una aplicación de portal extiende una página web existente o un portal para incluir información de buzón de correo de Exchange como un componente personalizado de la página. Elementos web de SharePoint son las aplicaciones del portal más comunes y proporcionan a los usuarios una experiencia personalizada proporcionando vistas en datos de buzón de correo de Exchange, como los mensajes no leídos, los mensajes más recientes y eventos del calendario, junto con sus visualizados con frecuencia Página del portal de SharePoint. Las aplicaciones del portal de EWS pueden usar acceso de cliente directo, acceso delegado o suplantación para recuperar datos del almacén del buzón. Debido a que Exchange 2013 y SharePoint 2013 admiten el protocolo de autorización de OAuth para la autenticación de servidor a servidor, OAuth proporciona el método de autenticación más segura y sin problemas.
  
## <a name="service-applications"></a>Aplicaciones de servicio
<a name="bk_serviceapps"> </a>

Una aplicación de servicio suele ser un trabajo en segundo plano integrado en una aplicación existente que se extiende a Exchange para correlacionar datos entre el sistema y el almacén de Exchange. Aplicaciones de servicio normalmente no tiene una interfaz de usuario y usar suplantación o OAuth para la autenticación y el acceso. Creación de una cuenta de servicio para suplantar a los usuarios es común en las aplicaciones de servicio EWS, porque puede conceder a una cuenta única de permiso para suplantar a un conjunto de usuarios y realizar operaciones de buzón de correo para esas cuentas. Por ejemplo, una aplicación de servicio EWS puede sincronizar datos entre listas de marketing en una solución CRM y grupos de distribución de Exchange mediante el uso de una cuenta de servicio y la suplantación.
  
## <a name="see-also"></a>Ver también


- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [Aplicaciones de EWS y la arquitectura de Exchange](ews-applications-and-the-exchange-architecture.md)
    
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    

