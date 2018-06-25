---
title: Sincronización de buzón de correo y EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: decf1eee-9743-44f3-9333-b3a01af3683e
description: Obtenga información acerca de cómo funciona la sincronización de buzón de correo cuando se usa EWS para tener acceso a Exchange.
ms.openlocfilehash: 7bca2f7b754dcceee99e4bc24519f6e4f6423ae7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763219"
---
# <a name="mailbox-synchronization-and-ews-in-exchange"></a>Sincronización de buzón de correo y EWS en Exchange

Obtenga información acerca de cómo funciona la sincronización de buzón de correo cuando se usa EWS para tener acceso a Exchange.
  
EWS en Exchange usa dos tipos de sincronización para recuperar contenido de los buzones y los cambios en el contenido del buzón:
  
- Sincronización de carpetas
    
- Sincronización de elementos
    
En este artículo, obtendrá información sobre los tipos de sincronización, cómo funciona la sincronización, modelos de diseño de la sincronización y procedimientos recomendados de sincronización.
  
## <a name="folder-and-item-synchronization"></a>Sincronización de carpetas y elementos
<a name="bk_typesofsyncs"> </a>

Sincronización de carpetas sincroniza una estructura de carpetas, o la jerarquía de carpetas. Sincronización de elementos sincroniza los elementos dentro de una carpeta. Cuando se sincronizan los artículos, se debe sincronizar cada carpeta en el buzón de forma independiente. Puede utilizar EWS o la API administrada de EWS en su aplicación para implementar carpeta y sincronización de elemento.
  
**La tabla 1. Las operaciones de EWS y métodos de la API administrada de EWS para sincronizar las carpetas y elementos**

|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
El ámbito de la sincronización que se produce es diferente dependiendo de si es un inicial o una sincronización continuada, como se indica a continuación:
  
- Una sincronización inicial sincroniza todas las carpetas o elementos en el servidor al cliente. Después de la sincronización inicial, el cliente tiene un estado de sincronización que almacena para futuras sincronizaciones. El estado de sincronización representa todos los cambios en el servidor que el servidor se comunica al cliente.
    
- Las sincronizaciones del curso sincronización los elementos o carpetas que se han agregado, eliminadas o cambiado desde la última sincronización. El servidor usa el estado de sincronización para calcular los cambios para informar al cliente durante cada uno de los bucles de sincronización en proceso.
    
Cada método de sincronización o la operación devuelve una lista de los cambios, no la carpeta real o un mensaje que ha cambiado. Se informa de los cambios realizados en los elementos y las carpetas por medio de los siguientes tipos de cambio:
  
- Crear: Indica que se debe crear un nuevo elemento o una carpeta en el cliente.
    
- Update: Indica que se debe cambiar una carpeta o elemento en el cliente.
    
- Eliminar: Indica que se debe eliminar una carpeta o elemento en el cliente.
    
- ReadStateChange para EWS o ReadFlagChange para la API administrada de EWS: indica que el estado del elemento ha cambiado, ya sea de no leído para leer o lectura a no leídos.
    
En Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de con Service Pack 2 de Exchange 2010, los elementos y las carpetas se devuelven en orden del más reciente al más antiguo. En las versiones anteriores de Exchange, se devuelven los elementos y carpetas desde la más antigua a más reciente.
  
## <a name="how-does-ews-synchronization-work"></a>¿Cómo funciona la sincronización de EWS?
<a name="bk_howdoesitwork"> </a>

En resumen, si sincroniza un buzón de correo por primera vez, use el proceso tal como se muestra en la figura 1. Aunque puede usar otros [patrones de diseño de la sincronización](mailbox-synchronization-and-ews-in-exchange.md#bk_syncpatterns), se recomienda este enfoque para aplicaciones escalables.
  
**En la figura 1. Modelo de diseño de la sincronización inicial**

![Ilustración que muestra el patrón de diseño de la sincronización inicial. El cliente llama a SyncFolderHierarchy y Load o GetItem para obtener las carpetas y después, llama a SyncFolderItems y LoadPropertiesForItems o GetItem para obtener los elementos de cada carpeta.](media/Exchange2013_SyncInitial.png)
  
Si utiliza un estado de sincronización existente en el cliente para sincronizar un buzón de correo, se recomienda implementar el modelo de diseño tal como se muestra en la figura 2. 
  
**La figura 2. Modelo de diseño de la sincronización actual**

![Ilustración que muestra el patrón de diseño de la sincronización continua. Un cliente recibe una notificación y llama a SyncFolderHierarchy o SyncFolderItems, obtiene las propiedades y después, actualiza el cliente o simplemente actualiza la marca de lectura en el cliente.](media/Exchange2013_Sync_Ongoing.png)
  
## <a name="synchronization-design-patterns"></a>Modelos de diseño de la sincronización
<a name="bk_syncpatterns"> </a>

Puede usar uno de los dos modelos de diseño de sincronización en la aplicación para mantener actualizados los buzones de correo: sincronización de notificación, o el método de sincronización.
  
Sincronización basada en notificación, tal como se ilustra en [la figura 2](mailbox-synchronization-and-ews-in-exchange.md#bk_howdoesitwork), se basa en notificaciones para el cliente para realizar una llamada a los métodos de la API administrada de EWS [SyncFolderItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) o [SyncFolderHierarchy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) o la dirección URL de EWS [SyncFolderHierarchy de alerta ](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)o [SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) operaciones. Por lo general se recomienda este tipo de sincronización para aplicaciones escalables, pero podría no ser el mejor enfoque para todos los usuarios. Sincronización de notificación tiene la ventaja de la siguiente: 
  
- Las notificaciones están optimizadas para reducir las llamadas a la base de datos de Exchange de back-end. Las suscripciones y las colas de evento son administradas por el servidor de buzones (o el servidor de acceso de cliente de Exchange 2010 y Exchange 2007); Sin embargo, la administración de los eventos y las suscripciones utiliza menos recursos que la alternativa, que es más frecuentes de las llamadas de sincronización a la base de datos de Exchange. Además, Exchange tiene específicos de [las directivas de limitación](ews-throttling-in-exchange.md) para que las notificaciones y suscripciones proteger el consumo de recursos. 
    
Sin embargo, también hay inconvenientes usa la sincronización de notificación:
  
- Las notificaciones son ruidosas debido a que la mayoría de los escenarios implica varias notificaciones de la intención de un usuario. Esto es especialmente así de la carpeta Calendario. Por ejemplo, cuando se recibe una convocatoria de reunión única, se crean varias notificaciones de elemento y carpeta, incluida una notificación para crear el elemento y otro para modificar el elemento. Una forma de mitigar este inconveniente es crear un retraso de unos segundos en la llamada de [carga](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobject.load%28v=exchg.80%29.aspx), [LoadPropertiesForItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.loadpropertiesforitems%28v=exchg.80%29.aspx), [GetItem](http://msdn.microsoft.com/en-us/library/exchange/aa565934%28v=exchg.150%29.aspx.aspx)o [GetFolder](http://msdn.microsoft.com/en-us/library/exchange/aa580274%28v=exchg.150%29.aspx.aspx) . En el caso de una convocatoria de reunión, si se han realizado las llamadas a la operación **GetItem** inmediatamente, puede que tenga una llamada para crear el elemento y otro para modificar el elemento. En su lugar, retrasar la llamada, puede llamar a la operación **GetItem** una vez y obtener los cambios que abarcan la creación y la modificación del elemento al mismo tiempo. 
    
- Las notificaciones se ponen en cola en el servidor de buzón de correo y las suscripciones se guardan en el servidor de buzón de correo. Si el servidor de buzones que administra la suscripción no está disponible, se pierden cualquier nuevas notificaciones, no sincronizar su buzón de correo y tendrá que volver a suscribirse a las notificaciones.
    
- Debe planear las estrategias de mitigación en caso de que se producirá un error en las notificaciones. De este modo, el segundo enfoque, el modelo de diseño solo sincronización, es más resistente que la sincronización basada en notificación, debido a que sólo requiere que el cliente de mantener el estado de sincronización: no hay ningún problema con afinidad con el servidor de buzones administración de la suscripción.
    
Si se implementa como se recomienda, el modelo de diseño basada en notificación de suscripción se basa en: 
  
- Notificaciones para determinar *cuándo* ha cambiado los datos. 
    
- La API administrada de EWS **SyncFolderHierarchy** o métodos **SyncFolderItems** , o el EWS **SyncFolderHierarchy** **SyncFolderItems** operaciones para determinar *qué* cambiar o, la optimización del número de eventos de sincronización devueltos. ¿Era un nuevo elemento crea, actualiza o elimina? Eso es todo lo que necesita saber de estos métodos, no se basan en ellos para la lista de propiedades de los cambios. (No se hace una llamada de **LoadPropertiesForItems** en todos los elementos o carpetas devueltos o **GetItem** ). 
    
- Uso de los métodos de **carga** o **LoadPropertiesForItems** en la API administrada de EWS, o la operación de EWS **GetItem** para determinar *cómo* los datos ha cambiado y para recuperar las propiedades desde el servidor según sea necesario, organizar solicitudes por lotes en función de en la cantidad de datos que se devolverán. Esto es seguido de una comparación de las propiedades en el cliente y los acaba devueltos desde el servidor y, finalmente, la creación, eliminación o modificación del elemento o la carpeta en el cliente. 
    
El método de sincronización depende completamente los métodos **SyncFolderItems** y la API administrada de EWS **SyncFolderHierarchy** , o el **SyncFolderHierarchy** o **SyncFolderItems** EWS operaciones, que puede llamar a ya sea continuamente, o como un evento con hora. Existen ventajas e inconvenientes de esta opción también. El método de sincronización es más resistente debido a que el estado de sincronización se almacena en el cliente en el nivel de buzón de correo y una relación única entre el estado de sincronización y cualquier el servidor de buzón de correo que se mantiene la suscripción de notificación no es necesario. El enfoque de sincronización puede sobrevivir a un buzón de correo de conmutación por error debido a su independencia desde el servidor de buzón de correo. Sin embargo, el método de sincronización aumenta la latencia para el usuario debido a que los elementos se sincronizan de forma intermitente o programada, no en tiempo de real cuando se reciben elementos. Este enfoque también es más costosa, debido a que está realizando llamadas a la base de datos de Exchange cuando es posible que no ha habido cambios. 
  
## <a name="synchronization-best-practices"></a>Procedimientos recomendados de sincronización
<a name="bk_bestpractices"> </a>

Para las aplicaciones altamente escalables, se recomienda que se aplican los siguientes procedimientos recomendados para sincronizar los buzones en su aplicación:
  
- Cuando una llamada al método de la API administrada de EWS **SyncFolderItems** o **SyncFolderHierarchy** usa el valor de _IdOnly_ para el parámetro _propertySet_ , o cuando se usa la dirección URL de EWS **SyncFolderHierarchy** o **SyncFolderItems** operaciones de usar el valor de **IdOnly** para el valor de [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) para reducir las llamadas a la base de datos de Exchange. Llamar a las propiedades más solicitudes en el conjunto de propiedades de la **SyncFolderItems** o **SyncFolderHierarchy** , el back-end más se crean las llamadas. Se realiza una llamada RPC nuevo para cada valor de la propiedad solicitada, mientras que se realiza sólo una llamada RPC para recuperar todos los el **ItemID** para una solicitud - independientemente del lugar en el número de resultados para el informe. Por lo que produce una solicitud de **IdOnly** en llamada de una base de datos, mientras que los resultados de una solicitud de contenedor de propiedad para el asunto y el remitente en tres llamadas de base de datos: uno para el **asunto**, uno para el **remitente**y otro para el **ItemId**.
    
- No llame a los métodos de la API administrada de EWS **carga** o **LoadPropertiesForItems** , o el EWS **GetItem** **GetFolder** operaciones o, en todos los elementos de una respuesta de sincronización. En su lugar, analizar los resultados; like se busca los cambios que no requieren todas las propiedades que se recuperarán, lea los cambios de estado. Si una respuesta incluye un cambio de estado de lectura, simplemente actualice la marca en el cliente y haya terminado; no es necesario para obtener todas las propiedades del elemento. Y asegúrese de que no duplica el esfuerzo mediante la realización de los cambios que se ha originado desde el mismo cliente. Por ejemplo, si la respuesta de sincronización incluye la eliminación de un elemento y la eliminación ha ocurrido en el cliente local, no es necesario eliminar el mensaje de nuevo u obtener todas las propiedades para ese elemento. 
    
- Evitar la introducción reducidas, haciendo lo siguiente:
    
  - Cuando se llama al método de la API administrada de EWS **LoadPropertiesForItems** o la operación de EWS **GetItem** para obtener los elementos de un lote, no por lotes demasiados elementos en la solicitud; de lo contrario, es posible que obtenga [reducidas](ews-throttling-in-exchange.md). Se recomienda que incluya 10 elementos por lote.
    
  - No se realiza demasiadas solicitudes en muy poco tiempo. Esto se también provocar limitación y aumentar el tiempo de respuesta, en lugar de acortarlo. 
    
  - Si el procesamiento por lotes de elementos, por lotes de todos los elementos con los mismos valores para los atributos **Id** y **ChangeKey** del elemento [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) . 
    
  - Si limita a obtener, dejar de enviar las solicitudes. Volver a enviar solicitudes va a prolongar los esfuerzos de recuperación. En su lugar, espere a que la devolución de tiempo a punto de caducar y, a continuación, intente volver a enviar las solicitudes de sincronización.
    
- Según el tipo de [evento de notificación](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_eventtypes) recibido: 
    
  - Para los eventos **NewMail** o **modificado** , llame al método de la API administrada de EWS **SyncFolderItems** o la operación de EWS **SyncFolderItems** debido a que las notificaciones no proporcionan un **ChangeKey**y el estado de lectura no llame a las notificaciones cambios.
    
  - Para los eventos de **Deleted** , si la suscripción de notificación estaba activa antes de la sincronización anterior, simplemente elimine el evento localmente. No es necesario llamar al método de la API administrada de EWS **SyncFolderItems** o la operación de EWS **SyncFolderItems** inmediatamente después de la eliminación. 
    
  - Si se produjo un evento **modificado** por un cambio de estado de lectura, no llame al método de la API administrada de EWS **LoadPropertiesForItems** o la operación de EWS **GetItem** , sólo debe cambiar la marca en el elemento. 
    
- Cuando se sincroniza los datos del calendario, realice lo siguiente:
    
  - Usa un enfoque similar a la sincronización de notificación. Debido a que **SyncFolderItem** no incluye ninguna lógica de calendario, use el método de la API administrada de EWS [FindAppointments](http://msdn.microsoft.com/en-us/library/dd633767%28v=exchg.80%29.aspx) , o la [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) EWS con el elemento [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) para ver citas entre dos fechas y, a continuación, Llame al método de la API administrada de EWS **LoadPropertiesForItems** , o la operación de EWS **GetItem** para recuperar las propiedades de elemento para el elemento de calendario. 
    
  - No hay sondeo utilizando el método de la API administrada de EWS **FindAppointments** , o la operación de EWS **FindItem** con un elemento **CalendarView** . 
    
- Al sincronizar las carpetas de búsqueda:
    
  - Usa un enfoque similar a la sincronización de notificación. 
    
  - Usar notificaciones para determinar cuando cambian los datos.
    
  - Debido a que no se puede usar **SyncFolderItem** en una carpeta de búsqueda, use una operación de EWS **FindItem** o método de API administrada de EWS [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) ordenado y paginado con el conjunto de elemento [FractionalPageItemView](http://msdn.microsoft.com/library/4111afec-35e7-4c6f-b291-9bbba603f633%28Office.15%29.aspx) y [SortOrder](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) , para determinar ¿Qué ha cambiado. 
    
  - Utilice el método de la API administrada de EWS **LoadPropertiesForItems** o la operación de EWS **GetItem** para recuperar datos. 
    
## <a name="filtered-synchronization"></a>Sincronización filtrada
<a name="bk_filteredsync"> </a>

El método de la API administrada de EWS **SyncFolderItems** y la operación de EWS **SyncFolderItems** permiten omitir elementos específicos, según sus ItemID, estableciendo el parámetro _ignoreItemIds_ en la API administrada de EWS o el [Omitir](http://msdn.microsoft.com/library/7789eec5-ceec-43f2-84d5-d0d15b734076%28Office.15%29.aspx) elemento de EWS. Esto es ideal cuando, por ejemplo, las personas empiezan a responder a un mensaje de correo electrónico enviado a todos los usuarios de la compañía todos los. 
  
Puede que se pregunte, ¿puedo filtrar notificaciones de mi (y, por tanto, sólo se desencadenan sincronización) si cambian propiedades específicas? Aunque parece razonable, debido a que las suscripciones de notificación se basan en el tipo de cambio (crear, actualizar, eliminar), y no la propiedad que se está actualizando, no se puede filtrar las notificaciones de esta forma. En su lugar, puede hacer lo siguiente:
  
- Usar el modelo de diseño basada en notificación de suscripción.
    
- Llamar a la API administrada de EWS **SyncFolderItems** y **SyncFolderHierarchy** métodos repetidamente con el parámetro de _propertySet_ establecido en _IdOnly_ para que su estado de sincronización actual. O si el uso de EWS, llame a las operaciones de **SyncFolderItems** y **SyncFolderHierarchy** repetidamente con el valor de **BaseShape** establecido en **IdOnly**. 
    
- Descartar la respuesta (no analizarlo o hacer cualquier propiedad comparaciones).
    
- Use el método de la API administrada de EWS **FindItems** o la operación de EWS **FindItem** y ordenar y página para rellenar automáticamente los elementos en el ámbito filtrado que le interesa. 
    
- Use su estado de sincronización para seguir llame al método de la API administrada de EWS **SyncFolderItems** o la operación de EWS **SyncFolderItems** , pero sólo supervisar los cambios en el conjunto de elementos filtrados. Si se crean nuevos elementos, debe ver si esos elementos están dentro de su ámbito filtrado. 
    
## <a name="in-this-section"></a>En esta sección
<a name="bk_filteredsync"> </a>

- [Sincronizar carpetas mediante el uso de EWS en Exchange](how-to-synchronize-folders-by-using-ews-in-exchange.md)
    
- [Sincronizar elementos mediante el uso de EWS en Exchange](how-to-synchronize-items-by-using-ews-in-exchange.md)
    
- [Tratamiento de errores relacionados con la sincronización en EWS en Exchange](handling-synchronization-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [SyncFolderItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx)
    
- [SyncFolderHierarchy (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx)
    
- [Operación SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx)
    
- [Operación SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx)
    

