---
title: Establecer la dirección URL del servicio EWS usando la API administrada de EWS
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: cddf6525-1c04-484b-a911-56c2f0f1f7b6
description: Obtenga información sobre cómo configurar la dirección URL del servicio EWS en la aplicación de la API administrada de EWS.
ms.openlocfilehash: e1a414f7c6f13bd61a58403c9d2be546c0226a69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763167"
---
# <a name="set-the-ews-service-url-by-using-the-ews-managed-api"></a>Establecer la dirección URL del servicio EWS usando la API administrada de EWS

Obtenga información sobre cómo configurar la dirección URL del servicio EWS en la aplicación de la API administrada de EWS.
  
La dirección URL del servicio es la dirección que Exchange usa para comunicarse con los servicios Web Exchange (EWS). Una vez que la aplicación de API administrada de EWS tiene esta dirección y el debido acceso para [comunicarse con EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md), puede hacer llamadas a la [clase ExchangeService](http://msdn.microsoft.com/es-ES/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx). La URL del servicio para un servidor de Exchange local puede tener el aspecto siguiente. 
  
```HTML
https://computer.domain.contoso.com/EWS/Exchange.asmx
```

La dirección URL de EWS se puede establecer en la aplicación de dos formas. Le recomendamos que use el [servicio Detección automática](http://msdn.microsoft.com/library/39726b67-2eb2-451b-9307-cfd0b518b55c%28Office.15%29.aspx) para obtener la dirección URL porque, en un busque grande de servidores, la dirección URL puede cambiar si el buzón de correo se migra a otro servidor. Sin embargo, como la llamada a Detección automática puede tardar y ralentizar la aplicación (en el caso de que tenga que realizar varias llamadas en un breve período de tiempo), conviene almacenar en caché el valor de la URL obtenido de Detección automática y establecer manualmente la dirección URL del servicio EWS con dicho valor. De esta forma se logra mejorar el rendimiento de la aplicación. Debe asegurarse de usar Detección automática para actualizar periódicamente el valor almacenado en caché por si acaso cambia en el servidor. 
  
## <a name="set-the-ews-service-url-by-using-the-autodiscover-service"></a>Establecer la dirección URL del servicio EWS usando el servicio Detección automática
<a name="bk_SetURLusingAutoDiscover"> </a>

El método [AutodiscoverUrl](http://msdn.microsoft.com/es-ES/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) usa la dirección de correo electrónico para establecer el extremo [ExchangeService](http://msdn.microsoft.com/es-ES/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) y permite a la aplicación usar los métodos incluidos en las clases proxy **ExchangeService**. El ejemplo siguiente muestra cómo usar el método **AutodiscoverURL**. 
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.AutodiscoverUrl("User1@contoso.com");

```

## <a name="set-the-exchange-service-url-manually"></a>Establecer la dirección URL del servicio de Exchange manualmente
<a name="bk_SetURLmanually"> </a>

El ejemplo siguiente muestra cómo establecer la dirección URL del servicio EWS mediante un valor almacenado en caché. Antes de hacerlo, use el servicio Detección automática para obtener la dirección URL de EWS.
  
```cs
// Create the binding.
ExchangeService service = new ExchangeService();
// Set the credentials for the on-premises server.
service.Credentials = new WebCredentials("user1@contoso.com", "password");
// Set the URL.
service.Url = new Uri("https://computername.domain.contoso.com/EWS/Exchange.asmx");

```

## <a name="see-also"></a>Vea también

- [Empezar a trabajar con aplicaciones de cliente de la API administrada de EWS](get-started-with-ews-managed-api-client-applications.md)   
- [Configurar su entorno de desarrollo de aplicaciones de Exchange](setting-up-your-exchange-application-development-environment.md)   
- [Controlar el acceso a EWS en Exchange](how-to-control-access-to-ews-in-exchange.md) 
- [Comunicarse con EWS mediante la API administrada de EWS](how-to-communicate-with-ews-by-using-the-ews-managed-api.md)  
- [Usar autodetección para buscar puntos de conexión](how-to-use-autodiscover-to-find-connection-points.md)
    

