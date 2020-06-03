---
title: Propiedades y propiedades extendidas de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 68623048-060e-4602-b3fa-62617a94cf72
description: Descubra cómo puede definir y tener acceso a las propiedades de elementos y carpetas mediante EWS en Exchange.
localization_priority: Priority
ms.openlocfilehash: 0891cf6d6dddf74518fbbc8efbaebdd8eb0c706b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459338"
---
# <a name="properties-and-extended-properties-in-ews-in-exchange"></a>Propiedades y propiedades extendidas de EWS en Exchange

Descubra cómo puede definir y tener acceso a las propiedades de elementos y carpetas mediante EWS en Exchange.
  
Un buzón de Exchange contiene un gran número de elementos, incluidos los mensajes de correo electrónico, citas, reuniones, etc. Estos elementos se componen de propiedades; las propiedades describen los elementos. Puede usar propiedades de elemento para realizar una [búsqueda](search-and-ews-in-exchange.md), [sincronizar cambios de elementos](mailbox-synchronization-and-ews-in-exchange.md)y [crear tipos de propiedades personalizadas](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a). En este artículo se proporciona información general sobre las propiedades y cómo se puede trabajar con propiedades en la aplicación.
  
## <a name="exchange-item-properties"></a>Propiedades de elemento de Exchange
<a name="ItemsAreProperties"> </a>

Los elementos y las carpetas de Exchange son esencialmente filas en tablas. La propiedad principal que identifica un elemento o una carpeta es su [identificador EWS](ews-identifiers-in-exchange.md). Aunque hay otras propiedades relacionadas con el identificador en la base de datos de Exchange, para EWS, el identificador de EWS actúa como la clave principal para la colección de propiedades que describen un elemento. La propiedad de identificador de EWS contiene dos partes:
  
- Propiedad [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) o [FolderId](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) que identifica el elemento. 
    
- Una propiedad **changekey** que contiene información de estado sobre si un elemento o una carpeta ha cambiado 
    
Todos los elementos de un buzón de correo se almacenan en la misma base de datos de Exchange y usan el mismo esquema de base de datos. Los elementos se distinguen por una combinación de la propiedad [ItemClass](https://msdn.microsoft.com/library/56020078-50b4-4880-894a-a9f234033cfb%28Office.15%29.aspx) , las restricciones de propiedad y las capas de lógica empresarial que afectan al modo en que se administran en el almacén de Exchange. La tabla 1 muestra cómo se aplican las propiedades en distintos tipos de elementos; en este ejemplo, los elementos de correo electrónico y cita. Ambos elementos tienen un valor para la propiedad [Subject](https://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) . Pero tenga en cuenta que la propiedad [IsAllDayEvent](https://msdn.microsoft.com/library/29140a64-9d7a-4a14-a10d-c98197c9831b%28Office.15%29.aspx) no está establecida en el elemento de correo electrónico, y la propiedad **IsReadReceiptRequested** no está establecida en la cita. Afortunadamente, no es necesario saber qué propiedades son aplicables para cada clase de elemento; EWS controla esto por usted. 
  
**Tabla 1. Comparación de las propiedades de citas y correo electrónico**

|**Tipo de elemento**|**Clase Item**|**Asunto**|**IsAllDayEvent**|**IsReadReceiptRequested**|
|:-----|:-----|:-----|:-----|:-----|
|Correo electrónico  <br/> |IPM.Note  <br/> |Informe de estado: proyecto X completado  <br/> |QUE  <br/> |true  <br/> |
|Cita  <br/> |IPM.Appointment  <br/> |Reunión de la compañía contoso  <br/> |false  <br/> |QUE  <br/> |
   
El esquema EWS admite muchas de las restricciones administradas por la base de datos de Exchange y las capas de lógica empresarial entre EWS y la base de datos de Exchange. El esquema EWS aplica un conjunto de propiedades definido para cada tipo de elemento. A continuación se muestran los elementos de la base de datos de Exchange con establecimiento inflexible de tipos proporcionados por EWS: 
  
- Mensajes de correo electrónico
    
- Citas
    
- Contactos
    
- Listas de distribución
    
- Mensajes de reunión
    
- Convocatorias de reunión
    
- Respuestas a la reunión
    
- Cancelaciones de reunión
    
- Tareas
    
- Elementos para exponer
    
EWS devuelve los elementos genéricos como mensajes de correo electrónico. La API administrada de EWS implementa todos estos tipos de elementos.
  
> [!NOTE]
> Los objetos de respuesta solo los envía el cliente al servidor en respuesta a los elementos recibidos de otras personas. No existen en la base de datos de Exchange. 
  
## <a name="what-are-properties-in-ews"></a>¿Qué son las propiedades de EWS?
<a name="WhatAreEWSProperties"> </a>

El esquema EWS describe los datos que se envían entre un cliente EWS y Exchange. Una gran parte del esquema describe las propiedades de elementos y carpetas a las que puede tener acceso en la base de datos de Exchange. El esquema EWS describe la representación XML de las propiedades de la base de datos de Exchange que están disponibles para la aplicación. Las propiedades reales, en cuanto a qué propiedades están disponibles, qué formulario toman y los valores que devuelven, varían en función de lo que se intenta hacer. Por ejemplo, la propiedad **Body** solo devolverá los primeros 512 caracteres en una operación **FindItem** , pero la operación **GetItem** devuelve el texto completo del elemento. Aunque la mayoría de las propiedades se pueden establecer y recuperar, algunas propiedades solo las establece Exchange. Cada propiedad existe en el esquema en un formato XML que refleja la propiedad tal como está almacenada en la base de datos de Exchange o se calcula a partir de las propiedades almacenadas en la base de datos de Exchange. La propiedad **Subject** es un ejemplo de una propiedad configurable; la propiedad **UnreadCount** de una carpeta es un ejemplo de una propiedad calculada. Un conjunto básico de propiedades es común a los tipos de elemento principales. 
  
Los siguientes factores determinan el conjunto de propiedades que la aplicación obtiene de Exchange: 
  
- La operación a la que llama la aplicación
    
- La forma base de respuesta
    
- El tipo de elemento
    
- Las rutas de propiedades especificadas
    
Es importante comprender cómo estos distintos factores afectan a los datos a los que puede tener acceso. Como en el ejemplo de la propiedad **Body** mencionada anteriormente, parte de la información está disponible de forma condicional en función de diversos factores. Comprender estos factores puede ahorrarle tiempo al ayudarle a elegir las opciones correctas para obtener acceso a la información que desea. Para detectar las propiedades a las que se puede tener acceso, deberá probar estos factores para determinar cómo tener acceso a las propiedades que necesita la aplicación. En esta sección se describe cómo afectan estos distintos factores a las propiedades que se devuelven en las respuestas de EWS. 
  
### <a name="ews-response-shapes"></a>Formas de respuesta de EWS

Exchange almacena mucha información sobre los elementos. A veces, la aplicación no necesita toda la información y, en muchos casos, es mejor no obtenerla. Las [formas de respuesta de EWS](property-sets-and-response-shapes-in-ews-in-exchange.md), también denominadas formas de propiedad, indican las propiedades que se devuelven del servidor. El elemento principal de la forma respuesta es la forma base. Una forma base es un contenedor de propiedades preestablecido predeterminado para los elementos fuertemente tipados. El equivalente de la API administrada de EWS de la forma base es [BasePropertySet](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx). EWS incluye tres formas de respuesta predeterminadas.
  
**Tabla 2. Formas de respuesta predeterminadas**

|**Nombre de forma de respuesta predeterminado**|**Equivalente de API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|
|IdOnly  <br/> |Valor BasePropertySet. IdOnly  <br/> |Solo se devuelven el identificador de EWS y la clave de cambio. A menos que el cliente use todas las propiedades devueltas por la AllProperties o la forma predeterminada, use la forma IdOnly y especifique las propiedades adicionales mediante el uso de la ruta de acceso de propiedad establecida en la clase **PropertySet** . La mayoría de las aplicaciones deben usar la forma respuesta IdOnly con propiedades adicionales especificadas. Esto reduce la cantidad de datos sin usar que solicitan los clientes.  <br/> |
|Predeterminado  <br/> |N/D  <br/> |Un conjunto de propiedades estándar para el tipo de elemento. Use esta forma de respuesta solo si la aplicación usa todas las propiedades.  <br/> |
|AllProperties  <br/> |Valor BasePropertySet. FirstClassProperties  <br/> |Un conjunto mayor de propiedades que la forma predeterminada. Aunque el nombre lo implica, esta opción no devuelve todas las propiedades de un elemento. Este conjunto de propiedades devuelve las propiedades que las aplicaciones cliente usan con más frecuencia. Si necesita propiedades adicionales, puede solicitarlas por su ruta de acceso de propiedad.  <br/> Si la aplicación no usa todas las propiedades devueltas con esta forma de respuesta, use la forma respuesta IdOnly con propiedades adicionales especificadas.  <br/> |
   
Muchas operaciones de EWS devuelven elementos y sus propiedades. Independientemente de las formas de respuesta que especifique, las distintas operaciones pueden devolver distintos conjuntos de propiedades. Los diferentes tipos de elemento también devuelven diferentes propiedades, según la operación y la forma de respuesta que se especifique. Las siguientes operaciones utilizan formas de respuesta para identificar las propiedades que se van a devolver.
  
**Tabla 3. Operaciones que usan formas de respuesta**

|**Operación de EWS**|**Método de la API administrada de EWS**|
|:-----|:-----|
|[GetConversationItems](https://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |[Método ExchangeService. GetConversationItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |
|[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> |[Método Folder. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> |
|[GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> |[Método Item. bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Método ExchangeService. BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |
|[FindConversation](https://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |[Método ExchangeService. FindConversation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |
|[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |[Método Folder. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) <br/> [Método ExchangeService. FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |
|[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |[Método Folder. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> [Método ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) <br/> |
|[FindPeople](https://msdn.microsoft.com/library/446106b7-ff2d-4107-90c1-29f4d38ba128%28Office.15%29.aspx) <br/> |No implementado.  <br/> |
|[ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) <br/> |[Método ExchangeService. ResolveNames](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) <br/> |
|[SearchMailboxes](https://msdn.microsoft.com/library/8a67c1d8-d021-4e68-aa62-35f7d9c2edc7%28Office.15%29.aspx) <br/> |[Método ExchangeService. SearchMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.searchmailboxes%28v=exchg.80%29.aspx) <br/> [Método ExchangeService. BeginSearchMailboxes](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.beginsearchmailboxes%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) <br/> |[Método ExchangeService. SyncFolderHierarchy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) <br/> |
|[SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) <br/> |[Método ExchangeService. SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) <br/> |
   
Las formas de propiedad son una forma rudimentaria de identificar las propiedades que desea que devuelva la aplicación. Sin embargo, a veces la aplicación necesita un conjunto más refinado de propiedades específicas. Para esto, puede usar la ruta de acceso de la propiedad.
  
### <a name="choose-properties-by-their-property-path"></a>Elegir propiedades por su ruta de acceso de propiedad

Una ruta de acceso de propiedad de EWS son los metadatos que se usan para identificar propiedades en una solicitud o respuesta. 
  
**Tabla 4. Tipos de ruta de acceso de propiedad**

|**Tipo de ruta de acceso de propiedad**|**Tipo de esquema**|**Implementación de la API administrada de EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|FieldUri  <br/> |PathToUnindexedFieldType  <br/> |Tipos que heredan de [ServiceObjectSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceobjectschema%28v=exchg.80%29.aspx).  <br/> |La ruta de acceso de propiedad más común. Las rutas de la propiedad FieldUri se especifican en un objeto **PropertySet** en la API administrada de EWS. La mayoría de las propiedades de EWS se pueden especificar mediante la ruta de acceso de propiedad FieldUri. Esto lo describe la UnindexedFieldURIType en el esquema EWS.  <br/> El XML de la ruta de acceso de la propiedad FieldUri tiene el siguiente aspecto:  <br/> ```XML<FieldURI FieldURI="item:Subject"/>```Esta ruta de acceso de propiedad es el equivalente a ItemSchema. Subject en la API administrada EWS.  <br/> |
|IndexedFieldUri  <br/> |PathToIndexedFieldType  <br/> |Tipos que heredan de [ItemSchema](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.itemschema%28v=exchg.80%29.aspx).  <br/> |Identifica las propiedades de diccionario que requieren un índice de propiedad para especificar el valor que se va a devolver. Use esta ruta de acceso cuando una propiedad pueda tener más de un valor. Esto se describe en la propiedad **DictionaryURIType** del esquema EWS. Las rutas de la propiedad **DictionaryURIType** se especifican en un objeto **PROPERTYSET** en la API administrada de EWS.  <br/> El XML de la ruta de acceso de la propiedad IndexedFieldUri tiene el siguiente aspecto:  <br/> ```XML<IndexedFieldURI FieldURI="contacts:PhysicalAddress:Street FieldIndex="Home"/>```|
|ExtendedFieldUri  <br/> |PathToExtendedFieldType  <br/> |[ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Identifica una definición de propiedad extendida que identifica propiedades personalizadas o que no son de esquematizado en elementos.  <br/> El XML de la ruta de acceso de la propiedad ExtendedFieldUri tiene el siguiente aspecto:  <br/> ```XML<ExtendedFieldURI> PropertyTag="0x1234" PropertyType="Integer" />```|
|ExceptionFieldUri  <br/> |ExceptionFieldURI  <br/> |[ServiceResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse%28v=exchg.80%29.aspx) <br/> |Especifica las propiedades que están asociadas a un error en una respuesta de EWS. Esto se describe mediante el tipo **ExceptionPropertyURIType** en el esquema EWS. Esto sólo ocurre en el elemento **MessageXml** de las respuestas de error que se producen al trabajar con patrones de periodicidad del calendario.  <br/> |
   
Como procedimiento recomendado, cuando solicite propiedades, use la forma base IdOnly ([BasePropertySet. IdOnly](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.basepropertyset%28v=exchg.80%29.aspx) en la API administrada de EWS) y, a continuación, solicite solo las propiedades que necesita la aplicación; para ello, especifique las rutas de la propiedad. 
  
### <a name="schematized-properties"></a>Propiedades de esquematizado

La mayoría de las propiedades que necesita el cliente de EWS se describen en el esquema EWS. La carpeta principal y las definiciones de tipo de elemento, que contienen las definiciones de propiedad, se encuentran en el esquema Types. xsd. Los tipos de esquema siguientes contienen las definiciones de la mayoría de los objetos que se pueden usar.
  
**Tabla 5. Tipos de esquema que contienen definiciones de propiedad**

|**Tipo de esquema EWS**|**Tipo de API administrada de EWS equivalente**|**Define el...**|
|:-----|:-----|:-----|
|**ItemType** <br/> |[Clase Item](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de elemento base. Este tipo se puede crear desde un cliente, pero Exchange no lo devuelve nunca. Exchange devuelve un objeto MessageType para todos los objetos genéricos.  <br/> |
|**MessageType** <br/> |[Clase EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |El conjunto de propiedades de objeto de mensaje de correo electrónico y el conjunto de propiedades para todos los objetos genéricos.  <br/> |
|**CalendarItemType** <br/> |[Clase appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de elemento de calendario; Esto incluye citas únicas y periódicas.  <br/> |
|**ContactItemType** <br/> |[Clase Contact](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de elemento de contacto.  <br/> |
|**DistributionListType** <br/> |[Clase ContactGroup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de la lista de distribución personal.  <br/> |
|**MeetingMessageType** <br/> |[Clase MeetingMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingmessage%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de mensaje de reunión.  <br/> |
|**MeetingRequestMessageType** <br/> |[Clase MeetingRequest](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo convocatoria de reunión.  <br/> |
|**MeetingResponseMessageType** <br/> |[Clase MeetingResponse](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingresponse%28v=exchg.80%29.aspx) <br/> |Propiedad de tipo de respuesta de reunión establecida.  <br/> |
|**MeetingCancellationMessageType** <br/> |[Clase MeetingCancellation](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingcancellation%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de cancelación de reunión.  <br/> |
|**TaskType** <br/> |[Clase Task](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de tarea.  <br/> |
|**PostItemType** <br/> |[Clase PostItem](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo PostItem.  <br/> |
|**FolderType** <br/> |[Clase Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |Conjunto de propiedades de tipo de carpeta.  <br/> |
|**CalendarFolderType** <br/> |[Clase hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |Propiedad de tipo SearchFolder establecida.  <br/> |
|**ContactsFolderType** <br/> |[Clase hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |Propiedad Type hubiera establecida.  <br/> |
|**SearchFolderType** <br/> |[SearchFolder (clase)](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |Propiedad de tipo SearchFolder establecida.  <br/> |
|**TasksFolderType** <br/> |[Clase hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |Propiedad Type hubiera establecida.  <br/> |
|**UserConfigurationType** <br/> |[Clase UserConfiguration](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.userconfiguration%28v=exchg.80%29.aspx) <br/> |Propiedad Type UserConfiguration establecida.  <br/> |
   
Aunque las propiedades del esquema EWS son suficientes para muchas aplicaciones, no puede implementar algunos escenarios solo con lo que se describe en el esquema. Para esos escenarios, puede ampliar las propiedades. 
  
### <a name="extended-properties-aka-non-schematized-properties"></a>Propiedades extendidas (también conocidas, propiedades que no sean esquematizado)

Las propiedades extendidas permiten crear propiedades personalizadas, que proporcionan acceso a las propiedades de elementos y carpetas del almacén de Exchange que no se definen en el esquema EWS. Puede usarlas para tener acceso a las propiedades de elementos y carpetas MAPI nativos de la base de datos de Exchange. Puede usar las propiedades extendidas para tener acceso a todas las propiedades de esquematizado, ya que, en las cubiertas, esas propiedades de esquematizado no son nada más que las propiedades de MAPI en la base de datos de Exchange. 
  
El tipo de esquema PathToExtendedFieldType, que se encuentra en el esquema Types. xsd, define el XML que representa una propiedad extendida. Este tipo de esquema define el elemento [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) en instancias XML; es decir, define el XML que se envía entre el servicio y el cliente. El tipo de esquema ExtendedPropertyType define tanto el elemento [ExtendedFieldURI](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) como el valor o la matriz de valores que contiene una propiedad extendida. En la siguiente tabla se muestra la asignación aproximada del XML de la propiedad extendida y cómo se implementa en los elementos de la API administrada de EWS. 
  
**Tabla 6. XML de propiedad extendida como se implementó en la API administrada de EWS**

|**Implementación de la API administrada de EWS**|**Qué contiene**|**Qué se asigna a**|
|:-----|:-----|:-----|
|[Propiedad Item. ExtendedProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.extendedproperties%28v=exchg.80%29.aspx) <br/> |Una colección de propiedades extendidas de un elemento.  <br/> |Una o más instancias de propiedades extendidas de un elemento.  <br/> |
|[Clase las extendedproperty](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedproperty%28v=exchg.80%29.aspx) <br/> |La definición y los valores de la propiedad extendida.  <br/> |El tipo de esquema ExtendedPropertyType.  <br/> |
|[Clase ExtendedPropertyDefinition](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) <br/> |Una definición de propiedad extendida.  <br/> |El tipo de esquema PathToExtendedFieldType.  <br/> |
   
Si desea obtener más información sobre cómo puede usar las propiedades extendidas en la aplicación, puede explorar los ejemplos de código siguientes: 
  
- [MFCMapi](http://mfcmapi.codeplex.com/)
    
- [Exchange 2013: aprovisionar encabezados X personalizados mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Provision-d4ef5719)
    
- [Exchange 2013: obtener acceso a una propiedad por su etiqueta de propiedad](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-719875ac)
    
- [Exchange 2013: obtener acceso a una propiedad con nombre mediante su identificador](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-02dbe22f)
    
- [Exchange 2013: obtener acceso a una propiedad con nombre por su nombre](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-6556e183)
    
- [Exchange 2013: obtener acceso a una propiedad mediante el GUID y el nombre del conjunto de propiedades](https://code.msdn.microsoft.com/exchange/Exchange-2013-Access-a-4021f971)
    
- [Exchange 2013: crear propiedades extendidas personalizadas mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Create-314db25a)
    
## <a name="in-this-section"></a>En esta sección
<a name="bk_inthissection"> </a>

- [Aprovisionar encabezados x mediante EWS en Exchange](how-to-provision-x-headers-by-using-ews-in-exchange.md)
    
- [Errores relacionados con la propiedad EWS](ews-property-related-errors.md)
    
## <a name="see-also"></a>Vea también


- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)
    
- [MFCMapi](http://mfcmapi.codeplex.com/)
    

