---
title: Limitación de EWS en Exchange
manager: sethgros
ms.date: 05/10/2019
ms.audience: Developer
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: Obtenga información sobre las directivas de limitación que afectan a EWS cuando se usa Exchange.
localization_priority: Priority
ms.openlocfilehash: 27db12c01180abbaf92b5b9a09a072212b6012ec
ms.sourcegitcommit: eeda51cb037aa25566adb293f25574674fdb2d9e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2020
ms.locfileid: "45012555"
---
# <a name="ews-throttling-in-exchange"></a>Limitación de EWS en Exchange

Obtenga información sobre las directivas de limitación que afectan a EWS cuando se usa Exchange.

**Proporcionado por:** Escalas de Glen; Michael Mainer, Microsoft Corporation

En este artículo se proporciona información sobre la limitación de EWS en Exchange Online, Exchange online como parte de Office 365 y las versiones locales de Exchange a partir de Exchange 2010. La limitación en Exchange ayuda a garantizar la confiabilidad y el tiempo de actividad del servidor limitando la cantidad de recursos de servidor que un solo usuario o aplicación puede consumir. La limitación es una respuesta reactiva al uso excesivo de los recursos del sistema que pueden afectar a la confiabilidad y la funcionalidad del servicio. Exchange supervisa constantemente el estado de los recursos de infraestructura críticos, como las bases de datos de buzones de correo. Cuando se detectan factores de carga elevados que degradan el rendimiento de estos recursos, las conexiones de EWS se limitan proporcionalmente en función de la cantidad que cada autor de llamada contribuye a la condición de carga alta. El resultado es que un usuario puede encontrarse dentro del límite de limitación y seguir experimentando la ralentización hasta que el estado del recurso vuelve a los niveles operativos.

Cada protocolo de acceso de cliente de Exchange, incluido EWS, tiene una directiva de limitación. Al diseñar aplicaciones que usan EWS, es importante tener en cuenta las directivas de limitación, para ayudar a garantizar la confiabilidad de la aplicación y el estado de su servidor de Exchange. En este artículo se identifican las diferentes directivas de limitación y límites de servicio para EWS, tanto si se destina a Exchange online como a versiones de Exchange locales a partir de Exchange Server 2010. Según corresponda, este artículo también identifica las diferencias en las directivas de limitación en las diferentes versiones de Exchange.

> [!IMPORTANT]
> La Directiva de limitación predeterminada, el acceso a la Directiva de limitación y la configuración de la Directiva de limitación difiere entre Exchange Online y Exchange local. Los valores de configuración de limitación específicos solo son precisos para una versión específica de Exchange. Debido a que la configuración de valores varía entre versiones y los administradores de Exchange pueden cambiar las directivas de limitación predeterminadas para implementaciones locales, este artículo no proporciona los valores de configuración predeterminados. Es más importante tener en cuenta las consideraciones que hay que tener en cuenta al diseñar una aplicación que funcione dentro de límites de limitación y que reaccione adecuadamente a los escenarios de limitación.

Si es desarrollador de aplicaciones, tiene que factorizar la limitación en el diseño de la aplicación. Las diferentes versiones de Exchange tienen valores predeterminados diferentes para los parámetros de limitación de EWS. Las aplicaciones de servicio y cliente diseñadas para tener acceso a diferentes versiones de Exchange deberán tener en cuenta esta configuración, si son valores predeterminados, valores personalizados definidos por un administrador de Exchange o, como en Exchange Online, establecidos de forma predeterminada y no se pueden detectar. Dado que los valores de los parámetros de limitación no se pueden descubrir mediante programación, las especificaciones de diseño de clientes deben incluir un plan para que la aplicación se adapte a límites de limitación potenciales diferentes. Al diseñar aplicaciones multiproceso que tengan acceso a un gran número de buzones de correo o cuando muchos clientes obtengan acceso al mismo buzón, tenga en cuenta los límites de simultaneidad que la directiva predeterminada aplica a Exchange.

## <a name="throttling-policies-that-affect-ews"></a>Directivas de limitación que afectan a EWS

Las directivas de limitación de Exchange no afectan solo EWS, sino también todas las conexiones de cliente al servidor Exchange, incluidos los protocolos usados por Office Outlook, Outlook Web App y Exchange ActiveSync.

La Directiva de limitación de **CPUStartPercent** puede afectar al rendimiento de EWS al ejecutar Exchange 2010. Cuando el uso medio de CPU de los procesos de Exchange que se ejecutan en el servidor de acceso de cliente (incluido, entre otros, el proceso de EWS) supera el valor especificado por esta Directiva, las solicitudes de entrada se retrasarán para reducir el uso de la CPU. No puede cambiar el valor de esta Directiva, pero saber sobre ella puede ayudarle a solucionar problemas de rendimiento. La lógica de muestreo que el servidor de acceso de cliente realiza para este valor es un promedio de una ventana graduada de 10 segundos. Esto permite que el proceso responda adecuadamente a los picos rápidos de uso de la CPU. Cuando se supera este umbral, se retrasan las conexiones entrantes a EWS. Este retraso se limita a 500 milisegundos (mseg) a un uso teórico de la CPU 100% por cada solicitud de EWS. Si se pasa una solicitud EWS de lote para obtener 100 elementos, el servidor comprobará el uso de CPU 100 veces (una vez por elemento) durante un retraso máximo de 50 segundos. El tiempo de retraso es linealmente proporcional al uso de la CPU. En **CPUStartPercent**, el retraso es 0 (un rendimiento del subproceso) y aumenta linealmente hasta 500 ms en el 100% de uso de CPU. Como las directivas de limitación se aplican a todos los usuarios de Exchange, es improbable que el uso de la CPU supere el límite de **CPUStartPercent** en un servidor de acceso de cliente de Exchange, ya que los usuarios individuales o las aplicaciones no pueden obtener suficiente uso de CPU para afectar al funcionamiento del servidor.

En la siguiente tabla se enumeran los parámetros de la Directiva de limitación que afectan a las aplicaciones que usan EWS.

**Tabla 1: parámetros de la Directiva de limitación que afectan a EWS**

|**Nombre del parámetro de la Directiva de limitación**|**Se aplica a**|**Descripción**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de conexiones de búsqueda de detección simultáneas que un usuario puede realizar a la vez.  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de palabras clave que un usuario puede incluir en una búsqueda de detección.  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de palabras clave para las que se deben mostrar estadísticas.  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de buzones de origen que un usuario puede incluir en una búsqueda de detección.  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de buzones que puede buscar en una búsqueda de exhibición de documentos electrónicos local sin que sea posible ver las estadísticas.  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de mensajes devueltos en una respuesta de vista previa de búsqueda de exhibición de documentos electrónicos.  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define los límites de consumo de recursos para el usuario de EWS antes de bloquearlo completamente a fin de realizar operaciones en un componente específico.  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define la cantidad de tiempo que un usuario de EWS puede consumir una cantidad elevada de recursos antes de limitarse. Este valor se mide en milisegundos. y se establece por separado para cada componente.  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define la velocidad con la que se vuelve a cargar el presupuesto de un usuario de EWS (el presupuesto aumenta) durante el tiempo de duración del presupuesto.  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número máximo de suscripciones de notificación de inserción, extracción y transmisión activas que un usuario puede tener en un servidor de acceso de cliente específico al mismo tiempo. Esta se ha presupuestado de forma diferente para diferentes versiones de Exchange.  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |Define la cantidad de tiempo en segundos que las búsquedas rápidas realizadas mediante la búsqueda de Exchange en EWS continúan antes de que se agote el tiempo de espera. Las búsquedas rápidas son búsquedas realizadas mediante una cadena de consulta de sintaxis de consulta avanzada (AQS) en una [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).  <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número máximo de elementos desde una operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) o [FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) que puede haber en la memoria del servidor de acceso de cliente al mismo tiempo para un usuario. El valor predeterminado de esta propiedad es 1000. El [valor de retroceso](https://technet.microsoft.com/library/dd297964%28v=exchg.141%29.aspx#fallback)para este valor es 1000.  <br/> En Exchange Online y versiones locales de Exchange a partir de Exchange 2013, un cmdlet no puede consultar ni configurar esta directiva de limitación. En Exchange Online y versiones locales de Exchange a partir de Exchange 2013, la EWSFindCountLimit para la [búsqueda de AQS](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) y cualquier búsqueda de Exchange con una restricción es de 250 resultados. Una búsqueda de Exchange sin una restricción devolverá hasta 1000 resultados.  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar solicitudes de Active Directory.  <br/> |
|**EWSPercentTimeInCAS** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar el código del servidor de acceso de cliente.  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar solicitudes RPC de buzón de correo.  <br/> |
|**EWSMaxConcurrency** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número de conexiones abiertas simultáneas que un usuario específico puede tener en un servidor de Exchange que usa EWS al mismo tiempo. El valor predeterminado de Exchange 2010 es 10. El valor predeterminado de Exchange 2013 y Exchange Online es 27.  <br/> Esta Directiva se aplica a todas las operaciones excepto para las notificaciones de streaming. Las notificaciones de streaming usan el **HangingConnectionLimit** para indicar el número de conexiones de eventos de transmisión de apertura que están disponibles. Para obtener más información, vea [¿qué valores de limitación se deben tener en cuenta?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número de mensajes por minuto que se puede enviar.  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el límite para el número de destinatarios que un usuario puede direccionar en un período de 24 horas.  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el límite para el número de destinatarios de las acciones de redirección y redireccionamiento de la bandeja de entrada en un período de 24 horas.  <br/> |
|**ConcurrentSyncCalls** <br/> |Exchange 2019  <br/> Exchange 2016  <br/> Exchange Online  <br/> |Define el límite para el número de llamadas de sincronización simultáneas (SyncFolderHierarchy, SyncFolderItems) para un usuario. <br/> |

> [!CAUTION]
> No establezca las directivas de limitación en **null**. Esto establecerá que la Directiva sea igual a ilimitada, lo que indica que no se ha establecido una directiva de limitación.

## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>Visualización de las directivas que se aplican a los buzones de Exchange

Exchange local proporciona los cmdlets del shell de administración de Exchange que puede usar para establecer y obtener la Directiva de limitación. Exchange online no proporciona acceso a los cmdlets de la Directiva de limitación.

Puede usar los siguientes cmdlets para mostrar las directivas de limitación de peticiones para una implementación local de Exchange Server:

- **Get-ThrottlingPolicy** : obtiene la configuración de limitación de clientes para una o más directivas de limitación. Para obtener más información, vea [Get-ThrottlingPolicy](https://technet.microsoft.com/library/dd351264.aspx) en TechNet.

- **Get-ThrottlingPolicyAssociation** : permite ver la relación entre un objeto y sus directivas de limitación asociadas. El objeto puede ser un usuario con un buzón, un usuario sin buzón o un contacto. Para obtener más información, vea [Get-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459241.aspx) en TechNet.

Use el siguiente comando para mostrar la Directiva de limitación predeterminada para Exchange 2010.

**Get-ThrottlingPolicy | Where-Object {$ _. IsDefault-EQ "true"} | Format-List**

Use el siguiente comando para mostrar la Directiva de limitación global (que equivale a la Directiva de limitación predeterminada en Exchange 2010) en Exchange 2013.

**Get-ThrottlingPolicy | Where-Object {$ _. ThrottlingPolicyScope-EQ "global"} | Format-List**

Use el siguiente comando para mostrar la Directiva de limitación de peticiones asociada a un usuario en Exchange 2010 o Exchange 2013. Reemplace el nombre de usuario john@contoso.com por el nombre de usuario del usuario de destino para el que desea obtener información sobre la Directiva de limitación.

**Get-ThrottlingPolicyAssociation john@contoso.com | Format-List**

Al ejecutar este comando en el shell de administración de Exchange, se obtiene una salida similar a la siguiente.

```powershell
PS C:\>Get-ThrottlingPolicyAssociation john@contoso.com
RunspaceId               : 72153d6-9dce-2fae-8dbd-5ca5f760g2df
ObjectId                 : john
ThrottlingPolicyId       :
Name                     : john
Identity                 : FHXB-28178dom.contoso.com/Users/john
IsValid                  : True
NeedsToSuppressPii       : False
ExchangeVersion          : 0.10 (15.0.0.0)
DistinguishedName        : CN=john,CN=Users,DC=FHXB-28178dom,DC=contoso,DC=com
Guid                     : 2c10dab6-de28-1937-ad8g-535832613a08
```

> [!NOTE]
> Cuando la propiedad **ThrottlingPolicyId** está en blanco, se aplica la directiva predeterminada al buzón.

Puede establecer la Directiva de limitación en un servidor de Exchange mediante los cmdlets [set-ThrottlingPolicy](https://technet.microsoft.com/library/dd298094.aspx) y [set-ThrottlingPolicyAssociation](https://technet.microsoft.com/library/ff459231.aspx) . Puede crear y quitar directivas de limitación no predeterminadas con los cmdlets [New-ThrottlingPolicy](https://technet.microsoft.com/library/dd351045.aspx) y [Remove-ThrottlingPolicy](https://technet.microsoft.com/library/dd351178.aspx) .

> [!TIP]
> Le recomendamos que diseñe sus aplicaciones para que cumplan la Directiva de limitación de peticiones predeterminada. Solo realice cambios en las directivas de limitación predeterminadas si el diseño de la aplicación cliente no puede acomodar la directiva predeterminada. Tenga en cuenta que las directivas de limitación menos restrictivas pueden afectar negativamente la confiabilidad del servicio.

## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>Consideraciones de limitación para las aplicaciones que usan la suplantación de EWS

La [suplantación](impersonation-and-ews-in-exchange.md) es un método de autorización que permite que una única cuenta tenga acceso a muchas cuentas. Cuando una cuenta de servicio suplanta a los usuarios, actúa como los usuarios y, por lo tanto, asume los derechos asignados a dichos usuarios. Los archivos de registro registran el acceso como usuario suplantado. Los administradores usan el control de acceso basado en roles (RBAC) para configurar la suplantación a través del shell de administración de Exchange.

Cuando se usa la suplantación, los presupuestos de todos los umbrales de limitación se aplican de forma diferente en función de la versión de Exchange. El presupuesto se calcula en función de la cuenta que se suplanta, o bien de la cuenta de servicio. Si la aplicación es multiproceso y realiza solicitudes simultáneas en varios buzones, debe tener en cuenta cómo el umbral de limitación afectará al rendimiento de la aplicación. En general, tenga en cuenta los siguientes límites en las cuentas de servicio al crear una aplicación basada en servicios que use la suplantación para obtener acceso a todos los buzones de correo:

- Cuando se usa la suplantación, la cuenta de servicio tiene un presupuesto independiente para los siguientes parámetros de directiva:

  - **EWSMaxConcurrency**

  - **EWSPercentTimeInAD**

  - **EWSPercentTimeInCAS**

  - **EWSPercentTimeInMailboxRPC**

  - **EWSMaxSubscriptions**

  - **EWSFastSearchTimeoutInSeconds**

  - **EWSFindCountLimit**

- El presupuesto de **EWSMaxConcurrency** se comparte para la cuenta de servicio y la cuenta que se suplanta para todas las conexiones a las versiones de Exchange anteriores a Exchange 2010 Service Pack 2 (SP2) paquete acumulativo de actualizaciones 4 (RU4). A partir de Exchange 2010 SP2 RU4 e incluir Exchange Online, el acceso a la cuenta de servicio usa un presupuesto independiente del presupuesto de **EWSMaxConcurrency** de usuario. Para obtener más información acerca de la actualización de la Directiva de limitación de conexiones simultáneas de Exchange para EWS, consulte [Descripción del paquete acumulativo de actualizaciones 4 para Exchange Server 2010 Service Pack 2](https://support.microsoft.com/kb/2706690).

    Las notificaciones de streaming de EWS en versiones de Exchange a partir de Exchange 2010 e incluyen Exchange Online, tienen un presupuesto **EWSMaxConcurrency** clonado adicional desde el resto de conexiones de cliente de EWS. Las conexiones de notificación de transmisión por secuencias se cuentan con un presupuesto independiente que todas las demás operaciones de EWS. El presupuesto de simultaneidad máximo de la notificación de transmisión por secuencias es, en realidad, dos presupuestos distintos: un presupuesto es para todas las cuentas de servicio y un presupuesto para la cuenta que se va a suplantar. Las notificaciones de streaming en Exchange Online y las versiones de Exchange a partir de Exchange 2013 usan [HangingConnectionLimit](#throttling-considerations-for-ews-notification-applications) para limitar el número de conexiones.

    Por ejemplo, supongamos que **EWSMaxConcurrency** es igual a cinco. Un usuario puede tener cinco conexiones de notificación de extracción abiertas, mientras que una cuenta de servicio puede tener cinco conexiones de notificación de extracción simultáneas en el buzón del usuario al mismo tiempo que el usuario.

- En la siguiente tabla se identifica cómo se calculan los presupuestos de limitación de **EWSMaxSubscriptions** entre la cuenta de servicio y la cuenta que se va a suplantar.

   **Tabla 2: contabilidad del presupuesto de EWSMaxSubscriptions**

   |**Versión de Exchange**|**EWSMaxSubscriptions la Contabilidad presupuestaria del límite**|
   |:-----|:-----|
   |Exchange Online  <br/> |Se carga en el buzón de correo de destino.  <br/> |
   |Exchange 2013  <br/> |Se carga en el buzón de correo de destino.  <br/> |
   |Exchange 2010 SP3  <br/> |Se carga en el buzón de correo de destino.  <br/> |
   |Exchange 2010 SP2  <br/> |Se cargan en la cuenta de llamada. A partir de Exchange 2010 SP2 RU4, el presupuesto se carga en el buzón de correo de destino.  <br/> |
   |Exchange 2010 SP1  <br/> |Se cargan en la cuenta de llamada.  <br/> |
   |Exchange 2010  <br/> |Se cargan en la cuenta de llamada.  <br/> |

- Debido a que el presupuesto de limitación de **EWSMaxSubscriptions** se carga en la cuenta que se suplanta, no hay ningún límite en el número de buzones a los que puede suscribir y recibir notificaciones de transmisión por secuencias una cuenta de servicio, siempre que se use la suplantación. Para la cuenta que se va a suplantar, no puede tener más de _n_ solicitudes simultáneas por buzón de correo de destino, donde _n_ es el valor de **EWSMaxSubscriptions** . Si no estaba usando la suplantación, la misma cuenta de servicio no podría tener más de _n_ total de solicitudes simultáneas. Por lo tanto, la ventaja es que, al usar la suplantación en una cuenta de servicio, se aumenta exponencialmente el número de buzones a los que se puede atender. Para obtener más información, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).

- Los parámetros de directiva **EWSPercentTimeInMailboxRPC**, **EWSPercentTimeInCAS**y **EWSPercentTimeInAD** hacen referencia a acciones realizadas por un único hilo. Cuando una aplicación realiza varias operaciones simultáneas, debe tener en cuenta el efecto acumulado de estas operaciones en el presupuesto de recursos de usuario.

## <a name="throttling-implications-for-ews-batch-requests"></a>Implicaciones de limitación de solicitudes por lotes de EWS

EWS permite procesar en lote varias solicitudes de elementos en una única solicitud ejecutada por el servidor de acceso de cliente. Esto permite una mayor eficiencia y rendimiento. Cuando un servidor de Exchange ejecuta una solicitud por lotes, comprueba el presupuesto del usuario tras la ejecución de cada elemento del lote. Si la aplicación está por encima del presupuesto, el procesamiento del siguiente elemento del lote se retrasa hasta que el presupuesto de ese usuario se haya recargado. Para asegurarse de que las aplicaciones que usan operaciones por lotes se ejecutan correctamente, limite el número de solicitudes de elementos que se pueden incluir en un solo lote y divida los lotes grandes en varios lotes más pequeños para aumentar la confiabilidad de los resultados. El efecto que tiene una operación por lotes en umbrales de limitación específicos depende del tipo de solicitud, el tamaño de los elementos que se van a procesar (por ejemplo, en las operaciones **UploadItems** o **ExportItems** ) y el contenido del buzón. Las directivas de limitación afectan a las operaciones por lotes haciendo que la solicitud tarde más tiempo en procesarse. Por lo tanto, el autor de la llamada tendrá que esperar más tiempo para la respuesta y, debido a que EWS limita el tiempo de ejecución de una solicitud por lotes a un minuto, la llamada podría agotar el tiempo de espera.

Para determinar el tamaño de lote óptimo para una aplicación, realice pruebas unitarias con varios conjuntos de entrada para asegurarse de que la aplicación no encuentra ningún error en un entorno de producción.

## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>Parámetros de directivas de limitación que afectan a las operaciones de búsqueda de EWS

[Las operaciones de búsqueda en EWS](search-and-ews-in-exchange.md) pueden requerir grandes cantidades de tiempo y recursos, según el modo en que se ejecuta la búsqueda y la información que se solicita. Para controlar el uso de recursos durante las búsquedas, se aplican dos parámetros de directiva: **EWSFastSearchTimeoutInSeconds** y **EWSFindCountLimit**.

El parámetro de directiva **EWSFastSearchTimeoutInSeconds** especifica la cantidad de tiempo, en segundos, que se ejecutan las búsquedas rápidas de EWS (también conocido como búsqueda de indización de contenido) antes de que se agote el tiempo de espera. Una búsqueda rápida es una búsqueda realizada mediante una cadena de consulta de sintaxis de consulta avanzada (AQS) en una [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).

Puede buscar en una carpeta de buzón de Exchange de dos maneras:

- Mediante una búsqueda de almacén de Exchange, que realiza un análisis secuencial de todos los mensajes en el ámbito de la búsqueda de destino.

- Mediante el servicio de búsqueda de Exchange (indización de contenido).

Estos dos tipos de búsquedas pueden tener como resultado tiempos de espera. Cuando sea posible, use el servicio de búsqueda de Exchange, ya que estas búsquedas se destinan a índices de buzón y usan consultas AQS. En el siguiente ejemplo, se muestra cómo realizar una búsqueda AQS de la bandeja de entrada mediante EWS y el servicio de búsqueda de Exchange.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

Si no puedes usar una búsqueda AQS, evita el uso de filtros de búsqueda demasiado complejos. Intente evitar también la creación de filtros de búsqueda basados en valores calculados si la consulta incluye propiedades MAPI extendidas. La búsqueda de AQS se introdujo en Exchange 2010.

> [!NOTE]
> La primera vez que se ejecuta una consulta de búsqueda compleja del almacén de Exchange, se ejecuta muy despacio y puede agotar el tiempo de espera. A continuación, la consulta responderá con mayor rapidez. Para obtener más información acerca de los procesos de back-end de Exchange Server que se producen durante las consultas de búsqueda del almacén de Exchange, vea [Understanding the performance Impact of High Item Counts and Restricted views](https://technet.microsoft.com/library/cc535025%28EXCHG.80%29.aspx) on technet. El uso de un **SearchFilter** crea una restricción dinámica que ayuda a realizar consultas similares en el futuro, pero debido a que estas restricciones son de naturaleza dinámica, no son permanentes ni confiables y se eliminan después de un máximo de tres días.

El parámetro de directiva **EWSFindCountLimit** especifica el número máximo de elementos a partir de los resultados de una operación **FindItem** o **FindFolder** que puede existir en la memoria de un servidor de acceso de cliente al mismo tiempo para un usuario. Cada elemento o carpeta que procesa EWS en una solicitud **FindItem** o **FindFolder** se cuenta con el presupuesto especificado en el elemento **EWSFindCountLimit** . Cuando la respuesta se envía de vuelta al solicitante, se suelta la carga del recuento de búsqueda de la llamada actual. La respuesta que devuelve el servidor a un solicitante cuando se excede el presupuesto se basa en el valor del elemento **RequestServerVersion** y si el solicitante especificó la paginación. Cuando el valor del elemento **RequestServerVersion** indica Exchange 2010 o una versión anterior de Exchange, el servidor envía una respuesta de error con el código de error **ErrorServerBusy**. Si el valor del elemento **RequestServerVersion** indica una versión de Exchange que empieza con Exchange 2010 SP1 o Exchange Online, y el cliente usa la paginación, EWS puede devolver un conjunto de resultados parciales en lugar de un error. La aplicación debe esperar que EWS no puede devolver todos los elementos. Si el valor del elemento **IncludesLastItemInRange** es false, la aplicación debe realizar otra solicitud **FindItem** o **FindFolder** con el nuevo desplazamiento y continuar hasta que el elemento **IncludesLastItemInRange** devuelva true.

Cuando se usa una operación **FindItem** o **FindFolder** , es importante usar la paginación. La API administrada de EWS fuerza el uso de la paginación, pero si usa otros métodos, como objetos proxy de EWS o SOAP sin procesar, debe establecer la paginación explícitamente. En el ejemplo siguiente se muestra cómo usar la paginación en la API administrada de EWS.

```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> La directiva predeterminada de Exchange limita el tamaño de página a 1000 elementos. Establecer el tamaño de página en un valor mayor que este número no tiene ningún efecto práctico.

Las aplicaciones también deben tener en cuenta el hecho de que el valor del parámetro de limitación _EWSFindCountLimit_ puede dar como resultado la devolución de un conjunto de resultados parcial para las aplicaciones que realizan solicitudes simultáneas. En el siguiente ejemplo se muestra cómo usar la propiedad **MoreAvailable** en la API administrada de EWS para asegurarse de que todos los resultados se incluyen en una consulta.

```cs
ItemView iv = new ItemView(1000);
service.TraceEnabled = false;
FindItemsResults<Item> fiResults = null;
Do
{
    fiResults = service.FindItems(WellKnownFolderName.Inbox, iv);
    PropertySet itItemPropSet = new PropertySet(BasePropertySet.IdOnly) { EmailMessageSchema.Body };
    //Process Items in Result Set
    iv.Offset += fiResults.Items.Count;
}
while (fiResults.MoreAvailable == true);
```

## <a name="throttling-policies-and-concurrency"></a>Directivas de limitación de peticiones y concurrencia

La concurrencia hace referencia al número de conexiones de un usuario específico. Una conexión se mantiene desde el momento en que se recibe una solicitud hasta que se envía una respuesta al solicitante. Si los usuarios intentan efectuar más solicitudes simultáneas de las que permite su directiva, el nuevo intento de conexión dará error. Sin embargo, las conexiones existentes siguen siendo válidas. Las directivas de limitación pueden afectar a la simultaneidad de varias formas.

El parámetro de la Directiva de limitación **EWSMaxConcurrency** establece el número de conexiones simultáneas que un usuario específico puede tener en un servidor de Exchange al mismo tiempo. Para determinar el número máximo de conexiones simultáneas que se permiten, tenga en cuenta las conexiones que usarán los clientes de Outlook. Outlook 2007 y Outlook 2010 usan EWS para tener acceso a la información de disponibilidad y fuera de la oficina (OOF). Mac Outlook 2011 usa EWS para todas las funciones de acceso de cliente. Según el número de clientes de Outlook que se conectan de forma activa al buzón de un usuario, el número de conexiones simultáneas disponibles para un usuario puede ser limitado. Además, si la aplicación tiene que conectarse a varios buzones de forma simultánea mientras usa un solo contexto de seguridad, es importante tener en cuenta el valor de la directiva **EWSMaxConcurrency** . Para obtener más información sobre el uso de un solo contexto de seguridad con conexiones simultáneas, vea [consideraciones sobre limitación de aplicaciones que usan la suplantación de EWS](#throttling-considerations-for-applications-that-use-ews-impersonation) anteriormente en este artículo.

Las aplicaciones que se conectan a la vez a varios buzones de correo tienen que poder realizar un seguimiento del uso de recursos en el lado cliente. Como las operaciones de EWS se basan en solicitudes/respuestas, puede asegurarse de que funcionan correctamente en el umbral de **EWSMaxConcurrency** mediante el seguimiento del número de conexiones que se producen entre el inicio de una solicitud y el momento en que se recibe la respuesta, y que garantiza que no se produzcan más de diez solicitudes abiertas al mismo tiempo.

El parámetro de directiva **EWSFindCountLimit** especifica el tamaño máximo de resultado que puede usar una operación **FindItem** o **FindFolder** en un servidor de acceso de cliente al mismo tiempo para un usuario. Si una aplicación (o posiblemente varias aplicaciones) realiza dos solicitudes **FindItem** de EWS simultáneas que devuelven 100 elementos para un usuario específico, la carga de la **EWSFindCountLimit** con el presupuesto del usuario específico será 200. Cuando se devuelve la primera solicitud, el presupuesto desciende a 100 y, cuando se devuelve la segunda solicitud, el presupuesto disminuye a cero. Si la misma aplicación realizara dos solicitudes simultáneas de 1000 elementos, el valor de presupuesto sería 2000 elementos, lo que supera el valor de **EWSFindCountLimit** . Si el presupuesto del usuario para los elementos desciende por debajo de cero, la siguiente solicitud genera un error hasta que el presupuesto del usuario recarga a uno o más.

## <a name="throttling-considerations-for-ews-notification-applications"></a>Consideraciones sobre la limitación de solicitudes de notificaciones de EWS

Si va a compilar aplicaciones de notificación de EWS que usan las notificaciones de inserción, extracción o transmisión por secuencias, debe tener en cuenta las implicaciones de las directivas de limitación de peticiones de **EWSMaxSubscriptions** y **EWSMaxConcurrency** , y el **HangingConnectionLimit**.

El parámetro de directiva **EWSMaxSubscriptions** especifica el número máximo de suscripciones de inserción, extracción y transmisión activas que un usuario puede tener en un servidor de acceso de cliente específico al mismo tiempo. Las diferentes versiones de Exchange tienen valores predeterminados diferentes para este parámetro. Un usuario puede suscribirse a todas las carpetas de un buzón mediante la propiedad **SubscribeToAllFolders** , que usa una única suscripción contra el presupuesto **EWSMaxSubscriptions** . Los usuarios pueden suscribirse a carpetas individuales, con cada suscripción de carpeta contando hacia el presupuesto de **EWSMaxSubscriptions** , hasta el límite establecido por el valor del parámetro **EWSMaxSubscriptions** (por ejemplo, los usuarios pueden suscribirse a 20 carpetas de calendario en buzones diferentes si **EWSMaxSubscriptions** se establece en 20).

Para obtener información sobre la suplantación y el parámetro **EWSMaxSubscriptions** , vea [consideraciones sobre limitación de aplicaciones que usan la suplantación de EWS](#throttling-considerations-for-applications-that-use-ews-impersonation) anteriormente en este artículo.

El parámetro de directiva **EWSMaxConcurrency** también puede ser un problema de las notificaciones de EWS; por ejemplo:

- Cuando EWS incrementa el número de conexiones para el propietario de la suscripción mientras la notificación se genera mediante una suscripción de inserción.

- Cuando una aplicación está diseñada para escuchar buzones de varios usuarios y los usuarios reciben notificaciones simultáneas para una instancia de un mensaje que se envía a una lista de distribución.

Si la aplicación de notificaciones es multiproceso y realiza solicitudes de conexión simultáneas para obtener más información acerca de un mensaje en particular recibido por una cuenta de usuario, se puede superar el límite de directivas de **EWSMaxConcurrency** . Para tener esto en cuenta, considere la posibilidad de supervisar las conexiones simultáneas en la aplicación, incluidas las que puede usar el servidor y la implementación de la cola de solicitudes en el cliente.

**HangingConnectionLimit** solo se aplica a las notificaciones de transmisión por secuencias. Este límite se establece en el archivo de web.config, lo que significa que un administrador de Exchange puede establecer este valor en un servidor de Exchange local, pero los buzones de correo de Exchange Online deben usar el valor predeterminado para este límite, que es 10 para Exchange Online, Exchange 2019, Exchange 2016 y 3 para Exchange 2013. Para obtener más información, vea [¿qué valores de limitación se deben tener en cuenta?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).

## <a name="throttling-policy-and-application-performance"></a>Rendimiento de la aplicación y la Directiva de limitación

Los tres parámetros siguientes de la Directiva de limitación **PercentTimeIn** afectan a la cantidad de tiempo que puede consumir una aplicación EWS en un servidor de acceso de cliente:

- **EWSPercentTimeInAD**

- **EWSPercentTimeInCAS**

- **EWSPercentTimeInMailboxRPC**

Los valores especificados en los parámetros de directiva **PercentTimeIn** indican la cantidad de tiempo que se asigna un subproceso que realiza una solicitud. Por ejemplo, suponiendo un valor de **EWSPercentTimeInCAS** de 90, si un proceso realiza dos solicitudes simultáneas que pasan 54 segundos cada ejecución de código en el servidor de acceso de cliente, el proceso usa 108 segundos en una ventana de 60. Esto representa un valor de parámetro **EWSPercentTimeInCAS** de 180 por ciento.

> [!NOTE]
> El valor del parámetro **EWSPercentTimeInCAS** es un supraconjunto superpuestos de los valores de los parámetros **EWSPercentTimeInAD** y **EWSPercentTimeInMailboxRPC** . Esto significa que el gasto en el tiempo de procesamiento del servidor de acceso de clientes será siempre mayor que los gastos en **EWSPercentTimeInAD** y **EWSPercentTimeInMailboxRPC**. Esto se debe a que para que el componente de Exchange realice una llamada de Active Directory o RPC, ya debe estar ejecutando el código del servidor de acceso de cliente. Además, los gastos en el tiempo de procesamiento de **EWSPercentTimeInCAS** no se detienen mientras se realizan llamadas LDAP o RPC. Aunque la solicitud podría esperar de forma sincrónica una respuesta de servicios de dominio de Active Directory (AD DS) o del almacén de Exchange, el proceso todavía está consumiendo un subproceso en el servidor y, por lo tanto, el subproceso debe seguir cobrando por ese uso.

La cantidad de tiempo de CPU que puede tardar una aplicación en un período de 60-segundo puede superar estos límites de limitación; por lo tanto, es importante tener en cuenta el volumen y el tipo de solicitudes que se realizan. Por ejemplo, un lote grande de operaciones de **ResolveNames** que se realizan simultáneamente puede exceder el valor del parámetro de directiva **EWSPercentTimeInAD** . Los valores de directiva contenidos en la Directiva de limitación predeterminada están diseñados para permitir que la mayoría de las aplicaciones de EWS funcionen sin problemas; sin embargo, cuando las aplicaciones multiprocesos de alto volumen colocan un gran volumen de solicitudes en un servidor de acceso de cliente en particular, esto puede crear problemas. Para evitarlo, considere limitar el tamaño de los lotes que se van a ejecutar en el servidor.

## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>Limitación de las directivas y aplicaciones que envían un gran volumen de correo electrónico

Las directivas de limitación predeterminadas incluyen tres parámetros de directiva de límite de velocidad que pueden afectar a las aplicaciones que usan EWS para enviar un gran volumen de mensajes o enviar mensajes en lotes grandes en un breve período de tiempo.

> [!NOTE]
> En general, se recomienda no usar EWS para enviar correo electrónico masivo. Use un host SMTP especializado en servicios de correo masivo para enviar mensajes de correo electrónico masivos de gran tamaño.

El parámetro de directiva **MessageRateLimit** especifica el número de mensajes por minuto que puede enviar cualquier cliente de Exchange, incluido EWS. De forma predeterminada, esta directiva está configurada en 30 mensajes por minuto. Para los usuarios normales, suele ser suficiente. Sin embargo, las aplicaciones que envían lotes de mensajes de correo electrónico de gran tamaño, por ejemplo, como parte de un programa de facturación, pueden tener problemas. Cuando se supera el límite de esta Directiva, se retrasa la entrega de mensajes para el buzón. En concreto, los mensajes aparecerán en la carpeta Bandeja de salida o borradores durante períodos de tiempo más prolongados en los que un usuario o aplicación envía un número de mensajes mayor que el valor especificado por el parámetro **MessageRateLimit** . No olvide tener esto en cuenta al desarrollar un sistema de seguimiento de entregas, especialmente si la aplicación usa un buzón al que los usuarios se conectan a través de Outlook. Cuando los elementos aplazados se almacenan en la carpeta Bandeja de salida o borradores, los usuarios pueden interpretarlo como un error.

El parámetro de directiva **RecipientRateLimit** especifica el límite en el número de destinatarios que un usuario puede direccionar en un período de 24 horas. Por ejemplo, si este valor se establece en 500, significa que una sola cuenta de buzón de Exchange puede enviar mensajes a un máximo de 500 destinatarios cada día. Este límite se aplica a los mensajes a destinatarios que están dentro y fuera de la organización. Este límite predeterminado puede causar problemas para algunas aplicaciones de línea de negocio que realizan facturas de fin de mes y que necesitan enviar mensajes a más de este número de destinatarios. Puede usar servicios externos que permitan el procesamiento por lotes de mensajes o soluciones de retransmisión de salida local independientes para evitar esta limitación.

El parámetro de directiva **ForwardeeLimit** especifica el número máximo de destinatarios a los que se pueden reenviar o redirigir los mensajes mediante reglas de la bandeja de entrada. Este parámetro no limita el número de mensajes que se pueden reenviar o redirigir a los destinatarios.

## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>Errores generados al superar los límites de limitación

Cuando se superan las directivas de limitación, EWS genera uno de los errores enumerados en la siguiente tabla.

**Tabla 3: errores de límite de limitación**

|**Error**|**Parámetro de la Directiva de limitación**|**Descripción**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**EWSMaxConcurrency** <br/> |Indica que hay más solicitudes simultáneas en el servidor de las permitidas por la Directiva de un usuario.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |Indica que se ha superado el número máximo de suscripciones de la Directiva de limitación de un usuario.  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |Indica que una llamada a una operación de búsqueda ha superado el número total de elementos que se pueden devolver.  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC**         **EWSPercentTimeInCAS**         **EWSPercentTimeInAD** <br/> |Se produce cuando el servidor está ocupado. El valor BackOffMilliseconds devuelto con ErrorServerBusy errores indica al cliente la cantidad de tiempo que debe esperar hasta que deba volver a enviar la solicitud que causó la respuesta que ha devuelto el código de error.  <br/> |

En la siguiente tabla se enumeran los códigos de Estado HTTP que se devuelven al limitar los errores.

**Tabla 4: códigos de Estado HTTP devueltos por errores de limitación**

|**Código de estado HTTP**|**Descripción**|
|:-----|:-----|
|HTTP 503  <br/> |Indica que las solicitudes de EWS se encuentran en la cola de IIS. El cliente debe retrasar el envío de solicitudes adicionales hasta un momento posterior.  <br/> |
|HTTP 500  <br/> |Indica un error interno del servidor con el código de error ErrorServerBusy. Esto indica que el cliente debe retrasar el envío de solicitudes adicionales hasta un momento posterior. La respuesta puede contener una sugerencia de deshacer llamada BackOffMilliseconds. Si está presente, el valor de BackOffMilliseconds debe usarse como duración hasta que el cliente reenvíe una solicitud.  <br/> |
|HTTP 200  <br/> |Contiene una respuesta de error basada en esquema EWS con un código de error ErrorInternalServerError. Es posible que haya un código de error ErrorServerBusy interno. Esto indica que el cliente debe retrasar el envío de solicitudes adicionales hasta un momento posterior.  <br/> |

## <a name="see-also"></a>Vea también

- [Administración de la carga de trabajo de Exchange](https://technet.microsoft.com/library/jj150503.aspx)
- [New-ThrottlingPolicy cmdlet](https://technet.microsoft.com/library/dd351045.aspx)
- [Descripción de las directivas de limitación de clientes](https://technet.microsoft.com/library/dd297964.aspx)
- [Clase ThrottlingPolicy](https://msdn.microsoft.com/library/ff342496%28v=EXCHG.140%29.aspx)
- [Directivas de limitación de peticiones y EWSFindCountLimit](https://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [Instantáneas de presupuesto en los registros de IIS](https://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)

- [Efectos de la limitación en su implementación en Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Asociaciones de directivas de limitación de peticiones en Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [Directivas de limitación de peticiones y CPUStartPercent](https://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
