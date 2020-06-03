---
title: Eliminación de elementos mediante EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: c81e3160-e12b-47e0-b3d6-4be28537f301
description: Descubra cómo puede usar la API administrada de EWS o EWS en Exchange para eliminar elementos moviéndolos a la carpeta elementos eliminados o al contenedor.
localization_priority: Priority
ms.openlocfilehash: 83317ccd0fa1db64e14df68652489009fea4ea07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456139"
---
# <a name="deleting-items-by-using-ews-in-exchange"></a>Eliminación de elementos mediante EWS en Exchange

Descubra cómo puede usar la API administrada de EWS o EWS en Exchange para eliminar elementos moviéndolos a la carpeta elementos eliminados o al contenedor.
  
¿Se ha preguntado alguna vez cuál es la diferencia entre mover elementos a la carpeta elementos eliminados y moverlos al contenedor? Puede ser curioso sobre las distintas opciones para controlar los elementos eliminados y cómo implementar dichas opciones en la aplicación. Los servicios web Exchange (EWS) incluyen tres opciones para el tratamiento de elementos eliminados. Es muy probable que, en este artículo, se borre cualquier confusión que pueda tener acerca de las diferencias entre ellos.
  
## <a name="deleting-items---what-are-my-options"></a>Eliminar elementos: ¿Cuáles son mis opciones?
<a name="bk_DeletingItemsOptions"> </a>

Antes de comprender el panorama general para eliminar elementos, es importante que reconozca la diferencia entre lo siguiente:
  
- La carpeta elementos eliminados: cuando se eliminan elementos en un buzón de correo, aquí es donde van.
    
- El contenedor (también conocido como carpeta de elementos recuperables) cuando se quitan elementos de un buzón de correo, aquí es donde van.
    
Las figuras 1 y 2 muestran el aspecto que tiene el proceso de eliminación para los elementos y las carpetas de un buzón de correo. 

**Figura 1. Proceso para eliminar elementos de un buzón de correo**

![Ilustración que muestra a dónde van los elementos cuando se eliminan. Los elementos eliminados se mueven a la carpeta elementos eliminados y, a continuación, se mueven a la carpeta elementos recuperables por directiva de retención, donde expiran y se permantently eliminan.](media/Ex_DeleteItems_Source.png)

<br/>

**Figura 2. Proceso para eliminar carpetas de un buzón**

![Ilustración que muestra cómo las carpetas eliminadas se mueven a la carpeta Elementos eliminados y luego pueden eliminarse de manera permanente del buzón de correo.](media/Ex_.png)
   
Puede eliminar los elementos y las carpetas de tres maneras diferentes, en función de la "permanente" que desea que se elimine.
  
**Tabla 1: opciones para eliminar elementos mediante EWS**

|**Opción**|**Qué ocurre**|
|:-----|:-----|
|Mover a la carpeta Elementos eliminados  <br/> |Esta es la forma menos permanente de eliminar elementos.<br/><br/>Esto es similar a colocar una hoja de papel en la papelera de reciclaje de su escritorio. Puede tomarla fácilmente si es necesario.<br/><br/>Puede usar cualquier [operación de eliminación](deleting-items-by-using-ews-in-exchange.md#bk_howdoIdeleteitems) que implemente la opción mover a la carpeta elementos eliminados para realizar esta acción.<br/><br/>También puede usar la [operación MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) ( [Item. Move ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx)) o la [operación MoveFolder](https://msdn.microsoft.com/library/c7233966-6c87-4a14-8156-b1610760176d%28Office.15%29.aspx) ( [Folder. Move ()](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.move%28v=exchg.80%29.aspx)) para mover un elemento o una carpeta a la carpeta elementos eliminados.  <br/> |
|Eliminar temporalmente  <br/> |El elemento se mueve a la carpeta eliminaciones del contenedor.<br/><br/>Esto es como vaciar la papelera de reciclaje en el contenedor Curbside. Todavía puede tener acceso al elemento si es necesario, es un poco más difícil.  <br/><br/>Para obtener más información sobre el contenedor (también denominado la carpeta elementos recuperables) y escenarios como eDiscovery o retenciones por juicio, consulte [Recoverable items Folder](https://technet.microsoft.com/library/ee364755%28v=exchg.150%29.aspx) en TechNet.<br/><br/>No se recomiendan las eliminaciones de software para las aplicaciones destinadas a Exchange 2007. En Exchange 2007, las eliminaciones de software se administran estableciendo un bit en el elemento para indicar que se moverá al contenedor en un momento no especificado.<br/><br/>Los recorridos de eliminación de software, o búsquedas de elementos que se han eliminado de forma parcial mediante la [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx), no son compatibles con Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange que comienzan con Exchange 2010.  <br/><br/>**Nota**: las carpetas no se pueden eliminar temporalmente.           |
|Eliminar de forma permanente  <br/> |El elemento o carpeta se elimina de forma permanente.<br/><br/>Los elementos eliminados permanentemente se colocan en la carpeta purgas del contenedor. Esto es como cuando el camión de reciclaje vacía el contenedor de reciclaje de Curbside. No se puede acceder a los elementos desde un cliente de correo electrónico como Outlook o Outlook Web App y, a menos que haya un conjunto de suspensión en el buzón, los elementos se eliminarán permanentemente después de un período de tiempo establecido.<br/><br/>Para obtener más información acerca de la retención de elementos, vea el artículo configurar la retención de elementos [eliminados y las cuotas de elementos recuperables](https://technet.microsoft.com/library/ee364752%28v=exchg.150%29.aspx).<br/><br/>**Nota**: las carpetas no se colocan en la carpeta purgadores cuando se eliminan de forma permanente. Las carpetas eliminadas permanentemente se quitan del buzón de correo.  |
   
La carpeta mover a la carpeta elementos eliminados y las opciones para eliminar permanentemente son transaccionales, lo que significa que, en el momento en que finaliza la llamada al servicio Web, el elemento se movió a la carpeta elementos eliminados o al contenedor.
  
Para ayudarle a comprender mejor el ecosistema de las carpetas que se usan para almacenar los elementos eliminados, en la siguiente figura se muestra la jerarquía de carpetas que pueden contener elementos eliminados. Los nombres de carpeta son los que aparecen en el tipo de esquema **DistinguishedFolderIdNameType** o la enumeración **WELLKNOWNFOLDERNAME** en la API administrada de EWS. 
  
**Figura 3. Jerarquía de carpetas que contienen elementos eliminados**

![Figura que muestra la jerarquía de carpetas de las carpetas que pueden contener elementos eliminados en un buzón de correo principal y de archivo. Cada carpeta de la imagen se representa con su nombre de carpeta distintivo.](media/Ex_FolderHierarchyDeletedItems.png)
  
**Tabla 2: carpetas que contienen elementos eliminados**

|**Nombre de carpeta**|**Introducido en**|**Descripción**|
|:-----|:-----|:-----|
|deleteditems  <br/> |Exchange 2007  <br/> |Carpeta elementos eliminados predeterminada. Los elementos permanecen en esta carpeta hasta que se eliminan temporalmente o de forma permanente, o hasta que se supera un período de retención. A continuación, se mueven a una carpeta del contenedor. Las carpetas eliminadas se colocan en la carpeta elementos eliminados y, cuando se eliminan temporalmente o de forma permanente, se quitan permanentemente del buzón y no se pueden recuperar.  <br/> |
|recoverableitemsroot  <br/> |Exchange 2010  <br/> |La raíz del contenedor o la carpeta elementos recuperables. El acceso al contenedor se ha implementado en EWS en Exchange 2010. El nombre para mostrar de esta carpeta es "elementos recuperables".  <br/> |
|recoverableitemsdeletions  <br/> |Exchange 2010  <br/> |La carpeta de contenedor principal de un buzón de correo. Los elementos eliminados temporalmente y los elementos movidos de la carpeta elementos eliminados por una directiva de retención se colocan en esta carpeta. El nombre para mostrar de esta carpeta es "eliminaciones".  <br/> |
|recoverableitemsversions  <br/> |Exchange 2010  <br/> |Donde se almacenan versiones anteriores de un elemento. Las versiones anteriores de un elemento se crean cuando se actualiza un elemento. Las versiones de borrador de elemento no se guardan en esta carpeta. El nombre para mostrar de esta carpeta es "versiones".  <br/> |
|recoverableitemspurges  <br/> |Exchange 2010  <br/> |Dónde se almacenan los elementos que se quitan de la carpeta eliminaciones. Todos los elementos eliminados permanentemente de la tienda se mueven a esta carpeta. El nombre para mostrar de esta carpeta es "purgados".  <br/> |
|archiveddeletedtitems  <br/> |Exchange 2010  <br/> |La carpeta elementos eliminados predeterminada para un buzón de archivo.  <br/> |
|archiverecoverablesitemsroot  <br/> |Exchange 2010  <br/> |La carpeta raíz del contenedor de un buzón de archivo. Los elementos archivados que se eliminan temporalmente se mueven a una subcarpeta de esta carpeta.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Exchange 2010  <br/> |La carpeta de contenedor principal para un buzón de archivo. Los elementos archivados que se mueven al contenedor se colocan aquí.  <br/> |
|archiverecoverableitemsversions  <br/> |Exchange 2010  <br/> |Donde se almacenan versiones anteriores de los elementos archivados.  <br/> |
|archiverecoverableitemspurges  <br/> |Exchange 2010  <br/> |Dónde se almacenan los elementos que se eliminan de forma permanente de la carpeta eliminaciones de archivo en el contenedor. Todos los elementos archivados eliminados permanentemente se mueven a esta carpeta.  <br/> |
   
## <a name="how-do-i-delete-items"></a>¿Cómo se eliminan los elementos?
<a name="bk_howdoIdeleteitems"> </a>

Use una de las siguientes opciones para indicar si se debe mover un elemento a la carpeta elementos eliminados o realizar una eliminación temporal o una eliminación de hardware:
  
- El tipo simple **DisposalType** , si usa EWS para tener acceso a Exchange. 
    
- La [enumeración DeleteMode](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.deletemode%28v=exchg.80%29.aspx), si usa la API administrada de EWS.
    
Puede usar varias operaciones de EWS o métodos de API administrada de EWS para eliminar elementos y carpetas de un buzón.
  
**Tabla 3: operaciones de EWS y métodos de API administrada de EWS para eliminar elementos**

|**Operación de EWS**|**Método de la API administrada de EWS**|**Introducido en**|**Qué hace**|
|:-----|:-----|:-----|:-----|
|[Operación DeleteFolder](https://msdn.microsoft.com/library/b0f92682-4895-4bcf-a4a1-e4c2e8403979%28Office.15%29.aspx) <br/> |[Método Folder. Delete](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.folder.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Elimina carpetas de un buzón. Con EWS, puede eliminar las carpetas por lotes. Con la API administrada de EWS, solo puede eliminar una carpeta única por llamada.  <br/> |
|[Operación DeleteItem](https://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |[Método Item. Delete](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx)<br/><br/>[Método ExchangeService. DeleteItems](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.exchangeservice.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Elimina elementos de un buzón de correo.  <br/> |
|[Operación EmptyFolder](https://msdn.microsoft.com/library/98161486-e2f2-480f-8d5d-708ba81b208a%28Office.15%29.aspx) <br/> |[Método Folder. Empty](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.folder.empty%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Elimina todos los elementos de una carpeta y, opcionalmente, elimina todas las subcarpetas de una carpeta.  <br/> |
|[Operación ApplyConversationAction](https://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |[Método Conversation. EnableAlwaysDeleteItems](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx)<br/><br/>[Método Conversation. DeleteItems](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.conversation.deleteitems%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Establece una acción de procesamiento de eliminación en los mensajes de correo electrónico de una conversación para que se eliminen.  <br/> |
|[Operación DeleteUserConfiguration](https://msdn.microsoft.com/library/93e44690-be2d-4fdb-96a8-4ded3c193aed%28Office.15%29.aspx) <br/> |[Método UserConfiguration. Delete](https://msdn.microsoft.com/library/exchange/microsoft.exchange.webservices.data.userconfiguration.delete%28v=exchg.80%29.aspx) <br/> |Exchange 2010  <br/> |Elimina un elemento asociado a la carpeta y lo mueve al contenedor.  <br/> |
|[Operación CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> |[Método appointment. Accept](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.accept%28v=exchg.80%29.aspx) <br/><br/>[Método appointment. AcceptTentatively](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[Método appointment. CancelMeeting](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.cancelmeeting%28v=exchg.80%29.aspx)<br/><br/>[Appointment. declinar](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.appointment.decline%28v=exchg.80%29.aspx)<br/><br/>[Método MeetingRequest. Accept](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.accept%28v=exchg.80%29.aspx)<br/><br/>[Método MeetingRequest. AcceptTentatively](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.accepttentatively%28v=exchg.80%29.aspx)<br/><br/>[Método MeetingRequest. decline](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.meetingrequest.decline%28v=exchg.80%29.aspx) <br/> |Exchange 2007  <br/> |Mueve indirectamente un elemento a la carpeta elementos eliminados cuando se envía una respuesta a una convocatoria de reunión o cuando se establece la respuesta en la cita.<br/><br/>No se ha establecido el tipo de eliminación en esta operación. Los mensajes de reunión se mueven a la carpeta elementos eliminados cuando el servicio procesa correctamente un objeto de respuesta.  <br/> |
   
También puede mover elementos a la carpeta elementos eliminados mediante reglas de la bandeja de entrada. Por ejemplo, puede [crear reglas](inbox-management-and-ews-in-exchange.md) que tengan una acción de eliminación. 
  
Algunos puntos que tener en cuenta sobre la eliminación de elementos:
  
- La eliminación de una ocurrencia de un elemento periódico no desencadena un movimiento a la carpeta elementos eliminados o al contenedor. Esto da como resultado una actualización del elemento maestro periódico de la serie periódica.
    
- No se pueden eliminar las carpetas predeterminadas del buzón.
    
- Evite eliminar reuniones o mensajes de reunión, como solicitudes de reunión o actualizaciones de reuniones. En su lugar, responda a estos elementos mediante objetos Response. De esta forma, los elementos de calendario asociados se actualizan para reflejar las acciones del persona que responde o el organizador.
    
- La clave de cambio de un elemento no se actualiza cuando el elemento se mueve a la carpeta elementos eliminados o eliminados.
    
- Si realiza una eliminación dura en un elemento y después llama a una [operación de SyncFolderHierarchy](https://msdn.microsoft.com/library/b31916b1-bc6c-4451-a475-b7c5417f752d%28Office.15%29.aspx) o [SYNCFOLDERHIERARCHY](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderhierarchy%28v=exchg.80%29.aspx) método de API administrada de EWS, o a una [operación SyncFolderItems](https://msdn.microsoft.com/library/7f0de089-8876-47ec-a871-df118ceae75d%28Office.15%29.aspx) o a un método [SyncFolderItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.syncfolderitems%28v=exchg.80%29.aspx) , se devolverá una entrada de cambio de **eliminación** . Si mueve un elemento a la carpeta elementos eliminados, se devuelve una entrada de cambio de **actualización** . Esto se debe a que el elemento o carpeta tendrá un nuevo valor de la propiedad [ParentFolderId](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) . [Obtenga más información acerca](mailbox-synchronization-and-ews-in-exchange.md) de la sincronización si la sincronización de elementos eliminados forma parte de su escenario. 
    
## <a name="find-out-more-about-deleting-items"></a>Obtener más información sobre cómo eliminar elementos
<a name="findoutmore"> </a>

- [Notificaciones de extracción para eventos de buzón relacionados con la eliminación de EWS en Exchange](pull-notifications-for-ews-deletion-related-mailbox-events-in-exchange.md)
    
- [Administración de errores relacionados con la eliminación en EWS en Exchange](handling-deletion-related-errors-in-ews-in-exchange.md)
    
## <a name="see-also"></a>Vea también

- [Carpetas y elementos de EWS en Exchange](folders-and-items-in-ews-in-exchange.md)    
- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)    
- [Carpeta elementos recuperables](https://technet.microsoft.com/library/ee364755.aspx)    
- [Recuperación de un único elemento en Exchange Server 2010](https://blogs.technet.com/b/exchange/archive/2009/09/25/3408389.aspx#_Single_Item_Recovery)    
- [Exchange 2013: eliminar una serie periódica mediante programación desde servidores de Exchange](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-a-e1c7b89d)    
- [Exchange 2013: eliminar tareas de una cuenta en servidores de Exchange mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-tasks-13824637)    
- [Exchange 2013: carpetas vacías en los servidores de Exchange mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Empty-6487df37)    
- [Exchange 2013: eliminar carpetas mediante programación desde servidores de Exchange](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-aa1a5823)    
- [Exchange 2013: eliminar muchos elementos de servidores de Exchange mediante programación](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-many-064f8760)    
- [Exchange 2013: eliminar contactos mediante programación desde servidores de Exchange](https://code.msdn.microsoft.com/exchange/Exchange-2013-Delete-3b8b0640)    
- [Eliminar citas y cancelar reuniones mediante EWS en Exchange](how-to-delete-appointments-and-cancel-meetings-by-using-ews-in-exchange.md)    
- [Administración de la configuración de aplicaciones persistentes mediante EWS en Exchange](how-to-manage-persistent-application-settings-by-using-ews-in-exchange.md)
    

