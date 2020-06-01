---
title: Referencia del servicio Web de detección automática de SOAP para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 61c21ea9-7fea-4f56-8ada-bf80e1e6b074
description: Busque información de referencia para el servicio de detección automática de SOAP en Exchange.
ms.openlocfilehash: bfca8e8e260a6262d12542bd6834894a2375453f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468428"
---
# <a name="soap-autodiscover-web-service-reference-for-exchange"></a>Referencia del servicio Web de detección automática de SOAP para Exchange

Busque información de referencia para el servicio de detección automática de SOAP en Exchange.
  
El servicio Detección automática proporciona la información de configuración que la aplicación usa para crear una conexión a un servidor de Exchange. Puede usar el servicio Detección automática de SOAP para enviar mensajes entre la aplicación cliente y el servidor Exchange para buscar la configuración que la aplicación usará para conectarse a Exchange. A diferencia del servicio Detección automática de POX, el servicio Detección automática de SOAP permite solicitudes de detección automática por lotes para la configuración de muchos usuarios y un control más granular sobre la configuración que se devuelve en la respuesta. 
  
> [!NOTE]
> Para los clientes que tienen como destino versiones de Exchange que comienzan con Exchange Server 2010, se recomienda usar el servicio de detección automática de SOAP (en lugar del servicio Detección automática de POX). Los clientes que tienen el destino de Exchange 2007 deben usar el servicio Detección automática de POX. Se recomienda que los clientes que usen .NET Framework usen la API administrada de EWS porque contiene un cliente de detección automática de SOAP sólido y bien probado. Para obtener más información sobre la API administrada de EWS, vea Introducción [a las aplicaciones cliente de la API administrada de EWS](https://msdn.microsoft.com/library/c2267733-6f4f-49e5-9614-1e4a24c3af1a%28Office.15%29.aspx). 
  
En esta sección se proporciona información acerca de los elementos XML que se envían entre el cliente y el servidor durante la redirección de la solicitud de detección automática de SOAP y la configuración de usuario que se devuelve en una respuesta. La referencia del elemento XML contiene resúmenes de lo que representan los elementos y una descripción de las jerarquías de elementos potenciales que contienen el elemento. 
  
En los artículos de esta sección se describen las instancias de XML que se envían entre el cliente y el servidor. El esquema que describe estos elementos se puede encontrar en el directorio virtual del servidor que hospeda el servicio Detección automática de SOAP.
  
En los temas de funcionamiento de WSDL de esta sección se proporciona información general sobre lo que hace la operación y los ejemplos de solicitud y respuesta de la operación. Puede usar la información de versión proporcionada para determinar si las características que desea usar están disponibles en la versión del producto que está ejecutando. Los ejemplos de los temas de operación también ayudan a comprender la estructura del XML que se incluye en los mensajes SOAP que se envían a y desde el servidor.
  
En esta sección también se proporcionan ejemplos y descripciones de los mensajes que se usan para recuperar información de configuración de detección automática mediante el servicio Detección automática de SOAP. 
  
## <a name="in-this-section"></a>En esta sección
<a name="bk_InThisSection"> </a>

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)
    
- [Operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md)
    
- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
    
- [Operación GetOrganizationRelationshipSettings (SOAP)](getorganizationrelationshipsettings-operation-soap.md)
    
- [Elementos XML de detección automática de SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)
    
## <a name="see-also"></a>Vea también


- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Detección automática en Exchange](../exchange-web-services/autodiscover-for-exchange.md)
- [Usar autodetección para buscar puntos de conexión](https://msdn.microsoft.com/library/03896542-549b-4c45-973c-98f9025ea26c%28Office.15%29.aspx)
- [Obtener la configuración de usuario de Exchange mediante el uso de detección automática](https://msdn.microsoft.com/library/6d90c305-4802-4e18-8d52-f60349feaa8d%28Office.15%29.aspx)
- [Obtener la configuración de dominio de un servidor de Exchange](https://msdn.microsoft.com/library/2f9acb81-5135-4f72-94e8-65c235d725e6%28Office.15%29.aspx)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
    

