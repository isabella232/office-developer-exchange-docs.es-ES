---
title: Sincronización de buzones de correo y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: Descubra cómo funciona la sincronización de buzones de correo al usar EWS para tener acceso a Exchange.
localization_priority: Priority
ms.openlocfilehash: 5dc700c7feb9fce6121a27ee73fc1a58e88e643a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456263"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>Sincronización de buzones de correo y EWS en Exchange

Descubra cómo funciona la sincronización de buzones de correo al usar EWS para tener acceso a Exchange.
  
EWS en Exchange usa dos tipos de sincronización para recuperar el contenido de los buzones y los cambios en el contenido del buzón:
  
- Sincronización de carpetas
    
- Sincronización de elementos
    
En este artículo, obtendrá información sobre ambos tipos de sincronización, cómo funciona la sincronización, los patrones de diseño de sincronización y los procedimientos recomendados de sincronización.
  
## <a name="folder-and-item-synchronization"></a>Sincronización de carpetas y elementos
<a name="bk_typesofsyncs"> </a>

La sincronización de carpetas sincroniza una estructura de carpetas o una jerarquía de carpetas. La sincronización de elementos sincroniza los elementos dentro de una carpeta. Al sincronizar los elementos, tiene que sincronizar cada carpeta en el buzón de forma independiente. Puede usar EWS o la API administrada de EWS en su aplicación para implementar la sincronización de carpetas y elementos.
  
**Tabla 1. Operaciones de EWS y métodos de API administrada de EWS para sincronizar carpetas y elementos**

|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[Método ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[Método ExchangeService. SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
El ámbito de la sincronización que se realiza difiere en función de si es una sincronización inicial o en curso, de la siguiente manera:
  
- Una sincronización inicial sincroniza todas las carpetas o elementos del servidor con el cliente. Después de la sincronización inicial, el cliente tiene un estado de sincronización que almacena para futuras sincronizaciones. El estado de sincronización representa todos los cambios en el servidor que el servidor comunicó al cliente.
    
- Las sincronizaciones continuas sincronizan los elementos o carpetas que se han agregado, eliminado o cambiado desde la sincronización anterior. El servidor usa el estado de sincronización para calcular los cambios que se van a notificar al cliente durante cada uno de los bucles de sincronización en curso.
    
Cada operación o método de sincronización devuelve una lista de cambios, no la carpeta o el mensaje real que ha cambiado. Los cambios en los elementos y las carpetas se notifican por medio de los siguientes tipos de cambio:
  
- Crear: indica que se debe crear un nuevo elemento o una carpeta en el cliente.
    
- Actualizar: indica que se debe cambiar un elemento o una carpeta en el cliente.
    
- Eliminar: indica que un elemento o carpeta debe eliminarse en el cliente.
    
- ReadStateChange para EWS o ReadFlagChange para la API administrada de EWS: indica que el estado de lectura del elemento ha cambiado, ya sea de no leído a leído o de lectura a no leído.
    
En Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange que comienzan con Exchange 2010 SP2, los elementos y las carpetas se devuelven en orden del más reciente al más antiguo. En versiones anteriores de Exchange, los elementos y las carpetas se devuelven de más antiguo a más reciente.
  
## <a name="how-does-ews-synchronization-work"></a>¿Cómo funciona la sincronización de EWS?
<a name="bk_howdoesitwork"> </a>

En Resumen, si está sincronizando un buzón por primera vez, use el proceso como se muestra en la figura 1. Aunque puede usar otros [patrones de diseño de sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns), recomendamos este enfoque para las aplicaciones escalables.
  
**Figura 1. Modelo de diseño de sincronización inicial**

![Ilustración que muestra el patrón de diseño de la sincronización inicial. El cliente llama a SyncFolderHierarchy y Load o GetItem para obtener las carpetas y después, llama a SyncFolderItems y LoadPropertiesForItems o GetItem para obtener los elementos de cada carpeta.](media/Exchange2013_SyncInitial.png)
  
Si está usando un estado de sincronización existente en el cliente para sincronizar un buzón de correo, le recomendamos que implemente el patrón de diseño como se muestra en la figura 2. 
  
**Figura 2. Modelo de diseño de sincronización continua**

![Ilustración que muestra el patrón de diseño de la sincronización continua. Un cliente recibe una notificación y llama a SyncFolderHierarchy o SyncFolderItems, obtiene las propiedades y después, actualiza el cliente o simplemente actualiza la marca de lectura en el cliente.](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>Patrones de diseño de sincronización
<a name="bk_syncpatterns"> </a>

Puede usar uno de los dos patrones de diseño de sincronización en su aplicación para mantener sus buzones actualizados: sincronización basada en notificaciones o el método de sincronización.
  
La sincronización basada en notificaciones, tal como se muestra en la [figura 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork), se basa en notificaciones para avisar al cliente de que realice una llamada a los métodos [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) o [SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) de la API administrada de EWS o a las operaciones [SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) o [SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) de EWS. Este tipo de sincronización se suele recomendar para aplicaciones escalables, pero es posible que no sea el mejor enfoque para todos los usuarios. La sincronización basada en notificaciones tiene la siguiente ventaja: 
  
- Las notificaciones están optimizadas para reducir las llamadas a la base de datos de Exchange back-end. Las colas de eventos y las suscripciones se administran mediante el servidor de buzones (o el servidor de acceso de cliente de Exchange 2010 y Exchange 2007); sin embargo, la administración de los eventos y las suscripciones utiliza menos recursos que la alternativa, lo que hace llamadas de sincronización más frecuentes a la base de datos de Exchange. Además, Exchange tiene directivas de [limitación](ews-throttling-in-exchange.md) específicas para notificaciones y suscripciones, para proteger el consumo de recursos. 
    
Sin embargo, también hay algunas desventajas en el uso de la sincronización basada en notificaciones:
  
- Las notificaciones tienen ruido porque la mayoría de los escenarios implican varias notificaciones de un propósito del usuario. Esto es especialmente cierto en la carpeta calendario. Por ejemplo, cuando se recibe una sola convocatoria de reunión, se crean varias notificaciones de elementos y carpetas, incluida una notificación para crear el elemento y otra para modificarlo. Una forma de mitigar este inconveniente es crear un retraso de unos segundos en la llamada [Load](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx), [LoadPropertiesForItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx), [GetItem](https://msdn.microsoft.com/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)o [GetFolder](https://msdn.microsoft.com/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx) . En el caso de una convocatoria de reunión, si ha realizado llamadas a la operación **GetItem** inmediatamente, es posible que tenga una llamada para crear el elemento y otra para modificar el elemento. En su lugar, al retrasar la llamada, puede llamar a la operación **GetItem** una vez y obtener los cambios que abarcan la creación y la modificación del elemento al mismo tiempo. 
    
- Las notificaciones se ponen en cola en el servidor de buzones de correo y las suscripciones se guardan en el servidor de buzones. Si el servidor de buzones de correo que administra la suscripción no está disponible, perderá las notificaciones nuevas, el buzón no se sincronizará y tendrá que volver a suscribirse a las notificaciones.
    
- Deberá planear las estrategias de mitigación en el caso de que se produzca un error en las notificaciones. De esta forma, el segundo enfoque, el patrón de diseño de solo sincronización, es más resistente que la sincronización basada en notificaciones, ya que solo requiere que el cliente mantenga el estado de sincronización; no hay problemas con la afinidad con el servidor de buzones de correo que administra la suscripción.
    
Si se implementa como se recomienda, el patrón de diseño de la suscripción basada en notificaciones se basa en: 
  
- Notificaciones para determinar *Cuándo* se modificaron los datos. 
    
- Los métodos **SyncFolderHierarchy** o **SYNCFOLDERITEMS** de la API administrada de EWS, o las operaciones **SyncFolderHierarchy** o **SyncFolderItems** de EWS para determinar *lo que* ha cambiado, optimizando el número de eventos de sincronización devueltos. ¿Se ha creado, actualizado o eliminado un nuevo elemento? Esto es todo lo que necesita saber de estos métodos, no confíe en ellos para la lista de propiedades de los cambios. (No haga una llamada a **GetItem** o **LoadPropertiesForItems** en todos los elementos o carpetas devueltos). 
    
- Usar los métodos **Load** o **LOADPROPERTIESFORITEMS** en la API administrada de EWS, o la operación de **GetItem** de EWS para determinar *Cómo* los datos cambiaron y recuperar propiedades del servidor según sea necesario, organizando las solicitudes por lotes en función de la cantidad de datos que se devolverán. Esto va seguido de una comparación de las propiedades en el cliente y las que se devuelven desde el servidor, y en última instancia, la creación, eliminación o modificación del elemento o carpeta en el cliente. 
    
El método de sincronización solo depende completamente de los métodos de la API administrada de EWS **SyncFolderItems** y **SyncFolderHierarchy** , o de las operaciones de EWS **SyncFolderHierarchy** o **SyncFolderItems** , a las que puede llamar de forma continua o como un evento con hora. Esta opción también tiene ventajas y desventajas. El método de sincronización es más resistente porque el estado de sincronización se almacena en el cliente en el nivel de buzón y una relación única entre el estado de sincronización y cualquier servidor de buzones de correo que mantiene la suscripción de notificación no es necesaria. El método de sincronización puede sobrevivir a una conmutación por error de buzón debido a su independencia del servidor de buzones de correo. Sin embargo, el enfoque de sincronización aumenta la latencia del usuario porque los elementos se sincronizan una vez que se realiza un período de tiempo o de forma intermitente (no en tiempo real al recibir los elementos). Este enfoque también es más costoso, porque realiza llamadas a la base de datos de Exchange cuando es posible que no se hayan producido cambios. 
  
## <a name="synchronization-best-practices"></a>Procedimientos recomendados de sincronización
<a name="bk_bestpractices"> </a>

Para las aplicaciones altamente escalables, le recomendamos que aplique los siguientes procedimientos recomendados para sincronizar los buzones de la aplicación:
  
- Al llamar al método **SyncFolderItems** o **SYNCFOLDERHIERARCHY** de la API administrada de EWS, use el valor _IdOnly_ para el parámetro _PropertySet_ , o cuando use las operaciones **SyncFolderHierarchy** o **SyncFolderItems** de EWS, use el valor **IdOnly** para el valor [BaseShape](https://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) para reducir las llamadas a la base de datos de Exchange. Cuanto más propiedades solicite en el conjunto de propiedades de la llamada **SyncFolderItems** o **SyncFolderHierarchy** , se crearán más llamadas de back-end. Se realiza una nueva llamada RPC para cada valor de propiedad solicitado, mientras que solo se realiza una llamada RPC para recuperar todos los **ItemIds** de la solicitud, independientemente del número de resultados que se van a notificar. Por lo tanto, una solicitud de **IdOnly** da como resultado una llamada de base de datos, mientras que una solicitud de contenedor de propiedades para el asunto y el remitente da como resultado tres llamadas a la base de datos: una para el **asunto**, otra para el **remitente**y otra para **Itemid**.
    
- No llame a los métodos LoadPropertiesForItems **Load** o **LoadPropertiesForItems** de la API administrada de EWS, ni a las operaciones **GetItem** o **GetFolder** de EWS, en cada elemento de una respuesta de sincronización. En su lugar, analice los resultados; Busque cambios que no requieran que se recuperen todas las propiedades, como los cambios de estado de lectura. Si una respuesta incluye un cambio de estado de lectura, simplemente actualice la marca en el cliente y ya ha terminado; no es necesario obtener todas las propiedades del elemento. Y asegúrese de no duplicar el esfuerzo realizando cambios que provienen del mismo cliente. Por ejemplo, si la respuesta de sincronización incluye la eliminación de un elemento y la eliminación se produjo en el cliente local, no es necesario volver a eliminar el mensaje ni obtener todas las propiedades de ese elemento. 
    
- Para evitar obtener un límite, haga lo siguiente:
    
  - Cuando llame al método **LoadPropertiesForItems** de la API administrada de EWS o a la operación de **GetItem** de EWS para obtener los elementos de un lote, no se deben procesar demasiados elementos en la solicitud; de lo contrario, puede obtener una [limitación](ews-throttling-in-exchange.md). Se recomienda incluir 10 elementos por lote.
    
  - No realice demasiadas solicitudes en un momento muy corto. Esto también provocará una limitación y aumentará el tiempo de respuesta, en lugar de acortarlo. 
    
  - Si está procesando elementos por lotes, lote todos los elementos con los mismos valores para los atributos **ID** y **changekey** del elemento [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) . 
    
  - Si obtiene limitaciones, detenga el envío de solicitudes. Las solicitudes que se reenvíen prolongarán el esfuerzo de recuperación. En su lugar, espere a que expire el tiempo de espera y, a continuación, intente enviar de nuevo las solicitudes de sincronización.
    
- Según el tipo de evento de [notificación](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes) que se haya recibido: 
    
  - Para los eventos de **NewMail** o **Modified** , llame al método **SyncFolderItems** de la API administrada de EWS o a la operación de **SyncFolderItems** de EWS porque las notificaciones no proporcionan un **changekey**y las notificaciones no llaman a los cambios de estado de lectura.
    
  - Para los eventos **eliminados** , si la suscripción de notificación estaba activa antes de la sincronización anterior, elimine el evento localmente. No es necesario llamar al método **SyncFolderItems** de la API administrada de EWS o a la operación **SyncFolderItems** de EWS inmediatamente después de la eliminación. 
    
  - Si un evento **modificado** fue causado por un cambio de estado de lectura, no llame al método **LOADPROPERTIESFORITEMS** de la API administrada de EWS o a la operación **GetItem** de EWS; solo tiene que cambiar la marca en el elemento. 
    
- Al sincronizar datos de calendario, realice lo siguiente:
    
  - Use un método similar a la sincronización basada en notificaciones. Dado que **SyncFolderItem** no incluye ninguna lógica de calendario, use el método [FINDAPPOINTMENTS](https://msdn.microsoft.com/library/dd633767%28v=exchg.80%29.aspx) de la API administrada EWS o la [operación de FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de EWS con el elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) para ver las citas entre dos fechas y, a continuación, llame al método **LoadPropertiesForItems** de la API administrada EWS o a la operación de **GetItem** de EWS para recuperar las propiedades de elemento del elemento de calendario. 
    
  - No sondee con el método **FindAppointments** de la API administrada de EWS ni la operación **FindItem** de EWS con un elemento **CalendarView** . 
    
- Al sincronizar carpetas de búsqueda:
    
  - Use un método similar a la sincronización basada en notificaciones. 
    
  - Usar notificaciones para determinar cuándo cambian los datos.
    
  - Como no puede usar **SyncFolderItem** en una carpeta de búsqueda, use un método [FINDITEMS](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) de la API administrada de EWS ordenado y paginado, o una operación de **FindItem** de EWS con el conjunto de elementos [FractionalPageItemView](https://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) y [SortOrder](https://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) , para determinar qué ha cambiado. 
    
  - Use el método **LoadPropertiesForItems** de la API administrada de EWS o la operación de **GetItem** de EWS para recuperar datos. 
    
## <a name="filtered-synchronization"></a>Sincronización filtrada
<a name="bk_filteredsync"> </a>

El método **SyncFolderItems** de la API administrada de EWS y la operación **SyncFolderItems** de EWS permiten omitir elementos específicos en función de su ItemIds, estableciendo el parámetro _ignoreItemIds_ en la API administrada de EWS o en el elemento [Ignore](https://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx) de EWS. Esto es ideal cuando, por ejemplo, los individuos comienzan a responder a todos a un mensaje de correo electrónico que se envía a todos los usuarios de la compañía. 
  
Puede que se pregunte si se filtran las notificaciones (y, por lo tanto, solo la sincronización) si cambian las propiedades específicas. Aunque parece razonable, porque las suscripciones de notificación se basan en el tipo de cambio (crear, actualizar, eliminar) y no en la propiedad que se está actualizando, no se pueden filtrar las notificaciones de esta manera. En su lugar, puede hacer lo siguiente:
  
- Use el modelo de diseño de la suscripción basada en notificaciones.
    
- Llame repetidamente a los métodos **SyncFolderItems** y **SYNCFOLDERHIERARCHY** de la API administrada de EWS con el parámetro _propertySet_ establecido en _IdOnly_ para que su estado de sincronización sea actual. O bien, si usa EWS, llame repetidamente a las operaciones **SyncFolderHierarchy** y **SyncFolderItems** con el valor **BaseShape** establecido en **IdOnly**. 
    
- Descartar la respuesta (no la analiza ni realiza ninguna comparación de propiedades).
    
- Use el método **FindItems** de la API administrada de EWS o la operación **FindItem** de EWS y Sort and Page para rellenar previamente los elementos en el ámbito filtrado que le interesa. 
    
- Use el estado de sincronización para seguir llamando al método **SyncFolderItems** de la API administrada de EWS o a la operación de **SyncFolderItems** de EWS, pero solo supervise los cambios en el conjunto de elementos filtrados. Si se crean nuevos elementos, tendrá que ver si esos nuevos elementos están dentro del ámbito filtrado. 
    
## <a name="in-this-section"></a>En esta sección
<a name="bk_filteredsync"> </a>

- [Sincronización de carpetas mediante EWS en Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Sincronizar elementos mediante EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [Controlar errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Método SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [Método SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [Operación SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [Operación SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

