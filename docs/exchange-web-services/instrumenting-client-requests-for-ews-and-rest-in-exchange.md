---
title: Instrumentar solicitudes de cliente para EWS y REST en Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Obtenga información sobre los encabezados HTTP en las solicitudes y respuestas REST de EWS y que pueden ayudarle a supervisar y solucionar problemas de su aplicación Exchange.
ms.openlocfilehash: 3a8ce889ec7a6b9e70ec25a95ac248902f48ca6c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456307"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Instrumentar solicitudes de cliente para EWS y REST en Exchange

Obtenga información sobre los encabezados HTTP en las solicitudes y respuestas REST de EWS y que pueden ayudarle a supervisar y solucionar problemas de su aplicación Exchange.
  
¿Le ha sucedido alguna vez? Un usuario de la aplicación informa de un error inesperado. Desea investigar, pero no puede reproducirlo. El error ha desaparecido para el usuario y quedará con muy pocos datos que requieren acción. Frustrante, ¿no? Veamos cómo puede prepararse de forma proactiva para este escenario y, afortunadamente, evitar la frustración en el futuro.
  
## <a name="add-instrumentation-to-requests"></a>Agregar instrumentación a las solicitudes

Le recomendamos que agregue encabezados HTTP adicionales a sus solicitudes para facilitar la solución de problemas. Debe mantener un registro de esta información en algún lugar (por ejemplo, en un archivo de registro) para poder recuperarla más adelante si es necesario. Esto es útil al examinar el tráfico de red y también es útil si se pone en contacto con el soporte técnico de Microsoft para obtener ayuda.
  
**Tabla 1. Encabezados de solicitud para la solución de problemas**

|**Encabezado HTTP (EWS)**|**Equivalente de API administrada de EWS**|**Notas**|
|:-----|:-----|:-----|
|Agente de usuario  <br/> |[ExchangeService. UserAgent](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Establézcalo en un valor único que identifique la aplicación cliente.<br/><br/> Usar el mismo valor para todas las solicitudes que envía la aplicación permite que Microsoft Ayude a solucionar los errores de llamada, en caso de que se produzcan.  <br/> |
|identificador de solicitud de cliente  <br/> |[ExchangeService. ClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Establézcalo en un valor único diferente para cada solicitud que envíe la aplicación.<br/><br/> Le recomendamos que use un GUID. Este identificador único está pensado para usarse para correlacionar actividades entre dos sistemas en el caso de que algo vaya mal.  <br/> |
|Return-Client-request-ID  <br/> |[ExchangeService. ReturnClientRequestId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Establézcalo en **true** para indicar al servidor de Exchange que debe devolver el valor del identificador de solicitud de cliente en la respuesta correspondiente.<br/><br/> Puede usar esto para correlacionar las solicitudes y respuestas en los seguimientos de red o los seguimientos de API administrada de EWS.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService. SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Se usa para [informar de latencias de EWS](#bk_ReportLatency) a Microsoft si su aplicación tiene acceso a Exchange online o Exchange online como parte de Office 365.  <br/> |
   
## <a name="log-information-from-responses"></a>Registrar información de respuestas

Al igual que el cliente puede Agregar instrumental adicional a las solicitudes que envía, Exchange agrega instrumental adicional a las respuestas en forma de encabezados HTTP. El cliente debe capturar esta información para ir junto con la información de instrumentación de la solicitud.
  
> [!NOTE]
> Si usa la API administrada de EWS, no hay equivalente directo para los encabezados HTTP. Sin embargo, se puede tener acceso a todos los encabezados de respuesta HTTP a través de la propiedad [ExchangeService. HttpResponseHeaders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) . 
  
**Tabla 2. Encabezados de respuesta HTTP**

|**Encabezado HTTP**|**Descripción**|
|:-----|:-----|
|identificador de solicitud  <br/> |IDENTIFICADOR generado por el servidor para la solicitud que corresponde a esta respuesta.  <br/> |
|identificador de solicitud de cliente  <br/> |El valor del encabezado de identificador de solicitud de cliente en la solicitud.<br/><br/> Este encabezado solo está presente si la solicitud contiene el encabezado Return-Client-request-ID con un valor **true**.  <br/> |
|X-FEServer  <br/> |El FQDN del servidor de acceso de cliente que procesó la solicitud.  <br/> |
|X-TargetBEServer  <br/> |El FQDN del servidor de buzones de correo que ha procesado la solicitud.  <br/> |
|X-DiagInfo  <br/> |Información de diagnóstico adicional, según la solicitud.  <br/> |
|x-MS-Diagnostics  <br/> | Este encabezado solo se aplica si se usa la autenticación OAuth en la solicitud.<br/><br/> Contiene un código de error explícito que especifica por qué se produjo un error en la autenticación OAuth.<br/><br/> Tiene el siguiente formato:`errorId;reason="reason"error_type="error type"`<br/><br/> El campo **motivo** es una descripción legible del error por el usuario.<br/><br/> El campo **errorId** es un número entero y el campo ** \_ tipo de error** es la representación en forma de cadena de ese entero, de la siguiente manera:<ul><li>2 millones: firma no válida \_</li><li>2000001: token no válido \_</li><li>  2000002: token \_ expirado</li><li>2000003: recurso no válido \_</li><li>2000004: inquilino no válido \_  </li><li>2000005: usuario no válido \_</li><li>2000006: cliente no válido \_</li><li>2000007: \_ error interno</li><li>2000008: concesión no válida \_</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Informar de latencia de EWS a Microsoft
<a name="bk_ReportLatency"> </a>

Si la aplicación usa la API administrada de EWS o EWS para conectarse a Exchange Online, puede notificar la latencia en las solicitudes de EWS directamente a Microsoft. La información se pasa a través del encabezado de solicitud X-ClientStatistics. Si usa la API administrada de EWS, todo lo que tiene que hacer es establecer la propiedad [ExchangeService. SendClientLatencies](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) en **true**. Si usa EWS, deberá medir el tiempo entre emitir una solicitud y recibir una respuesta y, a continuación, agregar el encabezado X-ClientStatistics a la siguiente solicitud de EWS que envíe la aplicación, con el siguiente formato.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Mantenemos informes para estas latencias y los usamos para mejorar de forma continua los servicios EWS en Exchange Online.
  
## <a name="next-steps"></a>Pasos siguientes
<a name="bk_ReportLatency"> </a>

Una vez que haya agregado la instrumentación del cliente a la aplicación, es mejor preparado si algo va mal. Si esto ocurre, puede usar los datos de instrumentación para [solucionar los problemas de la aplicación](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md).
  
## <a name="see-also"></a>Vea también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Herramientas y recursos para solucionar problemas de las aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

