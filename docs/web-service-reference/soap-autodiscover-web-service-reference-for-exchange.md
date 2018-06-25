---
title: Referencia de servicio web de detección automática de SOAP para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Busque información de referencia para el servicio Detección automática de SOAP en Exchange.
ms.openlocfilehash: 1cb24a8667c71028f3dead78d9fa533dc9547a64
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837514"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Referencia de servicio web de detección automática de SOAP para Exchange

Busque información de referencia para el servicio Detección automática de SOAP en Exchange.
  
El servicio Detección automática proporciona la información de configuración que la aplicación se usa para crear una conexión a un servidor de Exchange. Puede usar el servicio Detección automática de SOAP para enviar mensajes entre la aplicación cliente y el servidor de Exchange para buscar la configuración de que la aplicación usará para conectarse a Exchange. A diferencia del servicio de detección automática de POX, permite que el servicio Detección automática de SOAP para solicitudes de detección automática por lotes para la configuración de muchos de los usuarios y un mayor control sobre qué configuración se devuelve en la respuesta. 
  
> [!NOTE]
> Para los clientes que estén destinados a las versiones de Exchange Server 2010 a partir de Exchange, se recomienda que use el servicio de detección automática de SOAP (en lugar del servicio de detección automática de POX). Los clientes que estén destinados a Exchange 2007 deben usar el servicio Detección automática POX. Se recomienda que los clientes que utilicen .NET Framework usan la API administrada de EWS porque contiene a un cliente de detección automática de SOAP robusto y probado. Para obtener más información acerca de la API administrada de EWS, vea [Introducción a las aplicaciones cliente de API administrada de EWS](http://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante el redireccionamiento de la solicitud de detección automática de SOAP y la configuración del usuario que se devuelve en una respuesta. La referencia de elemento XML contiene resúmenes de los elementos que representan y una descripción de los posibles jerarquías de elementos que contienen el elemento. 
  
Los artículos de esta sección describen las instancias XML que se envían entre el cliente y el servidor. El esquema que describe estos elementos puede encontrarse en el directorio virtual del servidor que hospeda el servicio de detección automática de SOAP.
  
La operación WSDL temas de esta sección proporcionan que una visión general de qué es la operación y ejemplos de solicitud y respuesta de la operación. Puede usar la información de versión proporcionada para determinar si las características que desea utilizar están disponibles en la versión del producto que se está ejecutando. En los ejemplos de los temas de la operación también le ayudarán a comprender la estructura de XML que se incluye en los mensajes SOAP que se envían a y desde el servidor.
  
En esta sección también proporciona ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio de detección automática de SOAP. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
    
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
    
- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
    
- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Vea también


- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática de Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Usar detección automática para buscar puntos de conexión](http://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](http://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Obtener la configuración de dominio de un servidor de Exchange](http://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Empezar a utilizar servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

