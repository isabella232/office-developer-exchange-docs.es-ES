---
title: Propiedades y propiedades extendidas de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: Descubra cómo puede definir y obtener acceso a las propiedades de los elementos y carpetas mediante el uso de EWS en Exchange.
ms.openlocfilehash: 0c01d9bd21cbef0a3536c8dbd85e192199b7b8ab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763298"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>Propiedades y propiedades extendidas de EWS en Exchange

Descubra cómo puede definir y obtener acceso a las propiedades de los elementos y carpetas mediante el uso de EWS en Exchange.
  
Un buzón de Exchange contiene un gran número de elementos, incluidos los mensajes de correo electrónico, citas, reuniones y así sucesivamente. Esos elementos se componen de propiedades; las propiedades describen los elementos. Puede usar las propiedades de elementos para realizar una [búsqueda](search-and-ews-in-exchange.md), [sincronizar los cambios de elemento](mailbox-synchronization-and-ews-in-exchange.md)y [creación de tipos de propiedad personalizada](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a). En este artículo se proporciona una introducción a las propiedades y cómo se puede trabajar con las propiedades de la aplicación.
  
## <a name="exchange-item-properties"></a>Propiedades de elementos de Exchange
<a name="ItemsAreProperties"> </a>

Elementos y carpetas de Exchange son esencialmente filas en las tablas. La propiedad principal que identifica una carpeta o elemento es su [identificador de EWS](ews-identifiers-in-exchange.md). Aunque existen otras propiedades relacionadas con el identificador de la base de datos de Exchange, para EWS, el identificador de EWS actúa como la clave principal de la colección de propiedades que describen un elemento. La propiedad de identificador EWS consta de dos partes:
  
- Una propiedad [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) o [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) que identifica el elemento 
    
- Ha cambiado una propiedad **ChangeKey** que contiene información de estado acerca de si un elemento o carpeta 
    
Todos los elementos de un buzón de correo se almacenan en la misma base de datos de Exchange y utilizan el mismo esquema de base de datos. Los elementos se distinguirán por una combinación de la propiedad [ItemClass](http://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) , restricciones de propiedad y los niveles de lógica empresarial que afectan a cómo se administran en el intercambio de almacenar. La tabla 1 muestra cómo se aplican las propiedades a través de diferentes tipos de elementos; en este ejemplo, correo electrónico y cita elementos. Ambos elementos tienen un valor para la propiedad [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) . Pero tenga en cuenta que la propiedad [IsAllDayEvent](http://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx) no está establecida en el elemento de correo electrónico, y la propiedad **IsReadReceiptRequested** no está establecida en la cita. Afortunadamente, no es necesario saber qué propiedades son aplicables para cada clase de elemento; EWS encarga de ello. 
  
**La tabla 1. Comparación de las propiedades de una cita y correo electrónico**

|**Tipo de elemento**|**Clase de artículo**|**Subject**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|Email  <br/> |IPM. Nota  <br/> |Informe de estado: completar Project X  <br/> |NULL  <br/> |true  <br/> |
|Cita  <br/> |IPM.Appointment  <br/> |Reunión de la compañía contoso  <br/> |falso  <br/> |NULL  <br/> |
   
El esquema EWS admite muchas de las restricciones administradas por la base de datos de Exchange y las capas de lógica de negocios entre EWS y la base de datos de Exchange. El esquema EWS aplica un definido un conjunto de propiedades para cada tipo de elemento. Los siguientes son los elementos de base de datos de Exchange fuertemente tipado proporcionados por EWS: 
  
- Mensajes de correo electrónico
    
- Citas
    
- Contacts
    
- Listas de distribución
    
- Mensajes de reunión
    
- Convocatoria de reunión
    
- Respuestas a la reunión
    
- Cancelaciones de reunión
    
- Tareas
    
- Elementos para exponer
    
Los elementos genéricos son devueltos por EWS como mensajes de correo electrónico. La API administrada de EWS implementa todos estos tipos de elemento.
  
> [!NOTE]
> Objetos de respuesta sólo son enviados por el cliente al servidor en respuesta a elementos recibidos de otras personas. No existen en la base de datos de Exchange. 
  
## <a name="what-are-properties-in-ews"></a>¿Cuáles son las propiedades de EWS?
<a name="WhatAreEWSProperties"> </a>

El esquema EWS describe los datos que se envían entre un cliente EWS y Exchange. Una gran parte del esquema describe las propiedades de elemento y carpeta que puede tener acceso a la base de datos de Exchange. El esquema EWS describe la representación XML de las propiedades de la base de datos de Exchange que están disponibles para su aplicación. Las propiedades reales, en cuanto a que las propiedades están disponibles, ¿qué formulario tomar y los valores que devuelven, varían en función de lo que intenta hacer. Por ejemplo, la propiedad **Body** sólo devolverá el primero 512 caracteres en una operación **FindItem** , pero la operación **GetItem** devuelve el texto completo del elemento. Aunque la mayoría de las propiedades es configurables y se puede recuperar, sólo se establecen algunas propiedades de Exchange. Cada propiedad existe en el esquema en un formato XML cualquiera refleja la propiedad tal como se almacena en la base de datos de Exchange, o se calcula a partir de las propiedades que se almacenan en la base de datos de Exchange. La propiedad **Subject** es un ejemplo de una propiedad configurable; la propiedad **UnreadCount** en una carpeta es un ejemplo de una propiedad calculada. Un conjunto básico de propiedades son comunes a los tipos de elemento principal. 
  
Los siguientes factores determinarán que la propiedad se establece que la aplicación obtiene de Exchange: 
  
- La operación que está llamando la aplicación
    
- La forma de respuesta base
    
- El tipo de elemento
    
- Las rutas de acceso especificada (propiedad)
    
Es importante comprender cómo estos distintos factores afectan a los datos que puede tener acceso. Como con el ejemplo de la propiedad **Body** mencionado anteriormente, parte de la información es condicionalmente disponible en función de diversos factores. Descripción de estos factores puede ahorrar mucho tiempo y ayudan a elegir las opciones correctas para tener acceso a la información que desee. Para descubrir las propiedades que son accesibles, debe probar estos factores para determinar cómo tener acceso a las propiedades que requiere su aplicación. En esta sección se describe cómo afectan estos factores diferentes a las propiedades que se devuelven en las respuestas EWS. 
  
### <a name="ews-response-shapes"></a>Formas de respuesta EWS

Exchange almacena una gran cantidad de información sobre los elementos. A veces, la aplicación no necesita toda la información y, en muchos casos, es mejor no obtener todo. [Las formas de respuesta EWS](property-sets-and-response-shapes-in-ews-in-exchange.md), también denominada formas de propiedad, indicar qué propiedades se devuelven desde el servidor. El elemento principal de la forma de respuesta es la forma base. Una forma de base es un contenedor de propiedades preestablecido de predeterminada para los elementos fuertemente tipados. El equivalente de la API administrada de EWS de la forma base es la [BasePropertySet](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx). EWS incluye tres formas de respuesta de forma predeterminada.
  
**Tabla 2. Formas de respuesta predeterminada**

|**Nombre predeterminado de la forma de respuesta**|**Equivalente de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|IdOnly  <br/> |Valor de BasePropertySet.IdOnly  <br/> |Se devuelven sólo el identificador de EWS y cambiar la clave. A menos que el cliente utiliza todas las propiedades devuelven por la forma AllProperties o de forma predeterminada, utilice la forma IdOnly y especificar propiedades adicionales mediante el uso de la ruta de acceso de la propiedad establecer en la clase **PropertySet** . La mayoría de las aplicaciones deben usar la forma de respuesta IdOnly con propiedades adicionales especificadas. Esto reduce la cantidad de datos no usados que se solicitan a los clientes.  <br/> |
|Default  <br/> |N/D  <br/> |Un conjunto de propiedades estándares para el tipo de elemento. Solo puede usar esta forma de respuesta si la aplicación utiliza todas las propiedades.  <br/> |
|AllProperties  <br/> |Valor de BasePropertySet.FirstClassProperties  <br/> |Un conjunto de propiedades más grande que la forma predeterminada. Aunque el nombre lo indica, esta opción no devuelve todas las propiedades en un elemento. En este conjunto de propiedades devuelve las propiedades que las aplicaciones cliente se usan con más frecuencia. Si necesita que las propiedades adicionales, se puede solicitar por su ruta de acceso de propiedad.  <br/> Si su aplicación no utiliza todas las propiedades devueltas con esta forma de respuesta, utilice la forma de respuesta IdOnly con propiedades adicionales especificadas.  <br/> |
   
Muchas operaciones de EWS devuelven elementos y sus propiedades. Independientemente de las formas de respuesta que especifique, diferentes operaciones pueden devolver conjuntos de propiedades diferentes. Diferentes tipos de elementos también devuelven distintas propiedades, dependiendo de la operación y la forma de respuesta especificado. Las siguientes operaciones de usar formas de respuesta para identificar qué propiedades se devuelven.
  
**Tabla 3. Operaciones que usan las formas de respuesta**

|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[ExchangeService.GetConversationItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Folder.Bind (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Item.Bind (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [ExchangeService.BindToItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[ExchangeService.FindConversation (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Folder.FindFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindFolders (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Folder.FindItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [ExchangeService.FindItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](http://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |No se ha implementado.  <br/> |
|[ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[ExchangeService.ResolveNames (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](http://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[ExchangeService.SearchMailboxes (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [ExchangeService.BeginSearchMailboxes (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](http://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderHierarchy (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](http://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[ExchangeService.SyncFolderItems (método)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Las formas de la propiedad son uno, rudimentaria manera para identificar las propiedades que desea que su aplicación para devolver. A veces, sin embargo, la aplicación necesita un conjunto más refinado de propiedades específicas. Para ello, puede usar la ruta de acceso de propiedad.
  
### <a name="choose-properties-by-their-property-path"></a>Elija propiedades por su ruta de acceso (propiedad)

Una ruta de acceso de la propiedad EWS es los metadatos que se usan para identificar las propiedades de una solicitud o una respuesta. 
  
**Tabla 4. Tipos de ruta de acceso (propiedad)**

|**Tipo de ruta de acceso (propiedad)**|**Tipo de esquema**|**Implementación de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |Tipos que heredan de [ServiceObjectSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx).  <br/> |La ruta de acceso de propiedad más comunes. Rutas de acceso de propiedad FieldUri se especifican en un objeto **PropertySet** en la API administrada de EWS. La mayoría de las propiedades EWS pueden especificarse por la ruta de acceso de la propiedad FieldUri. Esto se describe por la UnindexedFieldURIType en el esquema EWS.  <br/> La ruta de acceso de la propiedad FieldUri XML tiene este aspecto:  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```Esta ruta de acceso de la propiedad es el equivalente de ItemSchema.Subject en la API administrada de EWS.  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |Tipos que heredan de [ItemSchema](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx).  <br/> |Identifica las propiedades de diccionario que requieren un índice de propiedad para especificar el valor que se devolverá. Utilice esta ruta de acceso cuando una propiedad puede tener más de un valor. Esto se describe por la propiedad **DictionaryURIType** en el esquema EWS. Rutas de acceso de **DictionaryURIType** (propiedad) se especifican en un objeto **PropertySet** en la API administrada de EWS.  <br/> La ruta de acceso de la propiedad IndexedFieldUri XML tiene este aspecto:  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Identifica una definición de propiedad extendida que identifica las propiedades personalizadas o no encuentra esquematizado en los elementos.  <br/> La ruta de acceso de la propiedad ExtendedFieldUri XML tiene este aspecto:  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |Especifica las propiedades que están asociadas a un error en una respuesta EWS. Esto se describe en el tipo de **ExceptionPropertyURIType** en el esquema EWS. Esto sólo se produce en el elemento **MessageXml** de respuestas de error que se producen cuando se trabaja con patrones de periodicidad de calendario.  <br/> |
   
Como procedimiento recomendado, al solicitar propiedades, utilice la forma de base de IdOnly ([BasePropertySet.IdOnly](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) en la API administrada de EWS) y, a continuación, solicite solo las propiedades que necesita la aplicación mediante la especificación de las rutas de acceso de la propiedad. 
  
### <a name="schematized-properties"></a>Propiedades esquematizadas

La mayoría de las propiedades que necesita el cliente de EWS se describen por el esquema de EWS. La carpeta principal y las definiciones de tipo de elemento, que contienen las definiciones de propiedad, se encuentran en el esquema de types.xsd. Los siguientes tipos de esquema contienen las definiciones de propiedad para la mayoría de los objetos que se puede usar.
  
**Tabla 5. Tipos de esquema que contienen definiciones de (propiedad)**

|**Tipo de esquema EWS**|**Equivalente del tipo de API administrada de EWS**|**Define el...**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Clase de artículo](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de elemento base. Este tipo se puede crear desde un cliente pero nunca devuelto por Exchange. Exchange devuelve un objeto de tipo de mensaje para todos los objetos genéricos.  <br/> |
|**MessageType** <br/> |[Clase EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de objeto de mensaje de correo electrónico y la propiedad establecida para todos los objetos genéricos.  <br/> |
|**CalendarItemType** <br/> |[Clase de cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |Establece la propiedad del elemento de calendario; Esto incluye las citas periódicas y único.  <br/> |
|**ContactItemType** <br/> |[Clase de contacto](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de elemento de contacto.  <br/> |
|**DistributionListType** <br/> |[Clase ContactGroup](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de la lista de distribución personal.  <br/> |
|**MeetingMessageType** <br/> |[Clase MeetingMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |Establece la propiedad de tipo de mensaje de la reunión.  <br/> |
|**MeetingRequestMessageType** <br/> |[Clase MeetingRequest](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de solicitud de reunión.  <br/> |
|**MeetingResponseMessageType** <br/> |[Clase de MeetingResponse](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |Establece la propiedad de tipo de respuesta de la reunión.  <br/> |
|**MeetingCancellationMessageType** <br/> |[Clase MeetingCancellation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |Establece la propiedad type de cancelación de la reunión.  <br/> |
|**TaskType** <br/> |[Clase de la tarea](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de tarea.  <br/> |
|**PostItemType** <br/> |[Clase postItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo PostItem.  <br/> |
|**FolderType** <br/> |[Clase de carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de carpeta.  <br/> |
|**CalendarFolderType** <br/> |[Clase CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo SearchFolder.  <br/> |
|**ContactsFolderType** <br/> |[Clase ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo ContactsFolder.  <br/> |
|**SearchFolderType** <br/> |[Clase SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo SearchFolder.  <br/> |
|**TasksFolderType** <br/> |[Clase TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo TasksFolder.  <br/> |
|**UserConfigurationType** <br/> |[Clase UserConfiguration](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo UserConfiguration.  <br/> |
   
Si bien las propiedades en el esquema EWS son suficientes para muchas aplicaciones, no se puede implementar algunos escenarios utilizando sólo lo que se describe en el esquema. En estos casos, puede propiedades extendidas. 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>Propiedades extendidas (también conocido como no encuentra esquematizado propiedades)

Las propiedades extendidas permiten crear propiedades personalizadas, que proporcionan acceso a las propiedades de los elementos y carpetas en el almacén de Exchange que no están definidas en el esquema EWS. Puede usarlas para tener acceso a las propiedades de elemento y carpeta MAPI nativas en la base de datos de Exchange. Puede usar las propiedades extendidas para tener acceso a todas las propiedades esquematizadas, debido a que en realidad, esas propiedades esquematizadas no son más que las propiedades MAPI en la base de datos de Exchange. 
  
El tipo de esquema PathToExtendedFieldType, que se encuentra en el esquema types.xsd, define el XML que representa una propiedad extendida. Este tipo de esquema define el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) en instancias XML; en otras palabras, define el XML que se envía entre el servicio y el cliente. El tipo de esquema de ExtendedPropertyType define el elemento [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) y el valor o matriz de valores que contiene una propiedad extendida. En la siguiente tabla se muestra la asignación aproximada de la propiedad extendida XML y cómo se implementa en los elementos de la API administrada de EWS. 
  
**Tabla 6. Propiedad extendida XML tal como se implementa en la API administrada de EWS**

|**Implementación de la API administrada de EWS**|**¿Qué contiene**|**¿Qué asigna a**|
|:-----|:-----|:-----|
|[Item.ExtendedProperties (propiedad)](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |Una colección de las propiedades extendidas en un elemento.  <br/> |Una o más instancias de las propiedades extendidas en un elemento.  <br/> |
|[Clase ExtendedProperty](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |La definición de la propiedad extendida y valores.  <br/> |El tipo de esquema ExtendedPropertyType.  <br/> |
|[Clase ExtendedPropertyDefinition](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Una definición de propiedad extendida.  <br/> |El tipo de esquema PathToExtendedFieldType.  <br/> |
   
Si desea obtener más información acerca de cómo puede utilizar las propiedades extendidas en la aplicación, puede explorar los ejemplos de código siguientes: 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013: Aprovisionar encabezados X personalizados mediante programación](http://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013: Obtener acceso a una propiedad por su etiqueta (propiedad)](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013: Acceso a una propiedad con nombre mediante su identificador](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013: Obtener acceso a una propiedad con nombre por su nombre](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013: Obtener acceso a un nombre y el GUID del conjunto de propiedad por propiedad](http://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013: Crear personalizados mediante programación las propiedades extendidas](http://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Encabezados x de aprovisionamiento mediante el uso de EWS en Exchange](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [Errores relacionados con la propiedad EWS](ews-property-related-errors.md)
    
## <a name="see-also"></a>Ver también


- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

