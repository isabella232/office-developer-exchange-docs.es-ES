---
title: Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Buscar recursos que le ayuden a solucionar problemas de la API administrada de EWS o de la aplicación de EWS.
localization_priority: Priority
ms.openlocfilehash: 7c7cbe8c93edec5ad99df079c6eb96286c1ba063
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463744"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange

Buscar recursos que le ayuden a solucionar problemas de la API administrada de EWS o de la aplicación de EWS.
  
Las cosas no siempre se redirigen según lo previsto. A veces, las solicitudes de EWS producen errores o proporcionan resultados inesperados. Esto puede resultar frustrante, especialmente si la razón no es evidente. Espero que esto no suceda nunca, pero si lo hace, este artículo proporciona información acerca de las herramientas y los recursos que puede usar para solucionar el problema.
  
> [!NOTE]
> En este artículo se proporcionan consejos y orígenes de solución de problemas generales para la información de solución de problemas. Desafortunadamente, no es posible dar pasos detallados para la solución de problemas. Para obtener ayuda para solucionar el error específico, vea [los siguientes pasos](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Examinar las solicitudes y respuestas SOAP

Cuando los elementos no funcionan correctamente, es muy útil para ver lo que ocurre. La primera línea de consulta al investigar un problema con EWS o con la API administrada de EWS es examinar las solicitudes que la aplicación envía a través de la red y las respuestas que el servidor envía de vuelta.
  
La API administrada de EWS facilita el examen de solicitudes y respuestas SOAP con su [funcionalidad de seguimiento integrada](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Si usa EWS, puede o no tener acceso a una funcionalidad de seguimiento similar, en función de la plataforma o clases que use para enviar las solicitudes. Sin embargo, siempre puede usar una herramienta de seguimiento de red como el [monitor de red](https://www.microsoft.com/download/details.aspx?id=4865) o [Fiddler](http://www.telerik.com/fiddler) para examinar el tráfico de red y ver las cargas de solicitud y respuesta. 
  
Además, puede [instrumentar las solicitudes de cliente](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) para mejorar la información disponible en las solicitudes y respuestas. 
  
Una vez que tenga las solicitudes y respuestas, pregúntese lo siguiente: ¿parece que son correctas? ¿Se esperan los valores que envía la aplicación? ¿Las respuestas tienen sentido?
  
## <a name="examine-error-codes"></a>Examinar los códigos de error

A veces, el código de error puede avanzar mucho para identificar el problema, incluso si a primera vista no parece tener sentido. ¿El error indica que el cliente se está [limitando](ews-throttling-in-exchange.md)? ¿Quizá una llamada a la detección automática para [actualizar la información de configuración](how-to-refresh-configuration-information-by-using-autodiscover.md) está en orden? 
  
Para obtener más información acerca del tratamiento de errores específicos, vea los siguientes artículos:
  
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Control de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Controlar errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Administración de errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Comprobar versiones

Hay varios componentes diferentes involucrados en las operaciones de EWS y las versiones de dichos componentes pueden influir en los resultados.
  
**Tabla 1. Componentes con versiones que pueden afectar a los procesos de EWS**

|**Componente**|**API administrada EWS**|**EWS**|**Notas**|
|:-----|:-----|:-----|:-----|
|Versión del servidor solicitada  <br/> |Propiedad [ExchangeServiceBase. RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)  <br/> |Elemento [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)  <br/> |Este valor controla la versión del esquema EWS que se usa para procesar la solicitud de EWS. Asegúrese de que la versión del esquema que se especifica aquí tiene sentido para la solicitud que va a enviar. Algunas propiedades y operaciones no están disponibles en versiones anteriores del esquema.  <br/> |
|La versión del servidor  <br/> |Propiedad [ExchangeServiceBase. inicializado](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)  <br/> |Elemento [ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)  <br/> |Este valor lo devuelve el servidor en las respuestas de EWS e indica la versión del servidor que procesó la respuesta. Asegúrese de que este valor es el esperado. Si es posible, asegúrese de que el servidor de Exchange ejecuta la actualización más reciente de la versión principal de Exchange.  <br/> |
|La versión de la API administrada de EWS  <br/> |La propiedad Product version del archivo Microsoft. Exchange. webservices. dll.  <br/> |No aplicable  <br/> |Si está usando la API administrada de EWS, asegúrese de que está usando [la versión más reciente](https://aka.ms/ews-managed-api-readme).  <br/> |
   
## <a name="verify-access"></a>Comprobación del acceso

EWS está habilitado de forma predeterminada, pero se [pueden cambiar los valores predeterminados](how-to-control-access-to-ews-in-exchange.md). Use el cmdlet [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) para asegurarse de que EWS esté habilitado en el servidor y el cmdlet [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) para asegurarse de que EWS esté habilitado para el buzón de correo del usuario. Compruebe también ambas respuestas de cmdlet para una lista de permitidos o bloqueados de EWS y asegúrese de que la aplicación no esté bloqueada para usar EWS. 
  
También debe comprobar que no se ha modificado la [configuración de autenticación predeterminada](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) en el directorio virtual de EWS. 
  
## <a name="try-another-ews-client"></a>Probar otro cliente de EWS

A veces, es útil probar la misma solicitud desde otro cliente y comparar los resultados. Si otro cliente obtiene resultados diferentes, ¿qué es diferente? Averiguar qué es diferente entre una solicitud correcta y una solicitud con errores puede ayudar a explicar por qué se produce un error en una solicitud determinada.
  
Aunque puede escribir otro cliente para probarlo, no tiene que hacerlo. [EWSEditor](http://ewseditor.codeplex.com/) es un cliente de ejemplo que usa la API administrada de EWS y EWS. Puede descargar el cliente (incluido el código fuente) y usarlo para probar las mismas solicitudes que producen errores en la aplicación. 
  
## <a name="examine-iis-logs"></a>Examinar los registros de IIS

Si tiene acceso al servidor de Exchange, la funcionalidad de registro que proporcionan los servicios de Internet Information Server (IIS) en los servidores de acceso de cliente puede proporcionar más información sobre los errores. Sin embargo, tenga en cuenta que los registros de IIS solo serán útiles si recibe un error de HTTP.
  
IIS proporciona dos métodos de registro diferentes: el [registro de IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) y el seguimiento de [solicitudes con error](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Para trabajar con registros de IIS, puede usar [log parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), que incluye una serie de consultas de EWS integradas.
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_NextSteps"> </a>

Ahora que ya conoce las herramientas y los recursos que puede usar para solucionar problemas, es posible que necesite ayuda para comprender la información proporcionada por dichas herramientas. A continuación se muestran algunas opciones para obtener ayuda:
  
- [Foro de desarrollo de Exchange Server en MSDN](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) : formule una pregunta de la comunidad de desarrollo de Exchange Server de MSDN. 
    
- [Stackoverflow](http://stackoverflow.com/tags/ews) : formule una pregunta de la comunidad stackoverflow. Asegúrese de etiquetar la publicación con "EWS". 
    
- [Soporte técnico de Microsoft](https://support.microsoft.com/ph/730/en-us) : póngase en contacto con un profesional de soporte técnico de Microsoft para obtener ayuda. 
    
## <a name="see-also"></a>Vea también


Consulte los siguientes artículos:
  
- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Instrumentar solicitudes de cliente para EWS y REST en Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)
    
- [Actualizar la información de configuración mediante la detección automática](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Control de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Controlar errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Administración de errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Configuración del registro en IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Solución de problemas de solicitudes con error de seguimiento en IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Introducción a: log parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Configuración predeterminada para directorios virtuales de Exchange](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
Descargue lo siguiente:
  
- [Monitor de red de Microsoft 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [API administrada de servicios Web Exchange](https://go.microsoft.com/fwlink/?LinkID=255472)
    

