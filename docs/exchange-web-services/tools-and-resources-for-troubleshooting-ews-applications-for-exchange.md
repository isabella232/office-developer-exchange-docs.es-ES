---
title: Herramientas y recursos para la resolución de problemas de las aplicaciones EWS para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Encuentre recursos que le ayuden a solucionar los problemas de su aplicación EWS Managed API o EWS.
localization_priority: Priority
ms.openlocfilehash: 8a65b06cf911cd033d7fe5fe1b4566a7496de784
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542585"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Herramientas y recursos para la resolución de problemas de las aplicaciones EWS para Exchange

Encuentre recursos que le ayuden a solucionar los problemas de su aplicación EWS Managed API o EWS.
  
Las cosas no siempre salen como son planeadas. A veces, las solicitudes de EWS fallan, o proporcionan resultados inesperados. Esto puede ser frustrante, especialmente si la razón no es obvia. Esperemos que esto nunca le ocurra, pero si sucede, este artículo proporciona información sobre herramientas y recursos que puede utilizar para ayudar a solucionar su problema.
  
> [!NOTE]
> Este artículo proporciona consejos generales para la solución de problemas y fuentes de información para la solución de problemas. Lamentablemente, no es posible dar pasos detallados para la solución de problemas. Para obtener ayuda en la resolución de su error en específico, consulte [Pasos siguientes](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Examinar las solicitudes y respuestas SOAP

Cuando las cosas no funcionan correctamente, es muy útil poder ver lo que está pasando. La primera línea de investigación cuando se investiga un problema con EWS o la API administrada de EWS es examinar las solicitudes que su aplicación está enviando a través de la red y las respuestas que el servidor está enviando de vuelta.
  
La API administrada de EWS facilita el examen de las solicitudes y respuestas SOAP gracias a su [función de seguimiento integrada](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Si está usando EWS, puede o no tener acceso a una funcionalidad de rastreo similar, dependiendo de la plataforma o las clases que utilice para enviar sus solicitudes. Sin embargo, siempre se puede utilizar una herramienta de rastreo de red como [Network Monitor](https://www.microsoft.com/download/details.aspx?id=4865) o [Fiddler](http://www.telerik.com/fiddler) para examinar el tráfico de red y ver las cargas útiles de solicitud y respuesta. 
  
Además, puede [instrumentar las solicitudes de sus clientes](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) para mejorar la información disponible en las solicitudes y respuestas. 
  
Una vez que tenga las solicitudes y las respuestas, pregúntese lo siguiente: ¿Parecen correctas? ¿Los valores que envía su aplicación son los esperados? ¿Tienen sentido las respuestas?
  
## <a name="examine-error-codes"></a>Examinar códigos de error

A veces, el código de error puede ayudar mucho a localizar el problema, aunque a primera vista no parezca tener sentido. ¿Indica el error que su cliente está siendo [limitado](ews-throttling-in-exchange.md)? ¿Quizás sea necesario llamar a Autodiscover para [refrescar la información de configuración](how-to-refresh-configuration-information-by-using-autodiscover.md)? 
  
Para obtener más información sobre el manejo de errores específicos, consulte los siguientes artículos:
  
- [Manejo de los mensajes de error de Autodiscover](handling-autodiscover-error-messages.md)
    
- [Manejo de errores relacionados con las notificaciones en EWS en Exchange ](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Manejo de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Manejo de errores relacionados con el borrado en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Comprobar versiones

En las operaciones del sistema de alerta temprana intervienen varios componentes, y las versiones de esos componentes pueden influir en los resultados.
  
**Tabla 1. Componentes versionados que pueden afectar a los procesos del EWS**

|**Componente**|**API administrada EWS**|**EWS**|**Notas**|
|:-----|:-----|:-----|:-----|
|Versión del servidor solicitada  <br/> |Propiedad [ExchangeServiceBase.RequestedServerVersion](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx)  <br/> |Elemento [RequestServerVersion](https://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)  <br/> |Este valor controla qué versión del esquema EWS se utiliza para procesar la solicitud EWS. Asegúrese de que la versión del esquema especificada aquí tiene sentido para la solicitud que está enviando. Algunas propiedades y operaciones no están disponibles en versiones anteriores del esquema.  <br/> |
|La versión del servidor  <br/> |Propiedad [ExchangeServiceBase.ServerInfo](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx)  <br/> |Elemento [ServerVersionInfo](https://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)  <br/> |Este valor es devuelto por el servidor en las respuestas EWS, e indica la versión del servidor que ha procesado la respuesta. Asegúrese de que este valor sea el esperado. Si es posible, asegúrese de que el servidor Exchange está ejecutando la actualización más reciente para su versión principal de Exchange.  <br/> |
|La versión de la API administrada de EWS  <br/> |La propiedad Versión del producto del archivo Microsoft.Exchange.WebServices.dll.  <br/> |No aplicable  <br/> |Si está utilizando la API administrada de EWS, asegúrese de que está usando [la versión más reciente](https://aka.ms/ews-managed-api-readme).  <br/> |
   
## <a name="verify-access"></a>Comprobación del acceso

El EWS está habilitado de forma predeterminada, pero los [valores predeterminados pueden cambiarse](how-to-control-access-to-ews-in-exchange.md). Use el cmdlet [Get-OrganizationConfig](https://technet.microsoft.com/library/bb124754.aspx) para asegurarse de que EWS está habilitado en el servidor, y el cmdlet [Get-CASMailbox](https://technet.microsoft.com/library/aa997571.aspx) para asegurarse de que EWS está habilitado para el buzón del usuario. Compruebe también las respuestas de ambos cmdlets para ver si hay una lista de permisos o bloqueos de EWS, y asegúrese de que su aplicación no está bloqueada para usar EWS. 
  
También debe verificar que la [configuración de autenticación por defecto](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx) en el directorio virtual de EWS no ha sido modificada. 
  
## <a name="try-another-ews-client"></a>Probar otro cliente EWS

A veces es útil probar la misma solicitud desde otro cliente y comparar los resultados. Si otro cliente obtiene resultados diferentes, ¿cuál es la diferencia? Averiguar cuál es la diferencia entre una solicitud exitosa y una fallida puede ayudar a explicar por qué una solicitud en particular está fallando.
  
Si bien es cierto que puede escribir otro cliente para probarlo, no tiene por qué hacerlo. [EWSEditor](http://ewseditor.codeplex.com/) es un ejemplo de cliente que utiliza la API administrada de EWS y EWS. Puede descargar el cliente (incluyendo el código fuente) y usarlo para intentar las mismas peticiones que están fallando en la aplicación. 
  
## <a name="examine-iis-logs"></a>Examinar los registros de IIS

Si tiene acceso al servidor Exchange, la funcionalidad de registro proporcionada por Internet Information Services (IIS) en los servidores de Acceso de Clientes puede proporcionar más información sobre los fallos. Sin embargo, tenga en cuenta que los registros de IIS sólo serán útiles si recibe un error HTTP.
  
IIS proporciona dos métodos de registro diferentes: [Registro de IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) y [rastreo de solicitudes fallidas](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Para trabajar con los registros de IIS, puede utilizar [Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), que incluye una serie de consultas EWS incorporadas.
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_NextSteps"> </a>

Ahora que ya conoce las herramientas y los recursos que puede usar para solucionar problemas, es posible que necesite ayuda para entender la información que proporcionan esas herramientas. A continuación se indican algunas opciones para obtener ayuda:
  
- [Foro de desarrollo de Exchange Server en MSDN](https://social.msdn.microsoft.com/Forums/home?category=exchangeserver) — Haga una pregunta a la comunidad de desarrollo de MSDN Exchange Server. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews): Hacer una pregunta a la comunidad StackOverflow. Asegúrese de etiquetar su publicación con "ews". 
    
- [Soporte técnico de Microsoft](https://support.microsoft.com/ph/730/en-us): Póngase en contacto con un profesional de soporte técnico de Microsoft para obtener ayuda. 
    
## <a name="see-also"></a>Consulte también


Consulte los siguientes artículos:
  
- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Instrumentación de solicitudes de clientes para EWS y REST en Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [Limitación de EWS en Exchange](ews-throttling-in-exchange.md)
    
- [Actualizar la información de configuración mediante la detección automática](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Manejo de errores relacionados con las notificaciones en EWS en Exchange ](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Manejo de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Manejo de errores relacionados con el borrado en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Configuración del registro en IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Solución de problemas de solicitudes fallidas mediante el rastreo en IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Introducción: Log Parser Studio](https://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Configuración predeterminada para directorios virtuales de Exchange](https://technet.microsoft.com/library/gg247612%28v=exchg.150%29.aspx)
    
Descargar lo siguiente:
  
- [Monitor de red de Microsoft 3.4](https://www.microsoft.com/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [API administrada de servicios Web Exchange](https://www.nuget.org/packages/Microsoft.Exchange.WebServices/)
