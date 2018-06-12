---
title: Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1bda4094-88c3-4f61-9219-6ee70f6e81cf
description: Obtenga información acerca de mantener la afinidad entre un grupo de suscripciones y el servidor de buzón de correo.
ms.openlocfilehash: 7cfbfb5cc19e092c37e3d48a7fcc4f27023516e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763088"
---
# <a name="maintain-affinity-between-a-group-of-subscriptions-and-the-mailbox-server-in-exchange"></a>Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange

Obtenga información acerca de mantener la afinidad entre un grupo de suscripciones y el servidor de buzón de correo.
  
La afinidad es la asociación de una secuencia de mensajes de solicitud y respuesta con un determinado servidor de buzón de correo. Para la mayoría de las funciones de Exchange, el servidor controla la afinidad. Las notificaciones, sin embargo, son una excepción. El cliente es responsable de mantener la afinidad con el servidor de buzón de correo para las suscripciones de notificación. Esta afinidad permite el equilibrador de carga y servidores de acceso de cliente entre el cliente y el servidor para las suscripciones de notificación de ruta y solicitudes relacionadas en el servidor de buzón de correo que se mantiene la suscripción. Sin afinidad, la solicitud es posible que se enrutan a un servidor de buzón de correo diferente que no incluya las suscripciones del cliente, lo que pueden causar un error de [ErrorSubscriptionNotFound](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) que se va a devolver. 
  
## <a name="how-is-affinity-maintained"></a>¿Cómo se mantiene la afinidad?
<a name="bk_howmaintained"> </a>

Afinidad de Exchange es cookie según se indique. El cliente desencadena la creación de la cookie mediante la inclusión de los encabezados específicos en la solicitud de suscripción y, a continuación, la respuesta de suscripción contiene la cookie. El cliente envía a continuación, ese cookie en las solicitudes posteriores para asegurarse de que la solicitud se enruta al servidor de buzón de correo correcto.
  
Más concretamente, afinidad en Exchange se controla mediante el siguiente: 
  
- X-AnchorMailbox: Un encabezado que se incluye en la solicitud de suscripción inicial. Identifica el primer buzón de correo en un grupo de buzones que comparten afinidad con el mismo servidor de buzón de correo.
    
- X-PreferServerAffinity: Un encabezado HTTP que se incluye en la solicitud de suscripción inicial con el encabezado X-AnchorMailbox y se establece en true para indicar que el cliente solicita que se mantenga la afinidad con el servidor de buzones.
    
- X-BackEndOverrideCookie: Una cookie que se incluye en la respuesta de suscripción inicial y contiene una cookie que el equilibrador de carga y el servidor de acceso de cliente que se usan para enrutar las solicitudes posteriores en el mismo servidor de buzón de correo.
    
## <a name="how-do-i-maintain-affinity-by-using-the-ews-managed-api-or-ews"></a>¿Cómo se puede mantener la afinidad mediante el uso de la API administrada de EWS o EWS?
<a name="bk_howdoimaintain"> </a>

Puede usar los mismos pasos para mantener la afinidad para varias suscripciones de buzón de correo y sus servidores de buzones de correo, independientemente de si está utilizando la transmisión por secuencias, extracción o notificaciones de inserción, independientemente de si posea un Exchange locales y en servidor o Exchange Online.
  
1. Para cada buzón de correo, [detección automática de llamadas](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) y obtener la configuración de usuario GroupingInformation y ExternalEwsUrl. Para la detección automática de SOAP, use el elemento de [configuración](http://msdn.microsoft.com/library/43db26e1-f7be-49fd-b26b-fc1b10bd3458%28Office.15%29.aspx) y para la detección automática de POX, se utiliza el elemento de [GroupingInformation](http://msdn.microsoft.com/library/2d8a007f-d79c-43c8-90e3-2c6d883f3a7c%28Office.15%29.aspx) . 
    
2. Con la configuración de GroupingInformation y ExternalEwsUrl de las respuestas de detección automática, los buzones de correo electrónicos con el mismo ExternalEwsUrl y GroupingInformation concatena el valor en el mismo grupo. Si los grupos tienen más de 200 buzones, desglosar los grupos adicionales para que cada grupo tiene buzones no más de 200.
    
3. Crear y usar un objeto [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=EXCHG.80%29.aspx) para el resto del procedimiento. Cuando se usa el mismo **ExchangeService** objeto, cookies y encabezados (cuando se establecen) se mantienen automáticamente. Tenga en cuenta que si no desea suscripciones de transmisión por secuencias de grupo en una sola conexión, está libre para crear un objeto **ExchangeService** diferente para cada usuario suplantado. 
    
4. [Enviar una suscripción a](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) la solicitud para el usuario cuyo nombre de usuario aparece en primer lugar cuando todos los usuarios en el grupo se ordenan alfabéticamente (nos referiremos a este usuario como el usuario de buzón de correo de anclaje). Haga lo siguiente: 
    
  - Incluir el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario de buzón de correo de delimitador.
    
  - Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.
    
  - Use la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ). 
    
5. En la respuesta de suscripción, obtener el valor de X-BackEndOverrideCookie. Incluir este valor en cada una de las solicitudes posteriores de suscripción para los usuarios de este grupo.
    
6. Para cada usuario adicional en el grupo, envíe una solicitud de suscripción y haga lo siguiente:
    
  - Incluir el encabezado X-AnchorMailbox con un valor establecido en la dirección SMTP del usuario de buzón de correo de anclaje para el grupo.
    
  - Incluya el encabezado X-PreferServerAffinity con un valor establecido en true.
    
  - Incluir X-BackEndOverrideCookie que se devuelve en respuesta de suscripción del usuario de buzón de correo de delimitador.
    
  - Use la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) (el tipo [ExchangeImpersonation](http://msdn.microsoft.com/library/d8cbac49-47d0-4745-a2a7-545d33f8da93%28Office.15%29.aspx) ). 
    
    Tenga en cuenta que el servidor utiliza los valores de X-PreferServerAffinity y X-BackendOverrideCookie conjuntamente para realizar el enrutamiento para el servidor de buzones. El encabezado X-AnchorMailbox también es necesario, pero se omite el servidor si los dos valores son válidos. Si X-AnchorMailbox y X-PreferServerAffinity se encuentran en una solicitud y BackendOverrideCookie de X no se incluye, el valor de X-AnchorMailbox se usa para enrutar las solicitudes.
    
    Debido a que los valores de X-BackendOverrideCookie y X-PreferServerAffinity realizan el enrutamiento, si el buzón de correo de anclaje nunca se mueve a otro servidor o grupo, no cambie la lógica de debido a que la X-BackendOverrideCookie usará para enrutar la solicitud al servidor correcto para el grupo.
    
7. Enviar un único [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o solicitudes [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) para el grupo y haga lo siguiente: 
    
  - Incluir los valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) devueltos en cada una de las respuestas de suscripción individual para los buzones de correo en el grupo. 
    
  - Si existen más de 200 suscripciones para el grupo, crear varias solicitudes. El número máximo de valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) para incluir en una solicitud es 200. 
    
  - Si necesita más conexiones que están disponibles en el buzón de destino, use la cuenta de servicio para suplantar el buzón de correo de anclaje para el grupo; de lo contrario, no utilice la suplantación. Lo ideal es que desee suplantar a un único buzón por solicitud [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) o [GetEvents](http://msdn.microsoft.com/library/22d4da6b-d8a8-484f-82c4-3e4b8f5431cd%28Office.15%29.aspx) para evitar que no se produzcan nunca los límites de limitación de peticiones. 
    
  - Usar ApplicationImpersonation si necesita [más conexiones que están disponibles en el buzón de destino](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling); de lo contrario, no utilice ApplicationImpersonation.
    
  - Incluya el encabezado X-PreferServerAffinity y establézcalo en true. Este valor se incluye automáticamente si está utilizando el objeto **ExchangeService** que creó en el paso 2. 
    
  - Incluir la X-BackEndOverrideCookie para el grupo (la X-BackEndOverrideCookie que se devuelve en respuesta de suscripción del usuario de buzón de correo de anclaje). Este valor se incluye automáticamente si está utilizando el objeto **ExchangeService** que creó en el paso 2. 
    
8. Pase los eventos devueltos a un subproceso independiente para su procesamiento.
    
## <a name="what-throttling-values-do-i-need-to-take-into-consideration"></a>¿Qué valores de limitación de peticiones es necesario tener en cuenta?
<a name="bk_throttling"> </a>

Cuando planee la implementación de la notificación, querrá tener dos valores en cuenta: el número de conexiones y el número de suscripciones. En la siguiente tabla se enumera los valores predeterminados para cada opción de [limitación de peticiones](ews-throttling-in-exchange.md) y cómo se usa la configuración. Para cada valor, se asigna el presupuesto en el buzón de destino. Por este motivo, el uso de suplantación para conexiones adicionales de ganancia es un paso necesario en muchos escenarios. 
  
**La tabla 1. Limitación de los valores predeterminados**

|**Área de consideración**|**Configuración de limitación**|**Valor predeterminado**|**Descripción**|
|:-----|:-----|:-----|:-----|
|Conexiones de transmisión por secuencias  <br/> |Predeterminado de sangría límite de conexión  <br/> |10 para Exchange Online  <br/> 3 para Exchange 2013  <br/> |El número máximo de conexiones simultáneas de transmisión por secuencias que una cuenta puede tener abiertas a la vez en el servidor. Para que funcione dentro de este límite, utilice una cuenta de servicio con la función ApplicationImpersonation asignada a los buzones de correo de destino y representar al primer usuario en cada grupo de identificador de suscripción cuando Introducción transmitir eventos.  <br/> |
|Extracción o inserción de conexiones  <br/> |EWSMaxConcurrency  <br/> |27  <br/> |El número máximo de conexiones simultáneas de extracción o inserción (las solicitudes que se han recibido pero que aún no se ha respondido a) que una cuenta de a la vez puede tener abiertas en el servidor.  <br/> |
|Suscripciones  <br/> |EWSMaxSubscriptions  <br/> |20 para Exchange Online  <br/> 5000 para Exchange 2013  <br/> |El número máximo de suscripciones nonexpired que una cuenta puede tener al mismo tiempo. Este valor es disminuye cuando se crea la suscripción en el servidor.  <br/> |
   
En el ejemplo siguiente se muestra cómo se controlan los presupuestos entre cualquier buzón de correo de destino y la cuenta de servicio que tiene la función [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx) asignada a los buzones de correo de destino. 
  
- ServiceAccount1 (sa1) suplanta muchos usuarios (m1, m2, m3 y así sucesivamente) y crea suscripciones para cada buzón de correo. Tenga en cuenta que cuando se crean las suscripciones, el propietario de la suscripción es sa1, por lo que cuando sa1 abre una conexión con las suscripciones, EWS exige que las suscripciones pertenecen a sa1.
    
- Sa1 puede abrir la conexión de las siguientes maneras:
    
1. Sin suplantación, lo que la conexión se atribuyen a sa1.
    
2. Mediante la suplantación de cualquiera de los usuarios: m1, por ejemplo, para que la conexión se contabiliza en una copia del presupuesto de m1. (M1 sí puede abrir diez conexiones mediante el uso de Exchange Online y todas las cuentas de servicio suplantación m1 pueden abrir diez conexiones utilizando el presupuesto copiado.)
    
- Si se alcanza el límite de conexión, están disponibles las siguientes soluciones alternativas:
    
  - Si se usa la opción 1, el administrador puede crear varias cuentas de servicio para suplantar a los usuarios adicionales.
    
  - Si se usa la opción 2, el código puede suplantar a otro usuario: m2, por ejemplo.
    
## <a name="example-maintaining-affinity-between-a-group-of-subscriptions-and-the-mailbox-server"></a>Ejemplo: Mantenimiento de afinidad entre un grupo de suscripciones y el servidor de buzón de correo
<a name="bk_ce"> </a>

Bien, veamos en acción. En el ejemplo de código siguiente se muestra cómo agrupar los usuarios y usar los encabezados X-AnchorMailbox y X-PreferServerAffinity y la cookie de X-BackendOverrideCookie para mantener la afinidad con el servidor de buzones. Debido a que los encabezados y la cookie son de importancia principal en la historia de afinidad, en este ejemplo se centra en las solicitudes de EWS XML y respuestas. Para usar la API administrada de EWS para crear el cuerpo de las respuestas y solicitudes de suscripción, vea [notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md) y [extraer las notificaciones sobre los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md). En esta sección se incluye particular, pasos adicionales para mantener la afinidad y agregar los encabezados a las solicitudes.
  
Este ejemplo tiene cuatro usuarios: alfred@contoso.com, alisa@contoso.com, ronnie@contoso.com y sadie@contoso.com. La siguiente ilustración muestra la GroupingInformation y ExternalEwsUrl [configuración de detección automática](how-to-get-user-settings-from-exchange-by-using-autodiscover.md) para los usuarios. 
  
**En la figura 1. Configuración de detección automática usada para los buzones de correo de grupo**

![Tabla que muestra los valores de GroupingInformation y ExternalEwsUrl para cada uno de los usuarios.](media/Exchange2013_NotificationAffinityAutoDResults.png)
  
Con la configuración de las respuestas de detección automática, los buzones de correo se agrupan por el valor concatenado de los valores de GroupingInformation y ExternalEwsUrl. En este ejemplo, Alfred y Sadie tienen los mismos valores, por lo que se encuentran en un grupo y Alisa y Ronnie comparten los mismos valores, por lo que están en otro grupo.
  
**La figura 2. Creación de grupos de buzón de correo**

![Tabla que muestra cómo se crean los grupos de buzones usando la configuración de Detección automática.](media/Exchange2013_NotificationAffinityGrouping.png)
  
A efectos de este ejemplo, nos centraremos en grupo A. Se debería usar los mismos pasos para el grupo B, pero se puede usar un valor distinto de X-AnchorMailbox para ese grupo.
  
Uso de [ApplicationImpersonation](http://technet.microsoft.com/en-us/library/dd776119%28v=exchg.150%29.aspx), crear la solicitud de suscripción para el buzón de correo de anclaje (alfred@contoso.com), con el encabezado X-AnchorMailbox establecido en el su dirección de correo electrónico y un valor de encabezado X-PreferServerAffinity de true. Configuración de estos valores de dos encabezado se activará el servidor para crear un BackEndOverrideCookie X para la respuesta.
  
Si se usa la API administrada de EWS, use el método[Add](http://msdn.microsoft.com/EN-US/library/cy7xta5e) de [cadena](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice_members%28v=exchg.80%29.aspx)para agregar los encabezados de dos a petición de suscripción, tal como se muestra. 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", Mailbox.SMTPAddress);
service.HttpHeaders.Add("X-PreferServerAffinity", "true");
```

Por lo tanto solicitudes de suscripción de Alfred tiene este aspecto.
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>alfred@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>
```

El siguiente mensaje XML es la respuesta a la solicitud de suscripción de Alfred, e incluye la X-BackEndOverrideCookie. Volver a enviar esta cookie para todas las solicitudes posteriores para los usuarios de este grupo. Tenga en cuenta que la respuesta contiene también las cookies adicionales, como la cookie de exchangecookie utilizada por Exchange 2010. Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013, omitir exchangecookie si se incluye en las solicitudes de suscripción subsiguientes.
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=ddb8c383aef34c7694132aa679744feb; expires=Thu, 25-Sep-2014 18:42:45 GMT; path=/;
    HttpOnly
Set-Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295; path=/; secure; HttpOnly
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
    expires=Wed, 25-Sep-2013 18:52:49 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

Uso el X-BackEndOverrideCookie de respuesta de Alfred y el encabezado X-AnchorMailbox, se crea la solicitud de suscripción para Sadie, el otro miembro de la solicitud de suscripción del grupo A. Sadie tiene este aspecto.
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@consoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@consoso.com </t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:Subscribe>
      <m:StreamingSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox" />
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
        </t:EventTypes>
      </m:StreamingSubscriptionRequest>
    </m:Subscribe>
  </soap:Body>
</soap:Envelope>

```

Respuesta de suscripción de Sadie tiene este aspecto. Tenga en cuenta que no incluye el X-BackEndOverrideCookie. El cliente es responsable de almacenamiento en caché que el valor de las solicitudes futuras.
  
```XML
HTTP/1.1 200 OK
Content-Type: text/xml; charset=utf-8
Set-Cookie: exchangecookie=640ea858f69d47ff8cce8b44c337f6d9; path=/
Set-Cookie: X-BackEndCookie=alfred@contoso.com=Ox8XKzcXLxg==; 
   expires= Wed, 25-Sep-2013 18:53:06 GMT; path=/EWS; secure; HttpOnly
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="775"
                         MinorBuildNumber="7"
                         Version="V2_4"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</m:SubscriptionId>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </m:SubscribeResponse>
  </s:Body>
</s:Envelope>
```

Con los valores de [SubscriptionId](http://msdn.microsoft.com/library/3f86c178-2311-4844-82db-c2a0e469d116%28Office.15%29.aspx) de las respuestas de suscripción, ha creado una solicitud de operación de [GetStreamingEvents](http://msdn.microsoft.com/library/dbe83857-c4f8-4d98-813f-e03c289697a1%28Office.15%29.aspx) para todas las suscripciones en el grupo. Debido a que hay menos de 200 suscripciones en este grupo, todos se envían en una sola solicitud. El encabezado X-PreferServerAffinity se establece en true y se incluye el X-BackEndOverrideCookie. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0516.014
X-AnchorMailbox: alfred@contoso.com
X-PreferServerAffinity: true
Host: outlook.office365.com
Cookie: X-BackEndOverrideCookie=CO1PR06MB222.namprd06.prod.outlook.com~1941996295
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
    <t:ExchangeImpersonation>
      <t:ConnectingSID>
        <t:SmtpAddress>sadie@contoso.com</t:SmtpAddress>
      </t:ConnectingSID>
    </t:ExchangeImpersonation>
  </soap:Header>
  <soap:Body>
    <m:GetStreamingEvents>
      <m:SubscriptionIds>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAB4EQOy2pfrQJfM3hzs/nZJIZssan6H0Ag=</t:SubscriptionId>
        <t:SubscriptionId>JgBjbzFwcjA2bWIyMjIubmFtcHJkMDYucHJvZC5vdXRsb29rLmNvbRAAAAAUeGk+7JFdSaFM8/NI/gQQpVdgZX6H0Ag=</t:SubscriptionId>
      </m:SubscriptionIds>
      <m:ConnectionTimeout>10</m:ConnectionTimeout>
    </m:GetStreamingEvents>
  </soap:Body>
</soap:Envelope>
```

Los eventos devueltos, a continuación, se pasan a un subproceso independiente para el procesamiento.
  
## <a name="how-has-affinity-changed"></a>¿Cómo ha cambiado la afinidad?
<a name="bk_howchanged"> </a>

En Exchange 2010, las suscripciones se mantienen en el servidor acceso de cliente, como se muestra en la figura 3. En las versiones de Exchange posterior a Exchange 2010, las suscripciones se mantienen en el servidor de buzón de correo, tal como se muestra en la figura 4.
  
**La figura 3. Proceso para el mantenimiento de la afinidad de Exchange 2010**

![Ilustración que muestra cómo se mantiene la tabla de suscripciones activas en el servidor de acceso de cliente en Exchange 2010.](media/Exchange2013_NoficationAffinity2010.png)
  
**La figura 4. Proceso para el mantenimiento de afinidad en Exchange Online y Exchange 2013**

![Ilustración que muestra cómo el equilibrador de carga y el servidor de acceso de cliente enrutan las solicitudes al servidor de buzones que mantiene la tabla de suscripciones activas en Exchange Server y Exchange Online.](media/Exchange2013_NoficationAffinity2013.png)
  
En Exchange 2010, el cliente sólo sabe la dirección del equilibrador de carga y el exchangecookie que es devuelto por el servidor se asegura de que la solicitud se enruta al servidor de acceso de cliente correcto. Sin embargo, en versiones posteriores, el equilibrador de carga y las funciones de servidor acceso de cliente tienen que enrutar las solicitudes de forma adecuada antes de que se incluyen en el servidor de buzones. Para llevar a cabo, que se necesita información adicional, que es la razón por la que se introdujeron las cookies y los nuevos encabezados. El artículo de [suscripciones de notificación, eventos de buzón de correo y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md) explica cómo se mantienen las suscripciones en Exchange 2013. 
  
Es posible que tenga en cuenta que el exchangecookie que usa Exchange 2010 sigue siendo devuelto por versiones posteriores. No hay ningún riesgo en incluidos esta cookie en las solicitudes, pero las versiones posteriores de Exchange pasar por alto.
  
## <a name="see-also"></a>Ver también

- [Suscripciones de notificación de eventos de buzón de correo y EWS en Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
- [Notificaciones de secuencia acerca de los eventos de buzón de correo mediante el uso de EWS en Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Notificaciones sobre eventos de buzón de correo de extracción mediante el uso de EWS en Exchange](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
- [Tratamiento de errores relacionados con la notificación en EWS en Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
- [Cambios en la administración de afinidad para las suscripciones de EWS...](http://blogs.msdn.com/b/mstehle/archive/2013/04/17/changes-in-managing-affinity-for-ews-subscriptions.aspx)
- [EWS limitación en Exchange](ews-throttling-in-exchange.md)
    

