---
title: Las carpetas y elementos de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d8cf6fa-85a4-45ac-8165-e4d3ab92594e
description: Obtenga información sobre las carpetas y los elementos del buzón y cómo la API administrada de EWS o el cliente EWS representa ellos.
ms.openlocfilehash: a3358844f2317c9b0462456ff7d2f38442c98ee3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763034"
---
# <a name="folders-and-items-in-ews-in-exchange"></a>Las carpetas y elementos de EWS en Exchange

Obtenga información sobre las carpetas y los elementos del buzón y cómo la API administrada de EWS o el cliente EWS representa ellos.
  
Las carpetas son el elemento de organización de un buzón de Exchange. Las carpetas pueden contener elementos de buzón de correo, como mensajes de correo electrónico, contactos, citas, reuniones y tareas, o que pueden contener otras carpetas. Exchange incluye tipos diferentes de las carpetas, pero los tipos de carpeta son similares a los otros. La diferencia principal entre ellas es el tipo de elemento que contienen.
  
Elementos, sin embargo, tengan tipos únicos. Cada tipo de elemento tiene un conjunto diferente de propiedades o esquema para definirlo. En este artículo, analizaremos los tipos de carpetas y elementos que están disponibles y las diferencias entre ellos.

<a name="bk_folders"> </a>

## <a name="folders"></a>Carpetas

Todas las carpetas se derivan de la misma clase base o tipo base, la clase de la [carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx) en la API administrada de EWS, o el tipo de [carpeta](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) de EWS. La siguiente ilustración muestra las clases de API administrada de EWS y tipos de EWS. 
  
**En la figura 1. Clases de la carpeta de API administrada de EWS y tipos de carpeta EWS**

![Ilustración que muestra las clases que derivan de la clase Folder de la API administrada de EWS y los tipos que derivan del tipo Folder de EWS, todos ellos denominados CalendarFolder, ContactsFolder, SearchFolder y TasksFolder.](media/Ex2013_Folder_OverviewTypes.png)
  
La diferencia principal entre los tipos de carpeta y cada una de las clases de la carpeta es que sólo se puede crear un tipo determinado de elemento en cada tipo de carpeta. Otra diferencia está en modo en que el cliente muestra información en una carpeta. Por ejemplo, Exchange permite crear citas en la carpeta Calendario. Puede mover otros tipos de elementos en la carpeta del calendario después de que se crean, pero Outlook no mostrarlos. Outlook muestra sólo los elementos del calendario, como las citas y reuniones en la carpeta del calendario, [incluso si existe otro tipo de elemento en la carpeta](folders-and-items-in-ews-in-exchange.md#bk_item). 
  
**La tabla 1. Clases de la carpeta de API administrada de EWS y tipos de carpeta EWS**

|**Clase de la API administrada de EWS**|**Tipo EWS**|**Valor de FolderClass**|**Incluye**|**Notas**|
|:-----|:-----|:-----|:-----|:-----|
|[Folder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |IPF. Nota  <br/> |Mensajes de correo electrónico o las carpetas.  <br/> | Esta es la clase genérica de carpeta o tipo de las siguientes carpetas de API administrada de EWS [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y carpetas EWS [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) : <ul><li>  Raíz (subárbol IPM)</li><li>NonIpmSubtree</li><li>Bandeja de entrada</li><li>Elementos eliminados</li><li>Drafts</li><li>Journal</li><li>Notas  </li><li>Bandeja de salida</li><li>Elementos enviados</li><li>Carpeta de mensajes</li><li>Correo electrónico no deseado</li><li>correo de voz</li></ul> |
|[CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[CalendarFolder](http://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |IPF. Cita  <br/> |Las citas y reuniones.  <br/> |Cuando un usuario responde a una convocatoria de reunión, la cita se agrega a la API administrada de EWS [WellKnownFolderName.Calendar](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) o sólo el EWS [DistinguishedFolderId.CalendarFolder](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) . Estos son las únicas carpetas que admiten la interacción automática con las convocatorias de reunión y las respuestas.  <br/><br/>Esta clase de carpeta o el tipo de carpeta admite el uso de vistas del calendario para devolver las citas y reuniones en función de una fecha de inicio y una fecha de finalización mediante el método de la API administrada de EWS [Folder.FindItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) y la clase [CalendarView](http://msdn.microsoft.com/EN-US/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) o la dirección URL de EWS [FindItem ](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx)operación y el elemento [CalendarView](http://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) .  <br/> |
|[ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[ContactsFolder](http://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |IPF. Contacto  <br/> |Listas de distribución y contactos.  <br/> |Ninguno.  <br/> |
|[SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |IPF. Nota  <br/> |Contenido está determinado por una restricción o un filtro. Las carpetas de búsqueda no tienen las subcarpetas.  <br/> |Los elementos que cumplen los criterios de búsqueda no se encuentran realmente en la carpeta de búsqueda; en su lugar, estén ubicados en otro lugar en el buzón de correo.  <br/> Para asegurarse de que las carpetas de búsqueda están disponibles en Outlook, crear en la carpeta del Finder.  <br/> |
|[TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[TasksFolder](http://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |IPF. Tarea  <br/> |Contiene los elementos de trabajo para llevar a cabo.  <br/> |Ninguno.  <br/> |
   
### <a name="folder-structure"></a>Estructura de carpetas

Carpetas proporcionan una estructura de buzón de correo. Esto incluye el subárbol IPM, conocido como el principio del almacén de información de EWS, donde la mayoría de los usuarios interactuar con su buzón, así como las carpetas del sistema que nunca ve la mayoría de los usuarios, que están en el subárbol no IPM o raíz en EWS. En la siguiente ilustración muestra la estructura de carpetas de un usuario e indica que las carpetas son para los elementos del usuario y cuáles son las carpetas del sistema.
  
**La figura 2. Carpetas de elemento y el sistema en un buzón de correo**

![Ilustración que muestra las carpetas de sistema de la raíz, como Favoritos, Buscador, Datos de disponibilidad, Principio del almacén de información, etc. Principio del almacén de información contiene las carpetas de usuario, como Calendario, Contactos, etc.](media/Ex2013_Folder_OverviewSampleHierarchy.png)
  
### <a name="well-known-folders"></a>Carpetas conocidas

Las carpetas de un buzón de correo, algunas son carpetas especiales. Éstas equivalen a carpetas conocidas en la API administrada de EWS, o distintivo en EWS. Algunas de estas carpetas tienen restricciones en el nombre de la carpeta, dónde se encuentran en la estructura de carpetas, y si se pueden eliminar. Otras carpetas (no especial) "genéricos" no tienen las mismas restricciones. Es importante estar familiarizado con las siguientes carpetas conocidas o distintivos debido a que son el sistema de raíz, usuario y las carpetas de búsqueda y son aplicables a la mayoría de las implementaciones. 
  
**Tabla 2. Carpetas conocidas y distintivos principales**

|**Nombre descriptivo**|**Valores de **WellKnownFolderName** de API administrada de EWS**|**Valores de **DistinguishedFolderId** EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|Raíz (subárbol no IPM)  <br/> |WellKnownFolderName.Root  <br/> |DistinguishedFolderId.root  <br/> |Contiene la carpeta raíz de un buzón de correo, también conocido como el subárbol no IPM. Esta carpeta no tiene ningún elemento primario, y no se puede mover, copiar, cambiar el nombre o eliminarla. Cada almacén de mensajes contiene sólo una carpeta raíz.  <br/> |
|Parte superior del almacén de información (subárbol IPM)  <br/> |WellKnownFolderName.MsgFolderRoot  <br/> |DistinguishedFolderId.msgfolderroot  <br/> |Contiene la Bandeja de entrada y otras carpetas de usuario.  <br/> |
|Finder (las carpetas de búsqueda)  <br/> |WellKnownFolderName.SearchFolders  <br/> |DistinguishedFolderId.searchfolders.  <br/> |Contiene las carpetas de búsqueda que están visibles en Outlook.  <br/> |
   
Para obtener una lista completa de los valores de propiedad de la API administrada de EWS [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.wellknownfoldername%28v=exchg.80%29.aspx) , vea la enumeración [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=EXCHG.80%29.aspx) . Para obtener una lista completa de los valores EWS **DistinguishedFolderId** , vea [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx).
  
### <a name="folder-properties"></a>Propiedades de carpeta

En la API administrada de EWS, las [Propiedades de la carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder_properties%28v=exchg.80%29.aspx) se derivan de la clase base de la [carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx) . Y en EWS, todas las carpetas de usar los elementos de carpeta que están disponibles en el tipo de [carpeta](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) . La mayoría de las propiedades relacionadas con la carpeta y los elementos son un proceso sencillo (primario carpeta identificador, nombre para mostrar etc.), pero algunos requieren una mayor explicación. 
  
Las advertencias siguientes se aplican a la propiedad de la API administrada de EWS [Folder.FolderClass](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.folderclass%28v=EXCHG.80%29.aspx) o el elemento EWS [FolderClass](http://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) : 
  
- Si set, el valor de la propiedad o el elemento debe coincidir con la clase derivada o el tipo de la carpeta. Por ejemplo, la propiedad **FolderClass** o el elemento no se puede indicar que la carpeta es una carpeta de contactos mientras que la clase o tipo de la carpeta indica que la carpeta es una carpeta de calendario. 
    
- Puede puede ser [crear carpetas](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) de un tipo específico sin establecer la propiedad **FolderClass** o elemento, o puede crear una carpeta con el tipo de carpeta genérico y especifique la propiedad **FolderClass** o el elemento. Ambas opciones crean el mismo resultado. 
    
- Después de establecer el valor de **FolderClass** mediante la creación de un tipo específico de carpeta o estableciendo la propiedad de **FolderClass** o el propio elemento, no se puede cambiar. Por ejemplo, no se puede cambiar un error IPF. Carpeta de nota a un error IPF. Carpeta de contactos. Sin embargo, puede cambiar a un error IPF. Carpeta Note.Contoso. 
    
- Cualquier valor de **FolderClass** que no use uno de los prefijos predefinidos se trata como un error IPF. Carpeta de nota. Por ejemplo, un valor de **FolderClass** de IAmAFolderClass se trata como un error IPF. Carpeta de nota. 
    
El valor de la clase de carpeta es extensible. Esto significa que los valores de **FolderClass** predeterminados que aparecen en la tabla 1 se tratan como prefijos y puede agregar valores personalizados. Por ejemplo, puede crear una carpeta con un valor de **FolderClass** de IPF. Contact.Contoso y se trata como una carpeta de contactos. 
  
Puede determinar qué permisos que tiene el cliente en las carpetas, como eliminan, leerán y modificación, mediante el uso de la propiedad de la API administrada de EWS [Folder.EffectiveRights](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.effectiverights%28v=EXCHG.80%29.aspx) o el elemento EWS [EffectiveRights](http://msdn.microsoft.com/library/bf5278eb-3a1a-4d27-9d16-b8be043bb023%28Office.15%29.aspx) . 
  
### <a name="public-folders"></a>Carpetas públicas

Las carpetas públicas están diseñadas para el acceso compartido y proporcionan una forma fácil y efectiva de recopilar, organizar y compartir información con otras personas de su grupo de trabajo u organización. También puede utilizar las carpetas públicas para archivar el contenido de grupo de distribución. Para obtener información detallada acerca de las carpetas públicas, vea la [carpeta pública access con EWS en Exchange](public-folder-access-with-ews-in-exchange.md).

<a name="bk_hiddenfolders"> </a>

### <a name="hidden-folders"></a>Carpetas ocultas

Se ocultan todas las carpetas que Exchange se crea en la raíz del buzón, y puede usar la API administrada de EWS o EWS para ocultar las carpetas adicionales en la parte superior del almacén de información. Para obtener más información acerca de las carpetas ocultas, vea [trabajar con carpetas ocultas mediante el uso de EWS en Exchange](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md). 

<a name="bk_hiddenfolders"> </a>

### <a name="search-folders"></a>Carpetas de búsqueda

Las carpetas de búsqueda son iguales que las carpetas normales, excepto en que tienen una propiedad o un elemento que define el filtro de búsqueda. Puede crear carpetas de búsqueda en cualquier carpeta de un buzón de Exchange y crear de la misma manera que se crea cualquier otra carpeta. Sin embargo, para que una carpeta de búsqueda que aparezca en Outlook, Outlook Web App o Outlook Live, objetos [SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) que cree mediante el uso de la API administrada de EWS deben estar ubicados en la carpeta [WellKnownFolderName.SearchFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y [SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) tipos que se crean mediante el uso de EWS deben estar ubicados en la carpeta [DistinguishedFolderId.SearchFolders](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) . Si la carpeta de búsqueda se crea en una ubicación diferente, sigue estando disponible y puede verlo en aplicaciones de cliente personalizadas. 

<a name="bk_item"> </a>

## <a name="items"></a>Elementos

EWS en Exchange usa **los elementos** para representar los mensajes de correo electrónico individuales, las citas, reuniones, contactos, listas de distribución, tareas, entradas y otros elementos en un buzón de correo. Los elementos son que cualquiera establecimiento inflexible de tipos, lo que significa que disponen de una clase específica asociada o esquema o elementos no fuertemente tipados, también conocido como genéricos. Los elementos genéricos son objetos de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) en los tipos de API administrada de EWS y [elemento](http://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) de EWS. Elementos comunes, como mensajes de correo electrónico, contactos, listas de distribución, entradas y tareas están fuertemente tipadas y se puede establecer propiedades específicas de esquematizado o elementos en ellos. 
  
**Tabla 3. Elementos fuertemente tipados**

|**Tipo de elemento de la API administrada de EWS**|**Elemento de EWS**|
|:-----|:-----|
|[Appointment](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Contact](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contact](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[ContactGroup](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |[DistributionList](http://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx) <br/> |
|[EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[Objeto postItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |[Objeto postItem](http://msdn.microsoft.com/library/7727ed84-9591-4a1c-bb04-12129926499b%28Office.15%29.aspx) <br/> |
|[Tarea](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Tarea](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
API administrada de EWS fuertemente tipado elementos derivar de la clase de [elemento](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item%28v=EXCHG.80%29.aspx) base. Sin embargo, se suele trabajar con uno de los tipos derivados que aparecen en la tabla 3 y no con la clase de **elemento** directamente. Cuando se trabaja con la clase [ItemCollection](http://msdn.microsoft.com/en-us/library/dd634001%28v=EXCHG.80%29.aspx) , sin embargo, es posible que trabajar directamente con instancias de la clase de **elemento** . En ese caso, debe implementar la lógica que determina el tipo de elemento en el almacén que representa la instancia de la clase de **elemento** . Para que funcione con ese elemento, se debe enlazar al elemento mediante el uso de una instancia de la clase que representa el elemento. 
  
### <a name="items-in-folders"></a>Elementos de las carpetas

Algunas carpetas tienen restricciones sobre los tipos de elementos que pueden contener. Estos son las restricciones de la base de datos de buzón de correo de Exchange se aplica a las carpetas, no las limitaciones de vista del cliente. 
  
**Tabla 4. Restricciones de elemento para carpetas**

|**Clase de carpeta de API administrada de EWS**|**Tipo de carpeta de EWS**|**Restriction**|
|:-----|:-----|:-----|
|[Clase base de carpeta](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](http://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |Sólo se pueden crear nuevos objetos de la API administrada de EWS [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) y objetos [PostItem](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) , o EWS [mensaje](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) tipos o **PostItem** , en las carpetas genéricas. Puede mover otros tipos de elementos en carpetas genéricas, pero el cliente no puede mostrarlos.  <br/> |
|[CalendarFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[CalendarFolder](http://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |Sólo se pueden crear nuevos objetos de la API administrada de EWS [cita](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) y tipos de EWS [CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) en la carpeta Calendario. Puede mover otros tipos de elementos en la carpeta del calendario, pero el cliente no puede mostrarlos.  <br/> |
|[ContactsFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[ContactsFolder](http://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |Sólo se pueden crear nuevos objetos de [contacto](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) de API administrada de EWS y [ContactGroup](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) , o tipos de EWS [contacto](http://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) o [DistributionList](http://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx) tipos en la carpeta Contactos. Puede mover otros tipos de elementos en la carpeta de contactos, pero el cliente no puede mostrar ellos  <br/> |
|[SearchFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](http://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |No hay restricciones. Los elementos no se encuentran en realidad en la carpeta de búsqueda; se encuentran en cualquier parte del buzón de correo.  <br/> |
|[TasksFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[TasksFolder](http://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |Sólo se pueden crear nuevos objetos de la API administrada de EWS [tarea](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) o tipos de EWS [tarea](http://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) en la carpeta tareas. Puede mover otros tipos de elementos en la carpeta de tareas, pero el cliente no puede mostrar ellos  <br/> |

<a name="bk_upgrading"> </a>

## <a name="upgrading-from-earlier-product-versions"></a>Actualizar desde versiones anteriores del producto

Las carpetas para la mayor parte han cambiado en las versiones anteriores y actual del producto. Sin embargo, tenga en cuenta que las versiones anteriores de Exchange utilizan las carpetas administradas para llevar a cabo la administración de registros de mensajería (MRM). Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013 usar directivas de retención para MRM. Puede que la [actualización carpetas administradas en el uso de directivas de retención](http://technet.microsoft.com/en-us/library/dd298032%28v=exchg.150%29.aspx). 
  
Los elementos no han cambiado en las versiones anteriores y actual del producto.

<a name="bk_inthissection"> </a>

## <a name="in-this-section"></a>En esta sección

- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con carpetas ocultas con EWS en Exchange](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con los elementos del buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    
- [Eliminar elementos mediante el uso de EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Exportar e importar elementos mediante el uso de EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)   
- [Empezar a utilizar servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    

