---
title: Modelos de objeto generados por Servicios Web Exchange (EWS) para Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 67d7d831-9c53-46da-80e4-18f562e71284
description: Si usa la referencia del modelo de objeto generado por EWS para desarrollar aplicaciones para Exchange, descubra otras opciones para el desarrollo EWS.
ms.openlocfilehash: 6c97ca7973da84d96d102287b9c260409a0f57ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541437"
---
# <a name="ews-generated-object-models-for-exchange"></a>Modelos de objeto generados por EWS para Exchange

**Se aplica a**: Exchange Online | Exchange Server 2013 | Office 365

El modelo de objetos de servicios Web Exchange (EWS) generado por wsdl.exe inicialmente proporciona un modelo de objetos adecuada para trabajar con Exchange 2007. Sin embargo, cuando la API administrada de EWS estuvo disponible, presentaba una serie de ventajas para desarrolladores que trabajan con código administrado. 

La API administrada de EWS:

- Proporciona un modelo de objeto más intuitivo.

- Contiene la lógica empresarial del lado del cliente y la validación de datos.

- Es totalmente compatible y se actualiza periódicamente.

- Contiene un cliente de detección automática.

- Implementa las características de cliente como registro, administración de cookies e informes de diagnóstico de nuevo en Exchange.

La documentación de referencia administrada según wsdl.exe de EWS se ha retirado porque la API administrada de EWS sustituye a la mayoría de las funcionalidades proporcionadas por los modelos de objeto generados. Al mismo tiempo, sabemos que la API administrada de EWS no es para todos los usuarios. En la mayoría de los casos, es la mejor forma de crear clientes EWS para. NET, pero hay algunas excepciones; por ejemplo:

- Cuando la funcionalidad que desea usar [no se ha implementado en la API administrada de EWS](../exchange-web-services/web-service-api-feature-availability-in-exchange-and-the-ews-managed-api.md#bk_apifeatures).

- Si usa una plataforma de desarrollo distinta de. NET.

Si no puede usar la API administrada de EWS para desarrollar la aplicación, puede:

- Usar una API de cliente EWS de terceros.

- Crear su propio modelo de objetos de cliente EWS.

- Usar el generador de un modelo de objetos. Puede que espere encontrar generadores de modelos de objeto para admitir la mayoría de los idiomas y de las plataforma principales.

Si tiene previsto usar el generador de un modelo de objetos, puede usar la referencia XML para ayudarle a comprender el modelo de objetos generado. El modelo de objetos se genera desde las estructuras XML que se describen en el esquema. Normalmente, las clases creadas por los generadores del modelo de objeto se asignan a los tipos complejos en el esquema. Las propiedades normalmente se asignan a los elementos XML.

Ver el [ExchangeWebServices Namespace](https://docs.microsoft.com/dotnet/api/exchangewebservices?view=exchange-ews-proxy).

## <a name="see-also"></a>Vea también

- [Referencia de servicios web para Exchange](web-services-reference-for-exchange.md)
- [Explorar la API administrada de EWS, EWS y servicios web en Exchange](../exchange-web-services/explore-the-ews-managed-api-ews-and-web-services-in-exchange.md)
- [Novedades de EWS y otros servicios web de Exchange](../exchange-web-services/whats-new-in-ews-and-other-web-services-in-exchange.md)
