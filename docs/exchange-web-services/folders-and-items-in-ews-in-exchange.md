---
title: Carpetas y elementos de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 9d8cf6fa-85a4-45ac-8165-e4d3ab92594e
description: Obtenga información sobre carpetas y elementos de buzón y cómo los representa su cliente de EWS o la API administrada de EWS.
localization_priority: Priority
ms.openlocfilehash: 5e206d6973d148c6f70a17a8e7891bf3de7c1533
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/02/2020
ms.locfileid: "44455991"
---
# <a name="folders-and-items-in-ews-in-exchange"></a>Carpetas y elementos de EWS en Exchange

Obtenga información sobre carpetas y elementos de buzón y cómo los representa su cliente de EWS o la API administrada de EWS.
  
Las carpetas son el elemento de organización de un buzón de Exchange. Las carpetas pueden contener elementos de buzón, como mensajes de correo electrónico, contactos, citas, reuniones y tareas, o pueden contener otras carpetas. Exchange incluye distintos tipos de carpetas, pero los tipos de carpeta son similares. La diferencia principal es el tipo de elemento que contienen.
  
Los elementos, sin embargo, tienen tipos únicos. Cada tipo de elemento tiene un conjunto de propiedades o esquema diferente para definirlo. En este artículo, analizaremos los tipos de carpetas y elementos que están disponibles y las diferencias entre ellos.

<a name="bk_folders"> </a>

## <a name="folders"></a>Folders

Las carpetas se derivan de la misma clase base o tipo base, la clase de [carpeta](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx) en la API administrada de EWS o el tipo de [carpeta](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) en EWS. En la siguiente figura se muestran las clases de API administrada de EWS y los tipos EWS. 
  
**Figura 1. Clases de carpetas de la API administrada EWS y tipos de carpetas EWS**

![Ilustración que muestra las clases que derivan de la clase Folder de la API administrada de EWS y los tipos que derivan del tipo Folder de EWS, todos ellos denominados CalendarFolder, ContactsFolder, SearchFolder y TasksFolder.](media/Ex2013_Folder_OverviewTypes.png)
  
La principal diferencia entre cada una de las clases de carpeta y los tipos de carpeta es que solo se puede crear un tipo específico de elemento en cada tipo de carpeta. Otra diferencia radica en cómo el cliente muestra la información en una carpeta. Por ejemplo, Exchange permite crear citas en la carpeta calendario. Puede mover otros tipos de elementos a la carpeta calendario después de crearlos, pero Outlook no los mostrará. Outlook solo muestra elementos de calendario como citas y reuniones en la carpeta calendario, [incluso si existe otro tipo de elemento en la carpeta](folders-and-items-in-ews-in-exchange.md#bk_item). 
  
**Tabla 1. Clases de carpetas de la API administrada EWS y tipos de carpetas EWS**

|**Clase de API administrada de EWS**|**Tipo EWS**|**Valor FolderClass**|**Contains**|**Notas**|
|:-----|:-----|:-----|:-----|:-----|
|[Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |Error. Note  <br/> |Mensajes de correo electrónico o carpetas.  <br/> | Este es el tipo o clase de carpeta genérica para las carpetas de [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) de la API administrada de EWS y las carpetas de [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) de EWS: <ul><li>  Root (subárbol IPM)</li><li>NonIpmSubtree</li><li>Bandeja de entrada</li><li>Elementos eliminados</li><li>Borradores</li><li>Diario</li><li>Notas  </li><li>Bandeja de salida</li><li>Elementos enviados</li><li>Carpeta de mensajes</li><li>Correo electrónico no deseado</li><li>Correo de voz</li></ul> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |Error. Convoca  <br/> |Citas y reuniones.  <br/> |Cuando un usuario responde a una convocatoria de reunión, la cita se agrega a la API administrada de EWS [WellKnownFolderName. Calendar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) o la [DistinguishedFolderId. hubiera](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) de EWS. Estas son las únicas carpetas que admiten la interacción automática con las convocatorias de reunión y las respuestas.  <br/><br/>Esta clase de carpeta o tipo de carpeta admite el uso de vistas de calendario para devolver citas y reuniones en función de la fecha de inicio y la fecha de finalización mediante la carpeta de la API administrada de EWS. el método [FindItem](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=EXCHG.80%29.aspx) y la clase [CalendarView](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarview%28v=exchg.80%29.aspx) , o la operación [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) de EWS y el elemento [CalendarView](https://msdn.microsoft.com/library/a4a953b8-0710-416c-95ef-59e51eba9982%28Office.15%29.aspx) .  <br/> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |Error. Contact  <br/> |Contactos y listas de distribución.  <br/> |Ninguna.  <br/> |
|[SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |Error. Note  <br/> |El contenido se determina por una restricción o un filtro. Las carpetas de búsqueda no tienen subcarpetas.  <br/> |Los elementos que cumplen los criterios de búsqueda no se incluyen realmente en la carpeta de búsqueda; en su lugar, se ubican en cualquier lugar del buzón.  <br/> Para asegurarse de que las carpetas de búsqueda están disponibles en Outlook, créelos en la carpeta Finder.  <br/> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |Error. Tareas  <br/> |Contiene los elementos de trabajo que se deben completar.  <br/> |Ninguna.  <br/> |
   
### <a name="folder-structure"></a>Estructura de carpetas

Las carpetas proporcionan una estructura de buzón de correo. Esto incluye el subárbol IPM, conocido como la parte superior del almacén de información de EWS, donde la mayoría de los usuarios interactúan con sus buzones, así como las carpetas del sistema que la mayoría de los usuarios nunca ven, que están en el subárbol no IPM o la raíz en EWS. En la siguiente figura se muestra la estructura de carpetas de un usuario y se indica qué carpetas son para los elementos del usuario y cuáles son las carpetas del sistema.
  
**Figura 2. Elemento y carpetas del sistema de un buzón de correo**

![Ilustración que muestra las carpetas de sistema de la raíz, como Favoritos, Buscador, Datos de disponibilidad, Principio del almacén de información, etc. Principio del almacén de información contiene las carpetas de usuario, como Calendario, Contactos, etc.](media/Ex2013_Folder_OverviewSampleHierarchy.png)
  
### <a name="well-known-folders"></a>Carpetas conocidas

De las carpetas de un buzón de correo, algunas son carpetas especiales. Estos equivalen a carpetas conocidas en la API administrada de EWS o en carpetas completas en EWS. Algunas de estas carpetas tienen restricciones en el nombre de la carpeta, donde se encuentran en la estructura de carpetas y si se pueden eliminar. Otras carpetas "genéricas" (no especiales) no tienen las mismas restricciones. Es importante que esté familiarizado con las siguientes carpetas completas o conocidas, ya que son las carpetas del sistema raíz, el usuario y la búsqueda, y son aplicables a la mayoría de las implementaciones. 
  
**Tabla 2. Carpetas principales y conocidas principales**

|**Nombre descriptivo**|**Valores de **WellKnownFolderName** de la API administrada de EWS**|**Valores de **DistinguishedFolderId** de EWS**|**Descripción**|
|:-----|:-----|:-----|:-----|
|Raíz (subárbol no IPM)  <br/> |WellKnownFolderName. root  <br/> |DistinguishedFolderId. root  <br/> |Contiene la carpeta raíz de un buzón de correo, también conocido como subárbol no IPM. Esta carpeta no tiene ningún elemento primario y no se puede mover, copiar, cambiar el nombre o eliminar. Cada almacén de mensajes contiene sólo una carpeta raíz.  <br/> |
|Principio del almacén de información (subárbol IPM)  <br/> |WellKnownFolderName.MsgFolderRoot  <br/> |DistinguishedFolderId.msgfolderroot  <br/> |Contiene la bandeja de entrada y otras carpetas de usuario.  <br/> |
|Finder (carpetas de búsqueda)  <br/> |WellKnownFolderName. SearchFolders  <br/> |DistinguishedFolderId. SearchFolders.  <br/> |Contiene las carpetas de búsqueda que están visibles en Outlook.  <br/> |
   
Para obtener una lista completa de los valores de propiedad de [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.wellknownfoldername%28v=exchg.80%29.aspx) de la API administrada de EWS, vea la enumeración [WellKnownFolderName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=EXCHG.80%29.aspx) . Para obtener una lista completa de los valores de **DistinguishedFolderId** de EWS, consulte [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx).
  
### <a name="folder-properties"></a>Propiedades de carpeta

En la API administrada de EWS, las propiedades de la [carpeta](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder_properties%28v=exchg.80%29.aspx) se derivan de la clase base [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=EXCHG.80%29.aspx) . Y en EWS, todas las carpetas usan los elementos de la carpeta que están disponibles en el tipo de [carpeta](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) . La mayoría de las propiedades y elementos relacionados con carpetas son sencillos (identificador de carpeta principal, nombre para mostrar, etc.), pero algunos requieren una pequeña explicación. 
  
Las siguientes advertencias se aplican a la propiedad [Folder. FolderClass](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.folderclass%28v=EXCHG.80%29.aspx) de la API administrada de EWS o al elemento [FolderClass](https://msdn.microsoft.com/library/0041d135-2869-4612-89a5-d1aa86aa1093%28Office.15%29.aspx) de EWS: 
  
- Si se establece, el valor de la propiedad o del elemento debe estar de acuerdo con la clase derivada o el tipo de carpeta. Por ejemplo, la propiedad o el elemento **FolderClass** no puede indicar que la carpeta es una carpeta de contactos mientras que la clase o el tipo de la carpeta indica que la carpeta es una carpeta de calendario. 
    
- Puede [crear carpetas](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) de un tipo específico sin establecer la propiedad o el elemento **FolderClass** , o puede crear una carpeta con el tipo de carpeta genérica y especificar la propiedad o el elemento **FolderClass** . Ambas opciones crean el mismo resultado. 
    
- Después de establecer el valor **FolderClass** mediante la creación de un tipo específico de carpeta o estableciendo la propiedad **FolderClass** o el propio elemento, no se puede cambiar. Por ejemplo, no puede cambiar un IPF. Nota un error IPF en la carpeta. Carpeta de contactos. Sin embargo, puede cambiarlo a un error IPF. Carpeta Note. contoso. 
    
- Cualquier valor de **FolderClass** que no use uno de los prefijos predefinidos se trata como un IPF. Carpeta Nota. Por ejemplo, un valor **FolderClass** de IAmAFolderClass se trata como un IPF. Carpeta Nota. 
    
El valor de la clase Folder es extensible. Esto significa que los valores predeterminados de **FolderClass** que aparecen en la tabla 1 se tratan como prefijos y puede agregar valores personalizados. Por ejemplo, puede crear una carpeta con un valor **FolderClass** de ipf. Contact. contoso y se trata como una carpeta de contactos. 
  
Puede determinar qué permisos tiene el cliente en las carpetas, como eliminar, leer y modificar, mediante la propiedad [Folder. EffectiveRights](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.effectiverights%28v=EXCHG.80%29.aspx) de la API administrada de EWS o el elemento [EffectiveRights](https://msdn.microsoft.com/library/bf5278eb-3a1a-4d27-9d16-b8be043bb023%28Office.15%29.aspx) de EWS. 
  
### <a name="public-folders"></a>Carpetas públicas

Las carpetas públicas están diseñadas para un acceso compartido y ofrecen una manera fácil y efectiva de obtener, organizar y compartir información con otras personas de su grupo de trabajo u organización. También puede usar carpetas públicas para archivar el contenido del grupo de distribución. Para obtener información detallada acerca de las carpetas públicas, consulte [acceso a carpetas públicas con EWS en Exchange](public-folder-access-with-ews-in-exchange.md).

<a name="bk_hiddenfolders"> </a>

### <a name="hidden-folders"></a>Carpetas ocultas

Todas las carpetas que crea Exchange en la raíz del buzón de correo están ocultas y puede usar la API administrada de EWS o EWS para ocultar carpetas adicionales en la parte superior del almacén de información. Para obtener más información acerca de las carpetas ocultas, vea [trabajar con carpetas ocultas mediante EWS en Exchange](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md). 

<a name="bk_hiddenfolders"> </a>

### <a name="search-folders"></a>Carpetas de búsqueda

Las carpetas de búsqueda son similares a las carpetas normales, excepto por el hecho de que tienen una propiedad o elemento que define el filtro de búsqueda. Puede crear carpetas de búsqueda en cualquier carpeta de un buzón de Exchange y crearlas de la misma forma que crea cualquier otra carpeta. Sin embargo, para que una carpeta de búsqueda aparezca en Outlook, Outlook Web App o Outlook Live, los objetos [searchfolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) que cree mediante la API administrada de EWS deben estar ubicados en la carpeta [WellKnownFolderName. SearchFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) , y los tipos [searchfolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) que cree mediante EWS deben estar ubicados en la carpeta [DistinguishedFolderId. SearchFolders](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) . Si la carpeta de búsqueda se crea en una ubicación diferente, sigue estando disponible y se puede ver en aplicaciones cliente personalizadas. 

<a name="bk_item"> </a>

## <a name="items"></a>Elementos

EWS en Exchange usa **elementos** para representar mensajes de correo electrónico individuales, citas, reuniones, contactos, listas de distribución, tareas, publicaciones y otros elementos en un buzón. Los elementos tienen establecimiento inflexible de tipos, lo que significa que tienen una clase o esquema asociado específico, o que no tienen establecimiento inflexible de tipos, también conocidos como elementos genéricos. Los elementos genéricos son objetos de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=exchg.80%29.aspx) de la API administrada de EWS y tipos de [elementos](https://msdn.microsoft.com/library/4dfe8f48-e7b4-444d-bdf9-a34e180f598b%28Office.15%29.aspx) de EWS. Los elementos comunes como los mensajes de correo electrónico, los contactos, las listas de distribución, las publicaciones y las tareas tienen establecimiento inflexible de tipos, y puede establecer propiedades o elementos esquematizado específicos en ellos. 
  
**Tabla 3. Elementos con establecimiento inflexible de tipos**

|**Tipo de elemento de la API administrada EWS**|**Elemento de elemento EWS**|
|:-----|:-----|
|[Appointment](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) <br/> |[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |
|[Contacto](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) <br/> |[Contacto](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) <br/> |
|[ContactGroup](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) <br/> |[DistributionList](https://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx) <br/> |
|[EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) <br/> |[Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) <br/> |
|[PostItem](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) <br/> |[PostItem](https://msdn.microsoft.com/library/7727ed84-9591-4a1c-bb04-12129926499b%28Office.15%29.aspx) <br/> |
|[Tarea](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) <br/> |[Tarea](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) <br/> |
   
La API administrada de EWS los elementos fuertemente tipados derivan de la clase de [elemento](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item%28v=EXCHG.80%29.aspx) base. Sin embargo, normalmente se trabaja con uno de los tipos derivados que se enumeran en la tabla 3 y no con la clase de **elemento** directamente. Sin embargo, cuando trabaja con la clase [ItemCollection](https://msdn.microsoft.com/library/dd634001%28v=EXCHG.80%29.aspx) , puede trabajar directamente con instancias de la clase **Item** . En ese caso, debe implementar la lógica que determine el tipo de elemento del almacén que representa la instancia de la clase **Item** . Para trabajar con ese elemento, debe enlazar al elemento mediante una instancia de la clase que representa el elemento. 
  
### <a name="items-in-folders"></a>Elementos de carpetas

Algunas carpetas tienen restricciones sobre los tipos de elementos que pueden contener. Estas son restricciones que la base de datos de buzones de Exchange aplica a las carpetas, no a las limitaciones de la vista de cliente. 
  
**Tabla 4. Restricciones de elementos de carpetas**

|**Clase de carpeta de API administrada EWS**|**Tipo de carpeta EWS**|**Restriction**|
|:-----|:-----|:-----|
|[Clase de carpeta base](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder%28v=exchg.80%29.aspx) <br/> |[Folder](https://msdn.microsoft.com/library/812948d8-c7db-45ce-bb3a-77233a53a974%28Office.15%29.aspx) <br/> |Solo se pueden crear nuevos objetos [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) de la API administrada de EWS y objetos [PostItem](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.postitem%28v=exchg.80%29.aspx) , o tipos de [mensajes](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) EWS o tipos **PostItem** , en las carpetas genéricas. Puede mover otros tipos de elementos a carpetas genéricas, pero es posible que el cliente no los muestre.  <br/> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.calendarfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/48687a78-e757-4c04-9641-bf4302c6b565%28Office.15%29.aspx) <br/> |Solo se pueden crear nuevos objetos de [cita](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment%28v=exchg.80%29.aspx) de API administrada de EWS y tipos de [CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) de EWS en la carpeta calendario. Puede mover otros tipos de elementos a la carpeta calendario, pero es posible que el cliente no los muestre.  <br/> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactsfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/6c299de8-2087-4aeb-8e66-2bc7586509a6%28Office.15%29.aspx) <br/> |Solo se pueden crear nuevos objetos de [contacto](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contact%28v=exchg.80%29.aspx) y de [CONTACTGROUP](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.contactgroup%28v=exchg.80%29.aspx) de la API administrada de EWS, o tipos de [contacto](https://msdn.microsoft.com/library/66bfff50-7a91-4d81-b6a0-610b9962f677%28Office.15%29.aspx) de EWS o tipos de [DistributionList](https://msdn.microsoft.com/library/f65aea01-e870-44a2-8571-fa6c001341cc%28Office.15%29.aspx) en la carpeta de contactos. Puede mover otros tipos de elementos a la carpeta de contactos, pero es posible que el cliente no los muestre  <br/> |
|[SearchFolder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.searchfolder%28v=exchg.80%29.aspx) <br/> |[SearchFolder](https://msdn.microsoft.com/library/1a7d408b-2e98-4391-8834-085ed6d5757c%28Office.15%29.aspx) <br/> |Sin restricciones. Los elementos no se encuentran realmente en la carpeta de búsqueda; se encuentran en cualquier lugar del buzón.  <br/> |
|[Hubiera](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.tasksfolder%28v=exchg.80%29.aspx) <br/> |[Hubiera](https://msdn.microsoft.com/library/5a9a4612-8064-4986-b467-c44f268c64df%28Office.15%29.aspx) <br/> |Solo se pueden crear nuevos objetos de [tarea](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.task%28v=exchg.80%29.aspx) de la API administrada de EWS o tipos de [tareas](https://msdn.microsoft.com/library/7c84927e-db28-4c5d-b0b5-cbcc2b88d869%28Office.15%29.aspx) EWS en la carpeta tareas. Puede mover otros tipos de elementos a la carpeta tareas, pero es posible que el cliente no los muestre  <br/> |

<a name="bk_upgrading"> </a>

## <a name="upgrading-from-earlier-product-versions"></a>Actualización desde versiones anteriores del producto

Las carpetas tienen la mayor parte de las cuales se han mantenido sin cambios en versiones anteriores y actuales del producto. Sin embargo, tenga en cuenta que las versiones anteriores de Exchange usan carpetas administradas para realizar la administración de registros de mensajería (MRM). Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013 usar directivas de retención para MRM. Puede [actualizar las carpetas administradas para usar directivas de retención](https://technet.microsoft.com/library/dd298032%28v=exchg.150%29.aspx). 
  
Los elementos no han cambiado en versiones anteriores y actuales del producto.

<a name="bk_inthissection"> </a>

## <a name="in-this-section"></a>En esta sección

- [Trabajar con carpetas mediante EWS en Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con carpetas ocultas mediante EWS en Exchange](how-to-work-with-hidden-folders-by-using-ews-in-exchange.md)
    
- [Trabajar con elementos de buzón de Exchange mediante EWS en Exchange](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md)
    
- [Eliminar elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    
- [Exportar e importar elementos mediante EWS en Exchange](exporting-and-importing-items-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)   
- [Empezar a usar los servicios web de Exchange](start-using-web-services-in-exchange.md)   
- [Introducción al diseño de EWS cliente de Exchange](ews-client-design-overview-for-exchange.md)
    

