---
title: Instrumentación de solicitudes de cliente para EWS y REST en Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Obtenga información sobre los encabezados HTTP en las solicitudes y respuestas de EWS y REST que pueden ayudarle a supervisar y solucionar problemas de Exchange aplicación.
ms.openlocfilehash: f32a164436a1f8ab06192e71a287f5092fe9a6c4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520993"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Instrumentación de solicitudes de cliente para EWS y REST en Exchange

Obtenga información sobre los encabezados HTTP en las solicitudes y respuestas de EWS y REST que pueden ayudarle a supervisar y solucionar problemas de Exchange aplicación.
  
¿Alguna vez te ha pasado esto? Un usuario de la aplicación informa de un error inesperado. Desea investigar, pero no puede reproducirlo. El error ha desaparecido para el usuario y se le quedan muy pocos datos que se pueden actuar. Frustrante, ¿no? Veamos cómo puede prepararse proactivamente para este escenario y, con suerte, evitar la frustración en el futuro.
  
## <a name="add-instrumentation-to-requests"></a>Agregar instrumentación a las solicitudes

Se recomienda agregar encabezados HTTP adicionales a las solicitudes para facilitar la solución de problemas. Debe mantener un registro de esta información en algún lugar (por ejemplo, en un archivo de registro) para poder recuperarla más adelante si es necesario. Esto es útil al examinar el tráfico de red y también es útil si se contacta con el soporte técnico de Microsoft para obtener ayuda.
  
**Tabla 1. Encabezados de solicitud para solucionar problemas**

|**Encabezado HTTP (EWS)**|**Equivalente de API administrada ews**|**Notas**|
|:-----|:-----|:-----|
|User-Agent  <br/> |[ExchangeService.UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Esta opción se establece en un valor único que identifique la aplicación cliente.<br/><br/> Usar el mismo valor para todas las solicitudes que envía la aplicación permite a Microsoft ayudar a solucionar errores de llamadas, en caso de que surjan.  <br/> |
|client-request-id  <br/> |[ExchangeService.ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Esta opción se establece en un valor único diferente para cada solicitud que envíe la aplicación.<br/><br/> Se recomienda usar un GUID. Este identificador único está pensado para usarse para correlacionar actividades entre dos sistemas en caso de que algo salga mal.  <br/> |
|return-client-request-id  <br/> |[ExchangeService.ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Esta opción se establece en **true** para indicar al servidor Exchange que debe devolver el valor de su client-request-id en la respuesta correspondiente.<br/><br/> Puede usar esto para correlacionar solicitudes y respuestas en seguimientos de red o seguimientos de API administrada ews.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Se usa [para notificar las latencias de EWS](#bk_ReportLatency) a Microsoft si la aplicación tiene acceso a Exchange Online o Exchange Online como parte de Office 365.  <br/> |
   
## <a name="log-information-from-responses"></a>Registrar información de respuestas

Al igual que el cliente puede agregar instrumentación adicional a las solicitudes que envía, Exchange instrumentación adicional a las respuestas en forma de encabezados HTTP. El cliente debe capturar esta información para ir junto con la información de instrumentación de solicitud.
  
> [!NOTE]
> Si usa la API administrada ews, no hay equivalente directo para los encabezados HTTP. Sin embargo, se puede obtener acceso a todos los encabezados de respuesta HTTP a través de la [propiedad ExchangeService.HttpResponseHeaders.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) 
  
**Tabla 2. Encabezados de respuesta HTTP**

|**Encabezado HTTP**|**Descripción**|
|:-----|:-----|
|request-id  <br/> |Un identificador generado por el servidor para la solicitud que corresponde a esta respuesta.  <br/> |
|client-request-id  <br/> |Valor del encabezado client-request-id de la solicitud.<br/><br/> Este encabezado solo está presente si la solicitud contiene el encabezado return-client-request-id con un valor de **true**.  <br/> |
|X-FEServer  <br/> |FQDN del servidor de acceso de cliente que procesó la solicitud.  <br/> |
|X-TargetBEServer  <br/> |FQDN del servidor de buzones de correo que procesó la solicitud.  <br/> |
|X-DiagInfo  <br/> |Información de diagnóstico adicional, según la solicitud.  <br/> |
|x-ms-diagnostics  <br/> | Este encabezado solo es aplicable si se usa la autenticación de OAuth en la solicitud.<br/><br/> Contiene un código de error explícito que especifica por qué se produjo un error en la autenticación de OAuth.<br/><br/> Tiene el siguiente formato: `errorId;reason="reason"error_type="error type"`<br/><br/> El **campo motivo** es una descripción legible del error.<br/><br/> El **campo errorId** es un número entero y el campo **de tipo de error \_** es la representación de cadena de ese entero, como se muestra a continuación:<ul><li>2000000: firma \_ no válida</li><li>2000001: token \_ no válido</li><li>  2000002: token \_ expirado</li><li>2000003: recurso \_ no válido</li><li>2000004: inquilino \_ no válido  </li><li>2000005: usuario \_ no válido</li><li>2000006: cliente \_ no válido</li><li>2000007: error \_ interno</li><li>2000008: concesión \_ no válida</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Notificar latencia ews a Microsoft
<a name="bk_ReportLatency"> </a>

Si la aplicación usa la API administrada ews o EWS para conectarse a Exchange Online, puede notificar la latencia de las solicitudes EWS directamente a Microsoft. La información se pasa a través del encabezado de solicitud X-ClientStatistics. Si usa la API administrada ews, todo lo que tiene que hacer es establecer la propiedad [ExchangeService.SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) en **true**. Si usa EWS, deberá medir el tiempo entre emitir una solicitud y recibir una respuesta y, a continuación, agregar el encabezado X-ClientStatistics a la siguiente solicitud EWS que envíe la aplicación, con el siguiente formato.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Mantenemos informes de estas latencias y las usamos para mejorar continuamente los servicios EWS en Exchange Online.
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_ReportLatency"> </a>

Después de agregar instrumentación de cliente a la aplicación, está mejor preparado si algo sale mal. Si esto ocurre, puede usar los datos de instrumentación para [solucionar problemas de la aplicación](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md).
  
## <a name="see-also"></a>Ver también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Herramientas y recursos para solucionar problemas de aplicaciones EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

