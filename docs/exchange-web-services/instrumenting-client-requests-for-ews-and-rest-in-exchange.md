---
title: Instrumentación de las solicitudes de cliente para EWS y REST en Exchange
manager: sethgros
ms.date: 4/13/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 330de503-498d-447e-b4a9-c20fc1699fd1
description: Obtenga información acerca de los encabezados HTTP en EWS y solicitudes REST y las respuestas que pueden ayudarle a supervisión y solucionar problemas de la aplicación de Exchange.
ms.openlocfilehash: bcf362952c29956729c44397043a56bf3603d0af
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763200"
---
# <a name="instrumenting-client-requests-for-ews-and-rest-in-exchange"></a>Instrumentación de las solicitudes de cliente para EWS y REST en Exchange

Obtenga información acerca de los encabezados HTTP en EWS y solicitudes REST y las respuestas que pueden ayudarle a supervisión y solucionar problemas de la aplicación de Exchange.
  
¿Esto nunca pasó a usted? Un usuario de la aplicación informa de un error inesperado. Que desea investigar, pero no puede reproducirlo. Ha desaparecido el error para el usuario y está izquierda con muy poca datos procesables. Frustrante, ¿no? Veamos cómo puede prepararse para este escenario de forma proactiva y es de esperar que evite frustraciones en el futuro.
  
## <a name="add-instrumentation-to-requests"></a>Agregar instrumentación a las solicitudes

Se recomienda que agregue encabezados HTTP adicionales a las solicitudes para facilitar la solución de problemas. Debe mantener un registro de esta información en algún lugar (por ejemplo, en un archivo de registro) para que pueda recuperar más adelante si es necesario. Esto resulta útil para examinar el tráfico de red y también es útil si póngase en contacto con soporte técnico de Microsoft para obtener ayuda.
  
**La tabla 1. Encabezados de la solicitud para la solución de problemas**

|**Encabezado HTTP (EWS)**|**Equivalente de la API administrada de EWS**|**Notas**|
|:-----|:-----|:-----|
|Agente de usuario  <br/> |[ExchangeService.UserAgent](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.useragent%28v=exchg.80%29.aspx) <br/> |Establecerlo en un valor único que identifica la aplicación cliente.<br/><br/> Con el mismo valor para todas las solicitudes que su aplicación envía permite a Microsoft ayudar a solucionar problemas de errores de llamadas, debe se produzcan.  <br/> |
|identificador de solicitud de cliente  <br/> |[ExchangeService.ClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.clientrequestid%28v=exchg.80%29.aspx) <br/> |Establezca un valor único diferente para cada solicitud de que la aplicación envía.<br/><br/> Se recomienda que use un GUID. Este identificador único está destinado a ser utilizado para correlacionar las actividades entre dos sistemas en caso de que algo salga mal.  <br/> |
|retorno--solicitud-identificador de cliente  <br/> |[ExchangeService.ReturnClientRequestId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.returnclientrequestid%28v=exchg.80%29.aspx) <br/> |Debe establecer en **true** para señalar al servidor de Exchange que debe devolver el valor de su identificador de solicitud de cliente en la respuesta correspondiente.<br/><br/> Puede usar esto para correlacionar las solicitudes y respuestas en los seguimientos de red o los seguimientos de la API administrada de EWS.  <br/> |
|X-ClientStatistics  <br/> |[ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) <br/> |Se usa para [las latencias EWS informe](#bk_ReportLatency) a Microsoft si su aplicación tenga acceso a Exchange Online o Exchange Online como parte de Office 365.  <br/> |
   
## <a name="log-information-from-responses"></a>Información de registro de las respuestas proporcionadas

Al igual que el cliente puede agregar instrumentación adicional a las solicitudes que se envía, Exchange agrega instrumentación adicional a las respuestas en el formulario de encabezados HTTP. El cliente debe capturar esta información para ir junto con la información de Instrumental de solicitud.
  
> [!NOTE]
> Si está utilizando la API administrada de EWS, no hay ningún equivalente directo para los encabezados HTTP. Sin embargo, se pueden tener acceso a todos los encabezados de respuesta HTTP a través de la propiedad [ExchangeService.HttpResponseHeaders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.httpresponseheaders%28v=exchg.80%29.aspx) . 
  
**Tabla 2. Encabezados de respuesta HTTP**

|**Encabezado HTTP**|**Descripción**|
|:-----|:-----|
|identificador de la solicitud  <br/> |Un identificador generado por el servidor para la solicitud que corresponde a esta respuesta.  <br/> |
|identificador de solicitud de cliente  <br/> |El valor del encabezado del identificador de solicitud de cliente en la solicitud.<br/><br/> Este encabezado sólo está presente si la solicitud contiene el encabezado de retorno--solicitud-identificador de cliente con un valor de **true**.  <br/> |
|X-FEServer  <br/> |El FQDN del servidor de acceso de cliente que procesa la solicitud.  <br/> |
|X-TargetBEServer  <br/> |El FQDN del servidor de buzón de correo que procesa la solicitud.  <br/> |
|X-DiagInfo  <br/> |Información de diagnóstico adicional, dependiendo de la solicitud.  <br/> |
|x-ms-diagnostics  <br/> | Este encabezado solo es aplicable si se utiliza la autenticación de OAuth en la solicitud.<br/><br/> Contiene un código de error explícita que se especifica por qué no se pudo una autenticación de OAuth.<br/><br/> Toma el siguiente formato:`errorId;reason="reason"error_type="error type"`<br/><br/> El campo **motivo** es una descripción legible del error.<br/><br/> El campo de **identificador del error** es un número entero y el **error\_tipo** campo es la representación de cadena de ese número entero, como se indica a continuación:<ul><li>2000000: no válido\_firma</li><li>2000001: no válido\_símbolo (token)</li><li>  2000002: símbolo (token)\_expirado</li><li>2000003: no válido\_recursos</li><li>2000004: no válido\_inquilino  </li><li>2000005: no válido\_usuario</li><li>2000006: no válido\_cliente</li><li>2000007: interno\_error</li><li>2000008: no válido\_conceder</li></ul> |
   
## <a name="report-ews-latency-to-microsoft"></a>Latencia EWS informe a Microsoft
<a name="bk_ReportLatency"> </a>

Si la aplicación utiliza la API administrada de EWS o EWS para conectarse a Exchange Online, puede informar de latencia en las solicitudes EWS directamente a Microsoft. La información se pasa a través del encabezado de solicitud de X-ClientStatistics. Si está utilizando la API administrada de EWS, todo lo que tiene que hacer es establecer la propiedad [ExchangeService.SendClientLatencies](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservicebase.sendclientlatencies%28v=exchg.80%29.aspx) en **true**. Si usa EWS, que necesitará para medir el tiempo entre emitir una solicitud y recibir una respuesta, a continuación, agregue el encabezado X-ClientStatistics a la siguiente solicitud EWS envía la aplicación, con el siguiente formato.
  
`X-ClientStatistics: MessageId=<value of request-id header>,ResponseTime=<time in milliseconds>,SoapAction=<EWS operation>`
  
Mantenemos informes para estos latencias y usarlos para mejorar continuamente los servicios EWS en Exchange Online.
  
## <a name="next-steps"></a>Siguientes pasos
<a name="bk_ReportLatency"> </a>

Después de agregar instrumentación del cliente a la aplicación, está preparado mejor si se produce algún error. Si esto ocurre, puede usar los datos de instrumentación para [solucionar problemas de la aplicación](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md).
  
## <a name="see-also"></a>Vea también

- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
- [Seguimiento de las solicitudes y respuestas para solucionar problemas de aplicaciones de la API administrada de EWS](how-to-trace-requests-responses-to-troubleshoot-ews-managed-api-applications.md)
- [Herramientas y recursos para solucionar problemas de aplicaciones de EWS para Exchange](tools-and-resources-for-troubleshooting-ews-applications-for-exchange.md)
    

