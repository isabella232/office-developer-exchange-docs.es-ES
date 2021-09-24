---
title: Referencia de servicio web de detección automática SOAP para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Busque información de referencia para el servicio de detección automática SOAP en Exchange.
ms.openlocfilehash: 488862f5797abfd71d33c916fa96970ab300a2c0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521357"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Referencia de servicio web de detección automática SOAP para Exchange

Busque información de referencia para el servicio de detección automática SOAP en Exchange.
  
El servicio de detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un Exchange servidor. Puede usar el servicio de detección automática SOAP para enviar mensajes entre la aplicación cliente y el servidor Exchange para buscar la configuración que usará la aplicación para conectarse a Exchange. A diferencia del servicio de detección automática POX, el servicio de detección automática SOAP permite solicitudes de detección automática por lotes para la configuración de muchos usuarios y un control más detallado sobre qué opciones se devuelven en la respuesta. 
  
> [!NOTE]
> Para los clientes que tienen como destino las versiones de Exchange a partir de Exchange Server 2010, se recomienda usar el servicio de detección automática SOAP (en lugar del servicio de detección automática POX). Los clientes que Exchange 2007 deben usar el servicio de detección automática de POX. Se recomienda que los clientes que usan el .NET Framework la API administrada ews porque contiene un cliente de detección automática SOAP sólido y probado. Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx)cliente de la API administrada ews . 
  
En esta sección se proporciona información sobre los elementos XML que se envían entre el cliente y el servidor durante las redirecciones de solicitud de detección automática SOAP y la configuración del usuario que se devuelve en una respuesta. La referencia de elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las jerarquías de elementos potenciales que contienen el elemento. 
  
En los artículos de esta sección se describen las instancias XML que se envían entre el cliente y el servidor. El esquema que describe estos elementos puede encontrarse en el directorio virtual del servidor que hospeda el servicio de detección automática SOAP.
  
Los temas de operación WSDL de esta sección proporcionan una introducción a lo que hace la operación y ejemplos de solicitud de operación y respuesta. Puede usar la información de versión proporcionada para determinar si las características que desea usar están disponibles en la versión del producto que está ejecutando. Los ejemplos de los temas de operación también le ayudan a comprender la estructura del XML que se incluye en los mensajes SOAP que se envían al servidor y desde este.
  
En esta sección también se proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática SOAP. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
    
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
    
- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
    
- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Ver también


- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Usar autodetección para buscar puntos de conexión](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Obtener la configuración de dominio de un servidor de Exchange](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

