---
title: Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: ee7fcd05-35d7-47bf-bac4-e719c49c11fe
description: Encuentre recursos que le ayudarán a solucionar problemas de la API administrada de EWS o la aplicación de EWS.
ms.openlocfilehash: d8d8ea736ca3b896642ad06f5987caeba8d8d059
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763305"
---
# <a name="tools-and-resources-for-troubleshooting-ews-applications-for-exchange"></a>Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange

Encuentre recursos que le ayudarán a solucionar problemas de la API administrada de EWS o la aplicación de EWS.
  
Cosas siempre no funcione como se esperaba. A veces EWS solicita la conmutación por error, o proporcionar resultados inesperados. Esto puede ser frustrante, especialmente si el motivo no es obvio. Espero que nunca sucede esto, pero si lo hace, este artículo se proporciona información acerca de las herramientas y recursos que puede usar para ayudar a solucionar el problema.
  
> [!NOTE]
> Este artículo proporciona consejos para solucionar problemas generales y orígenes para obtener información de solución de problemas. Lamentablemente no se puede dar a los pasos detallados de solución de problemas. Para asistencia para solucionar el error específico, vea los [pasos siguientes](#bk_NextSteps). 
  
## <a name="examine-the-soap-requests-and-responses"></a>Se examinan las solicitudes y respuestas SOAP

Cuando las cosas no funcionan correctamente, resulta muy útil para poder ver lo que está ocurriendo. Es la primera línea de consulta al investigar un problema con EWS o la API administrada de EWS examinar las solicitudes de que la aplicación está enviando a través de la red y las respuestas que el servidor envía de vuelta.
  
La API administrada de EWS facilita examinar solicitudes y respuestas SOAP con su [integrado en la funcionalidad de seguimiento](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md). Si usa EWS, es posible que o no se puede tener acceso a la funcionalidad de seguimiento similar, dependiendo de qué plataforma o las clases que se usa para enviar las solicitudes. Sin embargo, siempre puede usar una herramienta de seguimiento de red como [Monitor de red](http://www.microsoft.com/en-us/download/details.aspx?id=4865) o [Fiddler](http://www.telerik.com/fiddler) para examinar el tráfico de red y ver las cargas de solicitud y respuesta. 
  
Además, puede agregar [instrumentación sus solicitudes de cliente](instrumenting-client-requests-for-ews-and-rest-in-exchange.md) para mejorar la información disponible en las solicitudes y respuestas. 
  
Una vez que tenga las solicitudes y respuestas, hágase las siguientes: ¿son correctas? ¿Son los valores que la aplicación está enviando esperada? ¿Las respuestas que tenga sentido?
  
## <a name="examine-error-codes"></a>Examinar los códigos de error

A veces el código de error puede ir mucho a identificar el problema, aunque a primera vista parece que no tiene sentido. ¿El error indica que el cliente se está [limitado](ews-throttling-in-exchange.md)? ¿Quizás una llamada a la detección automática para [actualizar la información de configuración](how-to-refresh-configuration-information-by-using-autodiscover.md) se encuentra en orden? 
  
Para obtener más información sobre el tratamiento de errores específicos, vea los siguientes artículos:
  
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la eliminación de EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="verify-versions"></a>Compruebe las versiones

Hay un número de distintos componentes implicados en las operaciones de EWS y las versiones de esos componentes pueden influir en los resultados.
  
**La tabla 1. Componentes que pueden afectar a los procesos EWS**

|**Componente**|**API administrada EWS**|**EWS**|**Notas**|
|:-----|:-----|:-----|:-----|
|Versión de servidor solicitado  <br/> |[ExchangeServiceBase.RequestedServerVersion](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.requestedserverversion%28v=exchg.80%29.aspx) (propiedad)  <br/> |Elemento [RequestServerVersion](http://msdn.microsoft.com/library/af4032d5-42b3-463e-9d0a-8236d78e5b75%28Office.15%29.aspx)  <br/> |Este valor controla qué versión del esquema EWS se utiliza para procesar la solicitud EWS. Asegúrese de que la versión del esquema especificado aquí tiene sentido para la solicitud que va a enviar. Algunas operaciones y propiedades no están disponibles en versiones anteriores del esquema.  <br/> |
|La versión del servidor  <br/> |[ExchangeServiceBase.ServerInfo](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.exchangeservicebase.serverinfo%28v=exchg.80%29.aspx) (propiedad)  <br/> |Elemento [ServerVersionInfo](http://msdn.microsoft.com/library/c04a6872-ca27-432b-aac2-36b023d0afc6%28Office.15%29.aspx)  <br/> |Este valor devuelto por el servidor en respuestas EWS e indica la versión del servidor que procesa la respuesta. Asegúrese de que este valor es el esperado. Si es posible, asegúrese de que el servidor de Exchange se está ejecutando la actualización más reciente de la versión principal de Exchange.  <br/> |
|La versión de la API administrada de EWS  <br/> |La propiedad de versión del producto del archivo Microsoft.Exchange.WebServices.dll.  <br/> |No disponible  <br/> |Si está utilizando la API administrada de EWS, asegúrese de que está usando [la versión más reciente](http://aka.ms/ews-managed-api-readme).  <br/> |
   
## <a name="verify-access"></a>Comprobación del acceso

EWS está habilitado de forma predeterminada, pero [se pueden cambiar los valores predeterminados](how-to-control-access-to-ews-in-exchange.md). Use el cmdlet [Get-OrganizationConfig](http://technet.microsoft.com/en-us/library/bb124754.aspx) para asegurarse de que EWS esté habilitado en el servidor y el cmdlet [Get-CASMailbox](http://technet.microsoft.com/en-us/library/aa997571.aspx) para asegurarse de que EWS está habilitado para el buzón del usuario. También comprobar ambas respuestas de cmdlet para una dirección URL de EWS permitirán o bloquean lista y asegúrese de que no se bloquea la aplicación de uso de EWS. 
  
También debe comprobar que la [configuración de autenticación predeterminada](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx) en el directorio virtual de EWS no se han modificado. 
  
## <a name="try-another-ews-client"></a>Probar con otro cliente EWS

En ocasiones, es útil probar la misma solicitud desde otro cliente y comparar los resultados. Si otro cliente obtiene resultados diferentes, ¿qué es diferente? Averiguar qué es diferente entre la solicitud es correcta y una solicitud errónea puede ayudar a explicar por qué se están produciendo errores de una solicitud en particular.
  
Mientras que sin duda puede escribir otro cliente para probar con, no es necesario! [EWSEditor](http://ewseditor.codeplex.com/) es un cliente de ejemplo que usa la API administrada de EWS y EWS. Puede descargar al cliente (incluido el código de origen) y usarlo para probar las mismas solicitudes que se producen errores en la aplicación. 
  
## <a name="examine-iis-logs"></a>Examine los registros de IIS

Si tiene acceso al servidor de Exchange, la funcionalidad de registro proporcionada por Internet Information Services (IIS) en los servidores de acceso de cliente puede proporcionar más información acerca de los errores. Sin embargo, tenga en cuenta que los registros de IIS sólo será útil si recibe un error HTTP.
  
IIS proporciona dos métodos diferentes de registro: [el registro de IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis) y [seguimiento de solicitudes erróneas](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis). Para trabajar con los registros de IIS, puede utilizar [Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx), que incluye un número de consultas EWS integradas.
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_NextSteps"> </a>

Ahora que ha aprendido acerca de las herramientas y recursos que puede usar para solucionar problemas, puede que necesite ayuda para comprender la información proporcionada por dichas herramientas. Las siguientes son algunas de las opciones para obtener ayuda:
  
- [Foro de desarrollo de Exchange Server en MSDN](http://social.msdn.microsoft.com/Forums/en-US/home?category=exchangeserver) : formular una pregunta de la Comunidad de desarrollo de MSDN Exchange Server. 
    
- [StackOverflow](http://stackoverflow.com/tags/ews) : formular una pregunta de la Comunidad de StackOverflow. Asegúrese de marcar la entrada de blog con "ews". 
    
- [Soporte técnico de Microsoft](http://support.microsoft.com/ph/730/en-us) , póngase en contacto con un profesional de soporte técnico de Microsoft para obtener ayuda. 
    
## <a name="see-also"></a>Ver también


Vea los siguientes artículos:
  
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
    
- [Instrumentación de las solicitudes de cliente para EWS y REST en Exchange](instrumenting-client-requests-for-ews-and-rest-in-exchange.md)
    
- [EWS limitación en Exchange](ews-throttling-in-exchange.md)
    
- [Actualizar información de configuración mediante el uso de detección automática](how-to-refresh-configuration-information-by-using-autodiscover.md)
    
- [Administrar los mensajes de error de detección automática](handling-autodiscover-error-messages.md)
    
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la eliminación de EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
- [Configuración del registro en IIS](http://www.iis.net/learn/manage/provisioning-and-managing-iis/configure-logging-in-iis)
    
- [Solución de problemas de error de solicitudes mediante el seguimiento en IIS 7](http://www.iis.net/learn/troubleshoot/using-failed-request-tracing/troubleshooting-failed-requests-using-tracing-in-iis)
    
- [Introducción: Log Parser Studio](http://blogs.technet.com/b/exchange/archive/2012/03/07/introducing-log-parser-studio.aspx)
    
- [Configuración predeterminada de los directorios virtuales de Exchange](http://technet.microsoft.com/en-us/library/gg247612%28v=exchg.150%29.aspx)
    
Descargar lo siguiente:
  
- [Microsoft Network Monitor 3.4](http://www.microsoft.com/en-us/download/details.aspx?id=4865)
    
- [Fiddler](http://www.telerik.com/fiddler)
    
- [EWSEditor](http://ewseditor.codeplex.com/)
    
- [API administrada de servicios Web de Exchange](http://go.microsoft.com/fwlink/?LinkID=255472)
    

