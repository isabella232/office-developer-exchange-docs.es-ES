---
title: Referencia de la API administrada de Servicios Web de Exchange (EWS)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
api_type:
- schema
ms.assetid: c6ca36f4-a67c-4e3c-aae7-9ead7b704e15
description: Obtenga información sobre los espacios de nombres que se incluyen en la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: aa5dd71bf1e9962611a8ea8471aca0c60aa232e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466755"
---
# <a name="ews-managed-api-reference"></a>Referencia de la API administrada de EWS

**Se aplica a**: API administrada de EWS | Exchange Online | Exchange Server 2007 | Exchange Server 2010 | Exchange Server 2013 | Office 365

La API administrada de Servicios Web de Exchange (EWS) incluye dos API: Microsoft.Exchange.WebServices.dll y Microsoft.Exchange.WebServices.Auth.dll.

## <a name="ews-managed-api-namespaces"></a>Los espacios de nombres de la API administrada de EWS

|Espacio de nombres |Descripción |
|:---------|:-----------|
|[Microsoft.Exchange.WebServices.Auth.Validation](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.auth.validation?view=exchange-ews-api) |Contiene los tipos y los métodos que se usan para validar los token de identidad de usuario enviados desde un servidor de Exchange. El espacio de nombre Microsoft.Exchange.WebServices.Auth.Validation es aplicable a los clientes que tienen Exchange Online y versiones de Exchange a partir de Exchange Server 2013. Este espacio de nombre se incluye en la API de Microsoft.Exchange.WebServices.Auth.dll.|
|[Microsoft.Exchange.WebServices.Autodiscover](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover?view=exchange-ews-api)|Contiene tipos que se usan para comunicarse con el servicio de detección automática hospedado por un servidor de Exchange. Este espacio de nombres también se usa para buscar objetos de punto de conexión de servicio en servicios de dominio de Active Directory (AD DS). Los servicios de detección automática proporcionan información de configuración a los clientes EWS. Esto permite a los clientes dirigirse a la dirección URL del servicio correspondiente.<br/><br/>La funcionalidad del espacio de nombres puede usarse para dirigir el servicio de detección automática de POX introducido en Microsoft Exchange Server 2007, la búsqueda de objeto de punto de conexión de servicio si el cliente está unido al dominio o el punto de conexión de detección automática de SOAP se introdujo en Exchange Server 2010. El tipo de este espacio de nombres principal es la [clase AutodiscoverService](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.autodiscover.autodiscoverservice?view=exchange-ews-api). Este espacio de nombre se incluye en la API de Microsoft.Exchange.WebServices.dll.|
|[Microsoft.Exchange.WebServices.Data](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data?view=exchange-ews-api)| Contiene tipos que se usan para comunicarse con un servidor de Exchange mediante EWS. Este espacio de nombres proporciona la funcionalidad de la API administrada de EWS principal. El tipo de este espacio de nombres principal es la [clase ExchangeService](https://docs.microsoft.com/dotnet/api/microsoft.exchange.webservices.data.exchangeservice?view=exchange-ews-api).|

## <a name="see-also"></a>Vea también

- [Referencia de servicios web para Exchange](web-services-reference-for-exchange.md)
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Novedades de EWS y otros servicios web de Exchange](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
- [Empezar a usar los servicios web de Exchange](../exchange-web-services/start-using-web-services-in-exchange.md)
- [Desarrollo de clientes de servicios web de Exchange](../exchange-web-services/develop-web-service-clients-for-exchange.md)

