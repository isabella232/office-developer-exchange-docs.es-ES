---
title: EWS limitación en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: b4fff4c9-c625-4d2a-9d14-bb28a5da5baf
description: Obtenga información acerca de las directivas de limitación que afectan a EWS cuando se usa Exchange.
ms.openlocfilehash: 64393c173a6fc60cd4be969e8c7457d5b0109713
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354018"
---
# <a name="ews-throttling-in-exchange"></a>EWS limitación en Exchange

Obtenga información acerca de las directivas de limitación que afectan a EWS cuando se usa Exchange.
  
**Proporcionado por:** Escalas de Glen; Michael Mainer, Microsoft Corporation 
  
El artículo proporciona información acerca de EWS limitación en Exchange Online, Exchange Online como parte de Office 365, locales y en las versiones de Exchange a partir de Exchange 2010. Limitación en Exchange ayuda a garantizar la confiabilidad del servidor y el tiempo de actividad si limita la cantidad de recursos de servidor que puede consumir un solo usuario o una aplicación. Limitación de peticiones es una respuesta reactiva para uso excesivo de recursos del sistema que pueden afectar a la funcionalidad y confiabilidad de los servicios. Exchange supervisa constantemente el estado crítico de recursos de infraestructura, como bases de datos de buzón de correo. Cuando se detectan los factores de carga elevada que degradar el rendimiento de estos recursos, conexiones de EWS se aceleran de forma proporcional en función de la cantidad que cada autor de la llamada ha contribuido a esta condición de carga elevada. El resultado es que un usuario puede estar dentro de su límite de limitación de peticiones y sigue teniendo una ralentización hasta que el estado del recurso es nuevamente en los niveles operativos.
  
Cada protocolo de acceso de cliente de Exchange, incluidos EWS, tiene una directiva de limitación. Al diseñar las aplicaciones que usan EWS, es importante tener en cuenta para que las directivas de limitación de peticiones, para ayudar a garantizar la confiabilidad de la aplicación y el estado de su servidor de Exchange. En este artículo identifica los límites de servicio y diferentes directivas de limitación de EWS, si identificación de Exchange Online o versiones de Exchange local empezando con Exchange Server 2010. Según corresponda, en este artículo se identifica las diferencias en la limitación de las directivas de diferentes versiones de Exchange.
  
> [!IMPORTANT]
> El valor predeterminado de directiva de limitación, acceso a la directiva de limitación y configuración de la directiva de limitación difiere entre Exchange Online y Exchange local. Valores de configuración de limitación de peticiones específicos sólo son precisos para una versión específica de Exchange. Debido a que los valores de configuración pueden variar entre versiones y debido a que los administradores de Exchange pueden cambiar la directivas para las implementaciones locales de limitación predeterminada, este artículo no proporciona los valores de configuración el valor predeterminado. Es más importante que debe tener en cuenta las consideraciones para el diseño de una aplicación que funciona dentro de los límites de limitación y reacciona adecuadamente para escenarios de limitación. 
  
Si es un desarrollador de aplicaciones, necesita factor de limitación en el diseño de la aplicación. Las diferentes versiones de Exchange tienen valores predeterminados diferentes para los parámetros de limitación de peticiones de EWS. Las aplicaciones cliente y el servicio que se han diseñado para tener acceso a las diferentes versiones de Exchange se deben tener en cuenta para estas configuraciones, ya sean valores predeterminados, valores personalizados establecidos por un administrador de Exchange, o bien, como para Exchange Online, establece de forma predeterminada y no que se pueda detectar. Debido a que la limitación de los valores de parámetro no se puede detectar mediante programación, las especificaciones de diseño de cliente deben incluir un plan para la aplicación para adaptarse a diferente potencial superado la limitación. Al diseñar aplicaciones multiproceso que tendrán acceso a un gran número de buzones de correo, o cuando muchos clientes se tenga acceso al buzón mismo, tenga en cuenta los límites de simultaneidad que la directiva predeterminada se aplica a Exchange. 
  
## <a name="throttling-policies-that-affect-ews"></a>Directivas de limitación que afectan a EWS
<a name="bk_PolicyParameters"> </a>

La limitación de directivas en afectan de Exchange no solo EWS, sino también todas las conexiones de cliente en el servidor de Exchange, incluidos los protocolos utilizan por Office Outlook, Outlook Web App y Exchange ActiveSync. 
  
El **CPUStartPercent** directiva de limitación puede afectar al rendimiento de EWS cuando se ejecutan Exchange 2010. Cuando el uso de CPU promedio de Exchange procesos que se ejecutan en el servidor de acceso de cliente, incluidos, pero sin limitarse a, el proceso de EWS: supera el valor especificado por esta directiva, se retrasarán las solicitudes entrantes para reducir el uso de la CPU. No se puede cambiar el valor de esta directiva, pero conocer acerca de él puede ayudarle a solucionar problemas de rendimiento. La lógica de muestreo que realiza el servidor de acceso de cliente para este valor es una media de un segundo 10 ventana con desplazamiento. Esto permite que el proceso de responder adecuadamente a rápido picos de uso de CPU. Cuando se supera este umbral, se retrasarán las conexiones entrantes a EWS. Este retraso se restringe al 500 milisegundos (ms) con un uso de CPU del 100% teórico por solicitud EWS. Si se pasa una solicitud EWS por lotes para obtener elementos de 100, el servidor comprobará el uso de CPU 100 veces (una vez por cada elemento) para un retraso máximo de 50 segundos. El tiempo de retraso es linealmente proporcional al uso de la CPU. En **CPUStartPercent**, el retraso es 0 (el rendimiento de un subproceso) y aumenta linealmente hasta llegar a 500 ms con 100% de uso de CPU. Debido a que las directivas de limitación de peticiones se aplican a todos los usuarios de Exchange, es poco probable que el uso de CPU excede el límite de **CPUStartPercent** en un servidor de acceso de cliente de Exchange, debido a que los usuarios individuales o aplicaciones no pueden obtener suficiente utilización de la CPU afecte a operación del servidor. 
  
En la siguiente tabla se enumera los parámetros de directiva de limitación que afectan a las aplicaciones que usan EWS.
  
**Tabla 1: Limitación de los parámetros de directiva que afectan a EWS**

|**Nombre de parámetro de la directiva de limitación**|**Se aplica a**|**Descripción**|
|:-----|:-----|:-----|
|**DiscoveryMaxConcurrency** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de conexiones de búsqueda de detección simultáneas que un usuario puede tener al mismo tiempo.  <br/> |
|**DiscoveryMaxKeywords** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de palabras clave que un usuario puede incluir en una búsqueda de detección.  <br/> |
|**DiscoveryMaxKeywordsPerPage** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de palabras clave que se va a mostrar las estadísticas.  <br/> |
|**DiscoveryMaxMailboxes** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de buzones de origen que un usuario puede incluir en una búsqueda de detección.  <br/> |
|**DiscoveryMaxMailboxesResultsOnly** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número máximo de buzones puede buscar en una exhibición de documentos electrónicos en contexto de búsqueda sin poder ver las estadísticas.  <br/> |
|**DiscoveryPreviewSearchResultsPageSize** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Especifica el número de mensajes devueltos en una respuesta de vista previa de búsqueda de exhibición de documentos electrónicos.  <br/> |
|**EwsCutoffBalance** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define los límites de consumo de recursos para el usuario EWS antes de que el usuario está bloqueado completamente de realizar operaciones en un componente específico.  <br/> |
|**EwsMaxBurst** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define la cantidad de tiempo que un usuario EWS puede consumir una cantidad de recursos con privilegios elevados antes de que se está limitado. Esto se mide en milisegundos. Este valor está establecido por separado para cada componente.  <br/> |
|**EwsRechargeRate** <br/> |Exchange 2013  <br/> Exchange Online  <br/> |Define la velocidad a la que se recarga presupuesto de un usuario EWS (el presupuesto aumenta) durante el tiempo de presupuesto.  <br/> |
|**EWSMaxSubscriptions** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número máximo de inserción activo, de extracción y transmisión por secuencias de suscripciones de notificación de que un usuario puede tener a la vez en un servidor de acceso de cliente específico. Es presupuestado de manera diferente para distintas versiones de Exchange.  <br/> |
|**EWSFastSearchTimeoutInSeconds** <br/> |Exchange 2010  <br/> |Define la cantidad de tiempo en segundos que fast búsquedas realizadas mediante el uso de búsqueda de Exchange en EWS continuar antes de que el tiempo de espera. Búsquedas Fast utilizan realizados mediante una cadena de consulta de sintaxis de consulta avanzada (AQS) en una [operación de FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).  <br/> |
|**EWSFindCountLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número máximo de elementos de una [operación de FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) u [FindFolder operación](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) que pueden existir en la memoria en el servidor de acceso de cliente a la vez para un usuario. El valor predeterminado de esta propiedad es 1000. El [valor de reserva](http://technet.microsoft.com/en-us/library/dd297964%28v=exchg.141%29.aspx#fallback)para este valor es 1000.  <br/> En Exchange Online y versiones locales de Exchange a partir de Exchange 2013, esta directiva de limitación no se puede ser consultada o configurada por un cmdlet. En las versiones de Exchange Online y local de Exchange a partir de con Exchange 2013, la EWSFindCountLimit para la [búsqueda AQS](how-to-perform-an-aqs-search-by-using-ews-in-exchange.md) y cualquier Exchange search con una restricción es 250 resultados. Una búsqueda de Exchange sin una restricción devolverá hasta 1000 resultados.  <br/> |
|**EWSPercentTimeInAD** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar solicitudes de Active Directory.  <br/> |
|**EWSPercentTimeInCAS** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar código de servidor de acceso de cliente.  <br/> |
|**EWSPercentTimeInMailboxRPC** <br/> |Exchange 2010  <br/> |Define el porcentaje de tiempo por minuto durante el cual un usuario específico puede ejecutar las solicitudes RPC de buzón de correo  <br/> |
|**EWSMaxConcurrency** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número de conexiones simultáneas de open que puede tener un usuario específico en un servidor de Exchange que está usando EWS al mismo tiempo. El valor predeterminado de Exchange 2010 es 10. El valor predeterminado de Exchange 2013 y Exchange Online es 27.  <br/> Esta directiva se aplica a todas las operaciones excepto la transmisión por secuencias de notificaciones. Las notificaciones de transmisión por secuencias utilizan la **HangingConnectionLimit** para indicar el número de conexiones de evento transmisiones abiertas que están disponibles. Para obtener más información, vea [qué valores limitación es necesario tener en cuenta?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).  <br/> |
|**MessageRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el número de mensajes por minuto que se pueda enviar.  <br/> |
|**RecipientRateLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el límite para el número de destinatarios que un usuario puede tratar en un período de 24 horas.  <br/> |
|**ForwardeeLimit** <br/> |Exchange 2010  <br/> Exchange 2013  <br/> Exchange Online  <br/> |Define el límite para el número de destinatarios para acciones de avance/redireccionamiento de bandeja de entrada en un período de 24 horas.  <br/> |
   
> [!CAUTION]
> No establezca directivas de limitación en **null**. Esto establecerá la directiva para que sea ilimitado, que indica que no se ha establecido una directiva de limitación. 
  
## <a name="displaying-the-policies-that-apply-to-exchange-mailboxes"></a>Visualización de las directivas que se aplican a los buzones de Exchange
<a name="bk_PolicyCmdlets"> </a>

Exchange local proporciona cmdlets del Shell de administración de Exchange que puede usar para establecer y obtener la directiva de limitación. Exchange Online no proporciona acceso a los cmdlets de directiva de limitación de peticiones.
  
Puede usar los siguientes cmdlets para mostrar la limitación de directivas para una implementación de Exchange Server local:
  
- **Get-ThrottlingPolicy** : Obtiene el cliente de la configuración para uno o varios de limitación directivas de limitación. Para obtener más información, vea [Get-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351264.aspx) en TechNet. 
    
- **Get-ThrottlingPolicyAssociation** : permite ver la relación entre un objeto y sus directivas de limitación asociadas. El objeto puede ser un usuario con un buzón de correo, un usuario sin un buzón o a un contacto. Para obtener más información, vea [Get-ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459241.aspx) en TechNet. 
    
Use el siguiente comando para mostrar la directiva de Exchange 2010 de limitación predeterminada.
  
**Get-ThrottlingPolicy | Where-Object {$_. IsDefault - eq "True"} | formato de lista**
  
Use el siguiente comando para mostrar la directiva de limitación global (que equivale a la directiva de limitación predeterminada en Exchange 2010) en Exchange 2013.
  
**Get-ThrottlingPolicy | Where-Object {$_. ThrottlingPolicyScope - eq "Global"} | formato de lista**
  
Use el siguiente comando para mostrar la directiva asociado con un usuario en Exchange 2010 o Exchange 2013 de limitación de peticiones. Reemplace el nombre de usuario john@contoso.com con el nombre de usuario del usuario de destino para el que desea obtener información de la directiva de limitación.
  
**Get-ThrottlingPolicyAssociation john@contoso.com | formato de lista**
  
Ejecutando este comando en Exchange Management Shell da como resultado un resultado similar al siguiente.
  
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
> Cuando la propiedad **ThrottlingPolicyId** está en blanco, se aplica la directiva predeterminada para el buzón de correo. 
  
Puede establecer la directiva en un servidor de Exchange de limitación mediante el uso de los cmdlets [Set-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd298094.aspx) y [Set-ThrottlingPolicyAssociation](http://technet.microsoft.com/en-us/library/ff459231.aspx) . Puede crear y quitar directivas de limitación mediante el uso de los cmdlets [New-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351045.aspx) y [Remove-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351178.aspx) distinta de la predeterminada. 
  
> [!TIP]
> Se recomienda que diseñe sus aplicaciones para que se ajustan a la directiva de limitación predeterminada. Sólo puede realizar cambios en las directivas de limitación si el diseño de la aplicación de cliente no puede dar cabida a la directiva predeterminada predeterminada. Tenga en cuenta que las directivas de limitación menos restrictivas pueden afectar negativamente a la confiabilidad de los servicios. 

<a name="bk_ThrottlingConsiderations"> </a>

## <a name="throttling-considerations-for-applications-that-use-ews-impersonation"></a>Consideraciones sobre la limitación de peticiones para las aplicaciones que usan la suplantación de EWS


[La suplantación](impersonation-and-ews-in-exchange.md) es un método de autorización que permite una única cuenta tener acceso a muchas cuentas. Cuando suplanta una cuenta de servicio a los usuarios, actúa como los usuarios y, por tanto, se da por supuesto los derechos que se asignan a los usuarios. Los archivos de registro registran el acceso como el usuario suplantado. Los administradores usar control de acceso basado en roles (RBAC) para configurar la suplantación a través de la consola de administración de Exchange. 
  
Cuando se utiliza la suplantación, los presupuestos de los umbrales de limitación de peticiones se aplican de manera diferente dependiendo de la versión de Exchange. O bien se calcula el presupuesto frente a la cuenta que se suplanta o la cuenta de servicio. Si la aplicación es multiproceso y realiza solicitudes simultáneas frente a varios buzones, debe tener en cuenta cómo el umbral de limitación de peticiones se afectan al rendimiento de la aplicación. En general, tenga en cuenta los siguientes límites en las cuentas de servicio cuando se crea una aplicación de servicio que emplea la suplantación para tener acceso a todos los buzones: 
  
- Cuando se utiliza la suplantación, la cuenta de servicio tiene un presupuesto independiente de los siguientes parámetros de directiva:
    
  - **EWSMaxConcurrency**
    
  - **EWSPercentTimeInAD**
    
  - **EWSPercentTimeInCAS**
    
  - **EWSPercentTimeInMailboxRPC**
    
  - **EWSMaxSubscriptions**
    
  - **EWSFastSearchTimeoutInSeconds**
    
  - **EWSFindCountLimit**
    
- El presupuesto de **EWSMaxConcurrency** se comparte para la cuenta de servicio y la cuenta suplantado para todas las conexiones a las versiones de Exchange anteriores a Service Pack 2 (SP2) de Exchange 2010 acumulativo de actualizaciones 4 (RU4). Empezando con Exchange 2010 SP2 RU4 e incluido Exchange Online, el acceso de la cuenta de servicio usa un presupuesto independiente desde el presupuesto de **EWSMaxConcurrency** de usuario. Para obtener más información acerca de la actualización para la directiva de limitación de conexiones simultáneas de Exchange para EWS, consulte [Descripción de actualización de paquete acumulativo de actualizaciones 4 para Exchange Server 2010 Service Pack 2](http://support.microsoft.com/kb/2706690).
    
    EWS transmisión por secuencias notificaciones en las versiones de Exchange comenzando con Exchange 2010 e incluido Exchange Online, tener un presupuesto de **EWSMaxConcurrency** clonado adicional de todas las otras conexiones de cliente EWS. Transmisión por secuencias de las conexiones de notificación se cuentan con un presupuesto independiente que todas las otras operaciones de EWS. El presupuesto de simultaneidad máximo de notificación transmisión por secuencias es realmente dos presupuestos diferentes: un presupuesto es para todas las cuentas de servicio, y un presupuesto para la cuenta que se suplanta. Transmisión por secuencias de notificaciones en Exchange Online y versiones de Exchange a partir de Exchange 2013 usan el [HangingConnectionLimit](ews-throttling-in-exchange.md#bk_ThrottlingNotifications) para limitar el número de conexiones. 
    
    Por ejemplo, supongamos que **EWSMaxConcurrency** es igual a cinco. Un usuario puede tener cinco conexiones de notificación de extracción abierto, mientras que una cuenta de servicio puede tener cinco conexiones de notificación de extracción simultáneas contra el buzón del usuario al mismo tiempo que el usuario. 
    
- En la siguiente tabla identifica cómo se calculan los presupuestos de limitación de peticiones de **EWSMaxSubscriptions** entre la cuenta de servicio y la cuenta para suplantar. 
    
   **La tabla 2: Contabilidad de presupuesto EWSMaxSubscriptions**

   |**Versión de Exchange**|**EWSMaxSubscriptions limitación de contabilidad de presupuesto**|
   |:-----|:-----|
   |Exchange Online  <br/> |Carga contra el buzón de destino.  <br/> |
   |Exchange 2013  <br/> |Carga contra el buzón de destino.  <br/> |
   |SP3 de Exchange 2010  <br/> |Carga contra el buzón de destino.  <br/> |
   |Exchange 2010 SP2  <br/> |Atribuyen a la cuenta que llama. A partir de Exchange 2010 SP2 RU4, se carga el presupuesto con el buzón de destino.  <br/> |
   |Exchange 2010 SP1  <br/> |Atribuyen a la cuenta que llama.  <br/> |
   |Exchange 2010  <br/> |Atribuyen a la cuenta que llama.  <br/> |
   
- Debido a que la **EWSMaxSubscriptions** limitación presupuestado se atribuyen a la cuenta que se suplanta, no hay ningún límite en el número de buzones de correo de una cuenta de servicio puede suscribirse a y recibir notificaciones de transmisión por secuencias para, siempre que sea de suplantación se utiliza. Para la cuenta que se suplanta, no puede tener más de solicitudes simultáneas de _n_ por buzón de destino, donde _n_ es el valor de **EWSMaxSubscriptions** . Si no se utiliza la suplantación, la misma cuenta de servicio podría no tener más de solicitudes simultáneas de _n_ totales. Por lo tanto, la conclusión es que mediante la suplantación en una cuenta de servicio, forma exponencial aumenta el número de buzones que puede dar servicio. Para obtener más información, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones en Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md).
    
- Los parámetros de directiva **EWSPercentTimeInMailboxRPC**, **EWSPercentTimeInCAS**y **EWSPercentTimeInAD** hacen referencia a las acciones realizadas por un único subproceso. Cuando una aplicación realiza varias operaciones simultáneas, debe contabilizar el efecto acumulativo de estas operaciones en el presupuesto de recurso de usuario. 
    
## <a name="throttling-implications-for-ews-batch-requests"></a>Limitación de implicaciones para las solicitudes de lote EWS
<a name="bk_ThrottlingBatch"> </a>

EWS permite por lotes varias solicitudes de elemento en una única solicitud que se ejecuta el servidor de acceso de cliente. Esto permite la mayor eficacia y rendimiento. Cuando un servidor de Exchange ejecuta una solicitud por lotes, comprueba presupuesto del usuario después de la ejecución de cada elemento dentro del lote. Si la aplicación está por encima del presupuesto, se retrasa el procesamiento del siguiente elemento en el lote hasta que se ha cargado el presupuesto de dicho usuario. Para asegurarse de que las aplicaciones que usan las operaciones por lotes se ejecutarán correctamente, limitar el número de solicitudes de elemento que se puede incluir en un único lote y dividir lotes grandes a través de varios lotes más pequeños para aumentar la confiabilidad de los resultados. El efecto que tiene una operación por lotes los umbrales de limitación de peticiones determinado depende del tipo de la solicitud, el tamaño de los elementos que va a procesar (por ejemplo, en las operaciones de **UploadItems** o **ExportItems** ) y el contenido de los buzones. Directivas de limitación afecta a las operaciones por lotes por lo que provoca que la solicitud a tardar más en proceso. El autor de la llamada, por tanto, tendrá que esperar la respuesta ya, y porque EWS limita el tiempo de ejecución de una solicitud por lotes a un minuto, la llamada podría tiempo de espera. 
  
Para determinar el tamaño de lote óptimo para una aplicación, realizar pruebas utilizando una unidad que diversas entradas establece para asegurarse de que la aplicación no producen errores en un entorno de producción. 
  
## <a name="throttling-policy-parameters-that-affect-ews-search-operations"></a>Operaciones de búsqueda de la limitación de los parámetros de directiva que afectan a EWS
<a name="bk_ThrottlingSearch"> </a>

[Operaciones de búsqueda en EWS](search-and-ews-in-exchange.md) puede requerir grandes cantidades de tiempo y recursos, dependiendo de cómo se ejecuta la búsqueda y qué información se solicita. Para controlar el uso de recursos durante las búsquedas, dos parámetros de directiva surtan efecto: **EWSFastSearchTimeoutInSeconds** y **EWSFindCountLimit**. 
  
El parámetro de directiva **EWSFastSearchTimeoutInSeconds** especifica la cantidad de tiempo, en segundos, que las búsquedas fast de EWS (también conocido como contenido de búsqueda indización) ejecutar antes de que se agote el tiempo. Una búsqueda rápida es una búsqueda realizada mediante el uso de una cadena de consulta de sintaxis de consulta avanzada (AQS) en una [operación de FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx).
  
Puede buscar en una carpeta de buzón de correo de Exchange de dos maneras:
  
- Mediante el uso de una búsqueda de almacén de Exchange, que realiza un examen secuencial de todos los mensajes en el ámbito de búsqueda de destino.
    
- Con el servicio de búsqueda de Exchange (indización de contenido).
    
Estos dos tipos de búsquedas pueden provocar tiempos de espera. Cuando sea posible, utilice el servicio de búsqueda de Exchange debido a que estas búsquedas en índices de buzón de correo a menudo destinadas y utilizar las consultas AQS. En el ejemplo siguiente se muestra cómo se realiza una búsqueda de AQS de la Bandeja de entrada mediante el uso de EWS y el servicio de búsqueda de Exchange.
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiitems = service.FindItems(WellKnownFolderName.Inbox, "subject:football", iv);
```

Si no se puede usar una búsqueda AQS, evitar el uso de filtros de búsqueda demasiado compleja. También intenta evitar la creación de filtros de búsqueda basándose en valores calculados si la consulta implica las propiedades extendidas de MAPI. Búsqueda AQS se introdujo en Exchange 2010.
  
> [!NOTE]
> La primera vez que ejecute una consulta de búsqueda de almacén de Exchange compleja, se ejecuta muy lentamente y es posible que el tiempo de espera. Después de, la consulta va a responder más rápidamente. Para obtener más información sobre el back-end Exchange los procesos del servidor que se producen durante Exchange almacenar las consultas de búsqueda, vea la [Descripción de las vistas restringidas y rendimiento impacto de alta recuentos de artículos](http://technet.microsoft.com/en-us/library/cc535025%28EXCHG.80%29.aspx) en TechNet. Uso de un **SearchFilter** crea una restricción dinámica que ayuda a consultas similares en el futuro, pero debido a que estas restricciones son de naturaleza dinámica, no son permanentes o confiable y se eliminan después de un máximo de tres días. 
  
El parámetro de directiva **EWSFindCountLimit** especifica el número máximo de elementos de los resultados de una operación **FindItem** o **FindFolder** que pueden existir en la memoria en un servidor de acceso de cliente al mismo tiempo para un usuario. Cada elemento o carpeta que procesa EWS en una solicitud **FindItem** o **FindFolder** se cuenta con respecto al presupuesto especificado en el elemento **EWSFindCountLimit** . Cuando se envía la respuesta de vuelta al solicitante, se libera el cargo de recuento de búsqueda para la llamada actual. La respuesta que devuelve el servidor a un solicitante cuando se supere el presupuesto se basa en el valor del elemento **RequestServerVersion** y si el solicitante especificado paginación. Cuando el valor del elemento **RequestServerVersion** indica Exchange 2010 o una versión anterior de Exchange, el servidor envía una respuesta de error con el código de error **ErrorServerBusy**. Si el valor del elemento **RequestServerVersion** indica una versión de Exchange a partir de Exchange 2010 SP1 o Exchange Online y el cliente está usando la paginación, EWS puede devolver un resultado parcial establecido en lugar de un error. La aplicación debe esperar que EWS no puede devolver todos los elementos. Si el valor del elemento **IncludesLastItemInRange** es false, la aplicación debe realizar otra solicitud **FindItem** o **FindFolder** con el nuevo desplazamiento y seguir hasta que el elemento **IncludesLastItemInRange** devuelve el valor true. 
  
Cuando se usa una operación **FindItem** o **FindFolder** , es importante utilizar la paginación. La API administrada de EWS exige el uso de paginación, pero si está utilizando otros métodos, como los objetos de servidor proxy EWS o SOAP sin procesar, debe establecer explícitamente la paginación. En el ejemplo siguiente se muestra cómo utilizar la paginación en la API administrada de EWS. 
  
```cs
ItemView iv = new ItemView(1000);
FindItemsResults<Item> fiFindItemResults = service.FindItems(WellKnownFolderName.Inbox, iv);
```

> [!NOTE]
> La directiva predeterminada de Exchange limita el tamaño de página a 1000 elementos. Si se establece el tamaño de página en un valor que es mayor que este número no tiene ningún efecto práctico. 
  
Aplicaciones también deben tener en cuenta el hecho de que la _EWSFindCountLimit_ en el valor del parámetro de limitación puede producir en un conjunto que se devuelve para aplicaciones que realizan solicitudes simultáneas de resultados parcial. En el ejemplo siguiente se muestra cómo usar la propiedad **MoreAvailable** de la API administrada de EWS para asegurarse de que todos los resultados se encuentran en una consulta. 
  
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

## <a name="throttling-policies-and-concurrency"></a>Directivas de limitación y simultaneidad
<a name="bk_ThrottlingConcurrency"> </a>

Simultaneidad hace referencia al número de conexiones de un usuario específico. Una conexión se mantiene desde el momento en que se recibe una solicitud hasta que se envía una respuesta al solicitante. Si los usuarios intentan realizar más peticiones simultáneas que permite su directiva, se produce un error en el intento de conexión nueva. Sin embargo, las conexiones existentes permanecen válidas. Limitación de las directivas puede afectar a la simultaneidad en un número de formas diferentes.
  
El parámetro de directiva de limitación de peticiones **EWSMaxConcurrency** establece el número de conexiones simultáneas que puede tener un usuario específico en un servidor de Exchange a la vez. Para determinar el número máximo de conexiones simultáneas para permitir, considere la posibilidad de las conexiones que va a usar los clientes de Outlook. Outlook 2007 y Outlook 2010 usan EWS para obtener acceso a la disponibilidad y la información de fuera de oficina (OOF). Mac Outlook 2011 usa EWS para toda la funcionalidad de acceso cliente. Según la cantidad de clientes de Outlook que se conecta activamente al buzón de un usuario, el número de conexiones simultáneas disponibles para un usuario podría estar limitado. Además, si tiene la aplicación para conectarse a varios buzones simultáneamente durante el uso de un contexto de seguridad único, es importante tener el valor de la directiva de **EWSMaxConcurrency** en cuenta. Para obtener más información acerca del uso de un contexto de seguridad único con conexiones simultáneas, vea [Consideraciones de la limitación para las aplicaciones que usan la suplantación de EWS](#bk_ThrottlingConsiderations) anteriormente en este artículo. 
  
Aplicaciones que se conectan simultáneamente a varios buzones de correo tienen que puedan realizar un seguimiento de uso de recursos en el lado del cliente. Debido a que las operaciones de EWS están basados en solicitud/respuesta, puede asegurarse de la función de las aplicaciones también dentro del umbral de **EWSMaxConcurrency** por el número de conexiones que se producen entre el inicio de una solicitud y cuando la respuesta de seguimiento recibidos y asegurarse de que no más de diez abrir solicitudes se producen simultáneamente. 
  
El parámetro de directiva **EWSFindCountLimit** especifica el tamaño máximo de resultados que una operación **FindItem** o **FindFolder** puede usar en un servidor de acceso de cliente al mismo tiempo para un usuario. Si una aplicación (o potencialmente varias aplicaciones) realiza dos solicitudes simultáneas de EWS **FindItem** que devuelven 100 elementos para un usuario específico, el cargo de **EWSFindCountLimit** frente a presupuesto de ese usuario específico será 200. Cuando se devuelve la primera solicitud, el presupuesto se coloca a 100 y, cuando se devuelve la segunda solicitud de, el presupuesto disminuye a cero. Si la misma aplicación eran realizar dos solicitudes simultáneas de 1000 elementos, el valor de presupuesto sería 2.000 elementos, que supera el valor de **EWSFindCountLimit** . Si presupuesto del usuario para elementos cae por debajo de cero, la siguiente solicitud da como resultado un error hasta que se recarga presupuesto del usuario a uno o más. 

<a name="bk_ThrottlingNotifications"> </a>
  
## <a name="throttling-considerations-for-ews-notification-applications"></a>Consideraciones sobre la limitación EWS para aplicaciones de notificaciones


Si va a crear la notificación de EWS aplicaciones hacen uso de inserción, extracción o transmisión por secuencias de notificaciones, debe tener en cuenta las implicaciones de la **EWSMaxSubscriptions** y las directivas de limitación de peticiones de **EWSMaxConcurrency** y el ** HangingConnectionLimit**. 
  
El parámetro de directiva **EWSMaxSubscriptions** especifica el número máximo de inserción activo, de extracción y suscripciones de transmisión por secuencias que puede tener un usuario en un servidor de acceso de cliente específico al mismo tiempo. Las diferentes versiones de Exchange tienen valores predeterminados diferentes para este parámetro. Un usuario puede suscribirse a todas las carpetas de un buzón de correo mediante el uso de la propiedad **SubscribeToAllFolders** - esto usa una sola suscripción con respecto al presupuesto **EWSMaxSubscriptions** . Los usuarios pueden suscribirse a carpetas individuales, con cada carpeta suscripción contando hacia el presupuesto **EWSMaxSubscriptions** , hasta el límite establecido por el valor del parámetro **EWSMaxSubscriptions** (por ejemplo, los usuarios pueden suscribirse a calendario de 20 carpetas de buzones diferentes si **EWSMaxSubscriptions** está establecido en 20). 
  
Para obtener información acerca de la suplantación y el parámetro **EWSMaxSubscriptions** , vea [Consideraciones de la limitación para las aplicaciones que usan la suplantación de EWS](#bk_ThrottlingConsiderations) anteriormente en este artículo. 
  
El parámetro de directiva de **EWSMaxConcurrency** también puede ser un problema para las notificaciones de EWS; Por ejemplo: 
  
- Cuando EWS incrementa el recuento de conexión para el propietario de la suscripción mientras se genera la notificación por una suscripción de inserción.
    
- Cuando una aplicación está diseñada para escuchar a los buzones de los usuarios de varios, y los usuarios reciben notificaciones simultáneas para una instancia de un mensaje que se envía a una lista de distribución.
    
Si la aplicación de notificación es multiproceso y hace que las solicitudes de conexión simultáneas para obtener más información acerca de un mensaje concreto que se ha recibido por una cuenta de usuario, puede ser se ha excedido el límite de la directiva de **EWSMaxConcurrency** . Para tener en cuenta para esto, considere la posibilidad de supervisar las conexiones simultáneas en la aplicación, los que podría ser utilizado por el servidor incluidos e implementación de solicitud de puesta en cola en el cliente. 
  
El **HangingConnectionLimit** sólo es aplicable a la transmisión por secuencias de notificaciones. Este límite se establece en el archivo web.config, lo que significa que un administrador de Exchange puede establecer este valor en un servidor de Exchange local, pero los buzones de Exchange Online deben usar el valor predeterminado de este límite, que es 3 para Exchange Online y Exchange 2013. Para obtener más información, vea [qué valores limitación es necesario tener en cuenta?](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md#bk_throttling).
  
## <a name="throttling-policy-and-application-performance"></a>Rendimiento de la aplicación y de directiva de limitación
<a name="bk_PercentTimeIn"> </a>

Los siguientes tres parámetros de la **PercentTimeIn** directiva de limitación afecta a la cantidad de tiempo que puede consumir una aplicación de EWS en un servidor de acceso de cliente: 
  
- **EWSPercentTimeInAD**
    
- **EWSPercentTimeInCAS**
    
- **EWSPercentTimeInMailboxRPC**
    
Los valores especificados en los parámetros de directiva **PercentTimeIn** indican la cantidad de tiempo que se asigna un subproceso realiza una solicitud. Por ejemplo, suponiendo que un valor de **EWSPercentTimeInCAS** de 90, si hace que un proceso de dos solicitudes simultáneas que dedican 54 segundos cada código que se está ejecutando en el servidor de acceso de cliente, el proceso utiliza 108 segundos en un segundo 60 ventana. Esto representa un valor del parámetro **EWSPercentTimeInCAS** por ciento de 180. 
  
> [!NOTE]
> El valor del parámetro **EWSPercentTimeInCAS** es un superconjunto de los valores de parámetro **EWSPercentTimeInAD** y **EWSPercentTimeInMailboxRPC** superpuesta. Esto significa que los gastos en tiempo de procesamiento en el servidor de acceso de cliente siempre será mayor que los gastos en **EWSPercentTimeInAD** y **EWSPercentTimeInMailboxRPC**. Esto es porque para que el componente de Exchange hacer un Active Directory o RPC de llamadas, debe ya se está ejecutando el código del servidor de acceso de cliente. Además, los gastos en tiempo de procesamiento para **EWSPercentTimeInCAS** no se detención mientras LDAP o se realizan llamadas RPC. Aunque la solicitud esté sincrónicamente esperando una respuesta de los servicios de dominio de Active Directory (AD DS) o el almacén de Exchange, el proceso aún está consumiendo un subproceso en el servidor y, por lo tanto, debe seguir el subproceso cargará para que el uso de. 
  
La cantidad de tiempo de CPU que una aplicación puede tardar en un período de 60 segundos es posible que exceden estos límites; por lo tanto, es importante tener en cuenta el volumen y el tipo de solicitudes que se realizan. Por ejemplo, un lote de gran tamaño de **ResolveNames** operaciones que se realizan simultáneamente puede superar el valor del parámetro **EWSPercentTimeInAD** directiva. Los valores de directiva que están contenidos en la directiva de limitación predeterminada están diseñados para permitir que la mayoría de las aplicaciones de EWS funcionar sin problemas; Sin embargo, cuando las aplicaciones de gran volumen multiproceso poner un gran volumen de solicitudes en un determinado servidor de acceso de cliente, puede crear problemas. Para evitar este problema, considere la posibilidad de limitar el tamaño de los lotes que se va a ejecutar en el servidor. 
  
## <a name="throttling-policies-and-applications-that-send-a-large-volume-of-email"></a>Limitación de las directivas y las aplicaciones que envían un gran volumen de correo electrónico
<a name="bk_RateLimits"> </a>

Las directivas de limitación predeterminada incluyen tres parámetros de directiva de límite de velocidad que pueden afectar a las aplicaciones que usan EWS para enviar un gran volumen de mensajes o enviar mensajes en lotes grandes en un breve período de tiempo. 
  
> [!NOTE]
> En general, se recomienda que no use EWS para enviar correo electrónico masivo. Use un host SMTP que está especializado en servicios de correo masivo para enviar mensajes de correo masivo de gran tamaño frecuentes. 
  
El parámetro de directiva **MessageRateLimit** especifica el número de mensajes por minuto que se pueden enviar por cualquier cliente de Exchange, incluidos EWS. De forma predeterminada, esta directiva se establece en 30 mensajes por minuto. Para los usuarios normales, esto es suele ser suficiente. Sin embargo, pueden ejecutar aplicaciones que envían lotes de gran tamaño de los mensajes de correo electrónico, por ejemplo como parte de un programa de facturación, problemas. Cuando se excede este límite de directiva, se retrasa la entrega de mensajes para el buzón de correo. En concreto, los mensajes aparecerán en la carpeta Bandeja de salida o borradores durante largos períodos de tiempo cuando un usuario o una aplicación envía un número mayor de mensajes que el valor especificado por el parámetro **MessageRateLimit** . Asegúrese de tener en cuenta esto cuando está desarrollando una entrega seguimiento del sistema, especialmente si la aplicación utiliza un buzón de correo que los usuarios se conectan a través de Outlook. Cuando diferidos elementos se almacenan en la carpeta Bandeja de salida o borradores, los usuarios podrían interpretar como un error. 
  
El parámetro de directiva **RecipientRateLimit** especifica el límite en el número de destinatarios que un usuario puede tratar en un período de 24 horas. Por ejemplo, si este valor se establece en 500, significa que una única cuenta de buzón de correo de Exchange puede enviar mensajes a ningún día de más de 500 destinatarios cada. Este límite se aplica a los mensajes a los destinatarios que están dentro y fuera de la organización. Este límite predeterminado puede causar problemas en algunas aplicaciones de línea de negocio que no se ejecuta de factura de fin de mes y necesitan para enviar mensajes a más de este número de destinatarios. Puede usar los servicios externos que permiten el procesamiento por lotes de mensajes o independiente en retransmisión saliente las soluciones locales para evitar esta limitación. 
  
El parámetro de directiva **ForwardeeLimit** especifica el número máximo de destinatarios que se pueden reenviar los mensajes o redirige a por medio de las reglas de bandeja de entrada. Este parámetro no limita el número de mensajes que se pueden reenviar o redirige a los destinatarios. 
  
## <a name="errors-generated-when-throttling-limits-are-exceeded"></a>Se superan los errores generados cuando superado la limitación
<a name="bk_ThrottlingErrors"> </a>

Limitación de directivas cuando se superan, EWS genera uno de los errores que aparecen en la siguiente tabla.
  
**La tabla 3: Errores de límite de limitación**

|**Error**|**Parámetro de la directiva de limitación**|**Descripción**|
|:-----|:-----|:-----|
|ErrorExceededConnectionCount  <br/> |**EWSMaxConcurrency** <br/> |Indica que no hay más peticiones simultáneas en el servidor de los permitidos por la directiva de un usuario.  <br/> |
|ErrorExceededSubscriptionCount  <br/> |**EWSMaxSubscriptions** <br/> |Indica que un usuario de la limitación de directiva se ha superado el número máximo de suscripciones.  <br/> |
|ErrorExceededFindCountLimit  <br/> |**EWSFindCountLimit** <br/> |Indica que una llamada de la operación de búsqueda ha superado el número total de elementos que se pueden devolver.  <br/> |
|ErrorServerBusy  <br/> |**EWSPercentTimeInMailboxRPC** **EWSPercentTimeInCAS** **EWSPercentTimeInAD**                   <br/> |Se produce cuando el servidor está ocupado. El valor de BackOffMilliseconds devuelto con errores ErrorServerBusy indica al cliente la cantidad de tiempo que debe esperar hasta que debe volver a enviar la solicitud que ha provocado la respuesta que devuelve este código de error.  <br/> |
   
En la siguiente tabla se enumera los códigos de estado HTTP que se devuelven mediante la limitación de errores.
  
**Tabla 4: Códigos de estado HTTP devueltos por la limitación de errores**

|**Código de estado HTTP**|**Descripción**|
|:-----|:-----|
|HTTP 503  <br/> |Indica que las solicitudes EWS se puesta en cola con IIS. El cliente debe retrasar el envío de las solicitudes adicionales hasta más adelante.  <br/> |
|HTTP 500  <br/> |Indica un error de servidor interno con el código de error ErrorServerBusy. Esto indica que el cliente debe retrasar el envío de las solicitudes adicionales hasta más adelante. La respuesta puede contener una copia de sugerencia denominado BackOffMilliseconds. Si está presente, el valor de BackOffMilliseconds debe utilizarse como la duración hasta que el cliente vuelve a enviar una solicitud.  <br/> |
|HTTP 200  <br/> |Contiene una respuesta de error basada en el esquema EWS con un código de error ErrorInternalServerError. Un código de error interno de ErrorServerBusy puede estar presente. Esto indica que el cliente debe retrasar el envío de las solicitudes adicionales hasta más adelante.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Administración de carga de trabajo de Exchange](http://technet.microsoft.com/en-us/library/jj150503.aspx)
- [Cmdlet New-ThrottlingPolicy](http://technet.microsoft.com/en-us/library/dd351045.aspx)
- [Descripción de las directivas de limitación](http://technet.microsoft.com/en-us/library/dd297964.aspx)
- [Clase ThrottlingPolicy](http://msdn.microsoft.com/en-us/library/ff342496%28v=EXCHG.140%29.aspx)
- [Directivas de limitación y el EWSFindCountLimit](http://blogs.msdn.com/b/exchangedev/archive/2010/03/12/throttling-policies-and-the-ewsfindcountlimit.aspx)
- [Instantáneas de presupuesto en los registros de IIS](http://blogs.msdn.com/b/exchangedev/archive/2010/03/10/budget-snapshots-in-the-iis-logs.aspx)
- [Efectos de limitación de la implementación de Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/27/456040.aspx)
- [Limitación de las asociaciones de directivas de Exchange 2010 SP1](http://msexchangeteam.com/archive/2010/08/02/455707.aspx)
- [Directivas de limitación y CPUStartPercent](http://blogs.msdn.com/b/exchangedev/archive/2010/03/11/throttling-policies-and-cpustartpercent.aspx)
- [Suplantación y EWS en Exchange](impersonation-and-ews-in-exchange.md)
    

