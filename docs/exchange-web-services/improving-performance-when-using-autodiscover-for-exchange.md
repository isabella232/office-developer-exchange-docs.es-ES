---
title: Mejorar el rendimiento cuando se utiliza la detección automática de Exchange
manager: sethgros
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e65ff6b2-3810-43ad-9728-27308891b193
description: Obtenga información sobre maneras de mejorar el rendimiento del proceso de detección automática en la aplicación.
ms.openlocfilehash: 844b56084b4f0b5e49b4ee095688d58ce469baca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456335"
---
# <a name="improving-performance-when-using-autodiscover-for-exchange"></a>Mejorar el rendimiento cuando se utiliza la detección automática de Exchange

Este documento puede incluir contenido relacionado con funciones o productos preliminares que pueden cambiar mucho antes del lanzamiento comercial final. Este documento se proporciona "tal cual" solamente con fines informativos y Microsoft no realiza ninguna garantía, explícita ni implícita, en el documento. Obtenga información sobre maneras de mejorar el rendimiento del proceso de detección automática en la aplicación.
  
Hay una gran cantidad de razones para como detección automática. Configuración de la aplicación para conectarse a Exchange sin intervención del usuario es excelente! Si está leyendo este artículo, probablemente ya sabe todas las razones para usar y disfrutan de detección automática, por lo que no se muestran aquí. En su lugar, vamos a hablar sobre una desventaja potencial: rendimiento.
  
Detección automática no es esencialmente un proceso lento, pero no es por sí rápido ya sea. El [proceso de detección automática](autodiscover-for-exchange.md) implica una gran cantidad de actividad de red y, a continuación, presenta una gran cantidad de retraso potencial. El proceso de detección automática tiene tres fases; las tres tienen el potencial de afectar al rendimiento: 
  
- Definición del grupo de candidatos de extremo de detección automática: para las aplicaciones que se ejecutan en equipos unidos a un dominio, esto puede incluir en [las búsquedas de SCP](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md), lo que implica comunicarse con los servicios de dominio de Active Directory (AD DS).
    
- Intentar cada candidato: Esto requiere una solicitud o respuesta HTTP a cada extremo del candidato.
    
- Prueba de otras alternativas: cuando los candidatos en el grupo de candidatos de extremo de detección automática no producen resultados, puede realizar una solicitud GET no autenticada (solicitud/respuesta HTTP) y una búsqueda de DNS.
    
En la superficie de esto es posible que no parecen demasiado. Sin embargo, imagine un escenario donde el grupo de candidatos de extremo de detección automática es más de uno o dos direcciones URL y no encuentra un trabajo uno hasta la última dirección URL en el grupo de servidores. El retraso puede ser un poco más significativa. Por lo tanto, ¿qué puede hacer?
  
## <a name="consider-the-need-for-scp-lookup"></a>Tenga en cuenta la necesidad de búsqueda de SCP

Cuando los objetos SCP están presentes y correctamente configurado, puede acelerar el proceso de detección automática. En otras situaciones, sin embargo, pueden ralentizarlo. Si SCP no se usa en el entorno, omita la parte de búsqueda de SCP completa del proceso de detección automática para ahorrar tiempo.
  
La API administrada de EWS facilita esta tarea: establezca la propiedad [ExchangeService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.enablescplookup%28v=exchg.80%29.aspx) a **false** antes de llamar al método [ExchangeService.AutodiscoverUrl](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.autodiscoverurl%28v=exchg.80%29.aspx) . Si está usando la clase [AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx) , establezca la propiedad de [AutodiscoverService.EnableScpLookup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice.enablescplookup%28v=exchg.80%29.aspx) a **false** antes de llamar a cualquiera de sus métodos. 
  
## <a name="use-autodiscover-less-often"></a>Usar detección automática menos a menudo

Detección automática no está diseñada para ser utilizada con frecuencia uso por aplicaciones. La intención detrás de detección automática es para que una aplicación de uso para conocer la información de configuración y, a continuación, la memoria caché que la información de un período de tiempo. Si no son el almacenamiento en caché de la información de configuración, considere la posibilidad de agregar el almacenamiento en caché de la aplicación para reducir el número de veces que se utiliza la detección automática.
  
Incluso si ya están en la caché, evaluar cuánto tiempo es almacenar en caché la información de configuración. Es el estándar para [actualizar la información de detección automática cada 24 horas](how-to-refresh-configuration-information-by-using-autodiscover.md), pero es posible que pueda extender en ese momento. Debe probar con los entornos de destino y surgen con un "time-to-live" para la configuración que se adapte a sus necesidades.
  
## <a name="minimize-requested-data"></a>Minimizar los datos solicitados

If you're using the **AutodiscoverService** class in the EWS Managed API, or the [Operación GetUserSettings (SOAP)](https://msdn.microsoft.com/library/758d965c-ef63-4de4-9120-e293abf14ff8%28Office.15%29.aspx) operation via SOAP, you have direct control over what settings are returned in the response. Although you can request quite a few settings, chances are that your application only needs a handful of them. Every setting that you request requires more processing on the server, which means more time waiting for a response. Evaluate the settings you are requesting, and eliminate any that you don't need. 
  
Si usa el método **ExchangeService.AutodiscoverUrl** en la API administrada de EWS, no puede cambiar la configuración que se solicita. Sin embargo, este método ya es bastante eficaz; sólo se solicita la configuración de **ExternalEwsUrl** y **InternalEwsUrl** de la [enumeración UserSettingName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.usersettingname%28v=exchg.80%29.aspx).
  
Si usa el servicio de detección automática de POX, [no puede solicitar propiedades específicas](autodiscover-for-exchange.md#bk_Options).
  
## <a name="see-also"></a>Vea también


- [Detección automática en Exchange](autodiscover-for-exchange.md)
    
- [Buscar Autodisover extremos mediante el uso de búsqueda de SCP en Exchange](how-to-find-autodiscover-endpoints-by-using-scp-lookup-in-exchange.md)
    
- [Actualizar la información de configuración mediante la detección automática](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Clase ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)
    
- [Clase AutodiscoverService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.autodiscover.autodiscoverservice%28v=exchg.80%29.aspx)
    

