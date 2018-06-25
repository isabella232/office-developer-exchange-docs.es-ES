---
title: Identificadores EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 39b6b20b-e081-4347-9e15-9b8cf829fdf0
description: Obtenga información acerca de identificadores en Exchange y cómo se pueden usar en la API administrada de EWS y las aplicaciones de EWS.
ms.openlocfilehash: c09b54c8ec4f443a64f8222094ccf0a5e1f750e7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763027"
---
# <a name="ews-identifiers-in-exchange"></a>Identificadores EWS en Exchange

Obtenga información acerca de identificadores en Exchange y cómo se pueden usar en la API administrada de EWS y las aplicaciones de EWS.
  
Cada objeto en el almacén de Exchange tiene un identificador único. Puede usar un identificador de objeto para hacer referencia al objeto y para distinguirlo de otros objetos. Los dos identificadores más comunes que pueden funcionar con son la carpeta y los identificadores de elemento. 
  
Para entender los identificadores y cómo son importantes para su aplicación, es útil comprender la relación entre los objetos de Exchange. La API administrada de EWS o la aplicación de EWS se comunica con Exchange, se trabaja con una jerarquía de objetos que incluye el buzón de correo, carpeta y objetos de elemento. Un almacén puede ser uno de estos tipos de objeto. Con más frecuencia, es un buzón de correo en el servidor de Exchange, pero también puede ser una carpeta pública en el servidor de Exchange. (Tenga en cuenta que en Exchange Online, Exchange Online como parte de Office 365 y las versiones de Exchange a partir de Exchange 2013, las carpetas públicas son cualquier otro tipo de buzón de correo y no otro tipo de almacenamiento). El almacén contiene las carpetas y las carpetas que contienen elementos y cada una de estas carpetas y elementos tiene un identificador, como se muestra en la ilustración siguiente. 
  
**En la figura 1. Buzón de correo, carpeta y jerarquía de artículos**

![Ilustración que muestra la jerarquía de objetos del buzón. El buzón está en el nivel superior con la bandeja de entrada en el siguiente nivel. El diagrama muestra una carpeta que contiene los correos electrónicos. Se enumeran los identificadores y las claves de cambio para cada objeto, y aparecen acortadas.](media/Ex15_Identifier_diagram.png)
  
## <a name="ews-identifiers"></a>Identificadores EWS
<a name="bk_CommonIdentifiers"> </a>

Identificadores de EWS se utiliza para las carpetas y los elementos se denominan identificadores EWS o EwsIds. EwsIds puede encontrarse en muchos objetos diferentes dentro de EWS, pero se denominan algo diferente para los distintos objetos. Debido a que es posible que utilizar estos objetos en la aplicación, desea comprender cómo se relacionan con los identificadores de estos objetos a la EwsId. 
  
Son aplicables a la API administrada de EWS así como los identificadores de EWS. En la API administrada de EWS, los identificadores son las propiedades de los objetos y se administran internamente para asignar a los elementos EWS.
  
**La tabla 1. Identificadores de objeto de EWS**

|**Object**|**Identificador**|**¿Cómo se relaciona EwsId?**|
|:-----|:-----|:-----|
|[CalendarItem](http://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |El elemento secundario de [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) contiene el identificador único del elemento de calendario.  <br/> |El elemento secundario de [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) es el mismo que el EwsId para este elemento.  <br/> |
|[ConversationId](http://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |El atributo **Id** contiene el identificador de la conversación que forma parte de este elemento.  <br/> |El atributo **Id** es el mismo que el EwsId para este elemento.  <br/> |
|[AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |Proporciona el identificador único de los datos adjuntos. El atributo [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx) contiene el identificador único del elemento de almacén raíz al que se adjunta los datos adjuntos.  <br/> |Los datos adjuntos pueden ser otros elementos en el almacén de Exchange, en cuyo caso el [AttachmentId](http://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) es la misma que la EwsId. En todos los casos, el [RootItemId](http://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx) es un EwsId debido a que hace referencia a un elemento en el almacén.  <br/> |
|[PersonaId](http://msdn.microsoft.com/library/eec3a468-afd5-4d72-a61e-cd1964fb686c%28Office.15%29.aspx) <br/> |El atributo **Id** devuelve una cadena que contiene el identificador de la persona.  <br/> |El atributo **Id** es el mismo que el EwsId para el rol.  <br/> |
|[ID de contacto](http://msdn.microsoft.com/library/86f66275-1e39-48ed-bd89-ac3bffc465a7%28Office.15%29.aspx) <br/> |El atributo **Id** devuelve una cadena que contiene el identificador del contacto.  <br/> |El atributo **Id** es el mismo que el EwsId para el contacto.  <br/> |
|[GroupId](http://msdn.microsoft.com/library/656d9b9a-8a65-4a75-8466-5b0d96512dab%28Office.15%29.aspx) <br/> |El atributo **Id** devuelve una cadena que contiene el identificador del grupo.  <br/> |El atributo **Id** es el mismo que el EwsId para el grupo.  <br/> |
|[AssociatedCalendarItemId](http://msdn.microsoft.com/library/5b29898c-ea59-4e6a-914c-c011ec754032%28Office.15%29.aspx) <br/> |El atributo **Id** identifica el elemento de calendario que está asociado con un [MeetingMessage](http://msdn.microsoft.com/library/c95956a8-7505-44b4-bea4-11d1f5182796%28Office.15%29.aspx), [MeetingRequest](http://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx), [MeetingResponse](http://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)o [MeetingCancellation](http://msdn.microsoft.com/library/a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea%28Office.15%29.aspx).  <br/> |El atributo **Id** es el mismo que el EwsId para el elemento de calendario.  <br/> |
|[UserConfigurationProperties](http://msdn.microsoft.com/library/c143a6ec-62ad-4d48-b844-b1ad88054bc1%28Office.15%29.aspx) <br/> |El valor de **identificador** de este elemento especifica la propiedad del identificador.  <br/> |Este identificador no asigna directamente a la EwsId debido a que un identificador de la propiedad y no un elemento.  <br/> |
|[OccurrenceItemId](http://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) <br/> |El atributo **RecurringMasterId** identifica al patrón de un elemento periódico.  <br/> |El valor de **OccurrenceItemId** no se asignan directamente a la EwsId, pero la **RecurringMasterId** no debido a que hace referencia al objeto de nivel superior del elemento periódico.  <br/> |
|[StoreEntryId](http://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |Contiene el identificador de almacén de Exchange de un elemento.  <br/> |El valor de **StoreEntryId** no se asigna a la EwsId, pero da el identificador del almacén donde se conservan los elementos.  <br/> |
   
## <a name="working-with-identifiers"></a>Trabajar con identificadores
<a name="bk_WorkingWithIdentifiers"> </a>

El servidor de Exchange administra identificadores en una gran cantidad de diferentes formas. Tenga en cuenta lo siguiente cuando se desarrolla la API administrada de EWS o la aplicación de EWS:
  
- El valor del elemento **ItemID** para carpetas y elementos distingue mayúsculas de minúsculas. Si observa el identificador de elemento de una carpeta o elemento que es devuelto por la [operación FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método de la API administrada de EWS [FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) ), es posible que piense que es un duplicado de otro identificador de elemento; Sin embargo, uno o más caracteres en los identificadores de elementos para los dos artículos tendrá un caso diferente. 
    
- Si va a almacenar el identificador de elemento en una base de datos para recuperar más adelante, se recomienda que el tamaño del campo ser de 512 bytes, para que sea suficientemente grande para contener el GUID.
    
- No dé por sentado que su identificador siempre será válido si necesita recuperar el elemento en un momento posterior. Si se mueve un elemento en el almacén, puede cambiar el identificador debido a la forma en que se administra un movimiento. En realidad se copia un elemento, y se genera un nuevo identificador y, a continuación, [se elimina el elemento original](deleting-items-by-using-ews-in-exchange.md).
    
- Los identificadores de Exchange son opacos. Por ejemplo, se crea el EwsId de varias partes de información que no son importantes para usted como el programador, pero que son importantes para Exchange.
    
- Cuando se trabaja con elementos de Exchange, otro valor que deben tenerse en cuenta es el atributo **ChangeKey** . Este valor, además del identificador de elemento, se usa para realizar un seguimiento del estado de un elemento. Cada vez que se cambia un elemento, se genera una nueva clave de cambio. Cuando se realiza una [operación UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx), por ejemplo, puede usar el atributo **ChangeKey** para permitir que el servidor sabe que la actualización se aplica a la versión más reciente del elemento. Si otra aplicación realizado un cambio en el elemento que se va a actualizar, no coincidirán con las claves de cambio y no podrá realizar la actualización. 
    
## <a name="distinguished-folder-ids"></a>Carpeta distintivo identificadores
<a name="bk_DistinguishedFolderIds"> </a>

Exchange incluye una serie de carpetas del buzón predefinidos, cada uno de los cuales se le asigna un identificador, conocido como el identificador de carpeta distintivo. Estos se definen mediante la enumeración de la API administrada de EWS [WellKnownFolderName](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y el elemento EWS [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) . Puede usar estos identificadores de las carpetas distintivo con más facilidad hacer referencia a una de las carpetas predefinidas. Por ejemplo, para la carpeta Bandeja de entrada, puede usar simplemente "Bandeja de entrada" para el identificador, en lugar de determinar el identificador de la carpeta. 
  
Otras carpetas que se crean para organizar los elementos de correo electrónico también tienen un identificador único para esa carpeta. El ID no cambia incluso si cambiar otras propiedades en la carpeta.
  
Puede usar los identificadores de carpeta distintivo como un punto de entrada para el acceso de delegado. Cuando se inicia el acceso delegado, busca elementos o carpetas y proporcionar el identificador de carpeta distintivo para especificar dónde buscar. Cuando un usuario delegado obtiene acceso al servidor, un elemento de [buzón de correo](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) que es un elemento secundario del elemento **DistinguishedFolderId** se usa para especificar explícitamente el buzón para el delegado para obtener acceso a. 
  
## <a name="handling-errors"></a>Controlar errores
<a name="bk_DealingWithErrors"> </a>

Cada programa está enlazado a obtener un error cada ahora y, a continuación, y aplicaciones basadas en EWS no son una excepción (juego de palabras pensado). Es posible que reciba algunos errores relacionados con el identificador en el elemento EWS [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) o como parte de la de la enumeración de la API administrada de EWS [depuracuión puede contener](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) . 
  
Pueden producirse los siguientes errores en la API administrada de EWS o la aplicación de EWS. Si está trabajando con una aplicación de API administrada de EWS, los errores suelen ser problemas con los valores de propiedad; para las aplicaciones de EWS, los errores están asociados con los valores del elemento XML u operaciones.
  
**Tabla 2. Errores relacionados con el identificador**

|**Error**|**Se produce cuando...**|**Descripción**|
|:-----|:-----|:-----|
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |El valor de la **OccurenceID** no corresponde a un elemento periódico de calendario válido.  <br/> |El valor de **OccurenceId** que se especificó en la solicitud podría ser válido en la estructura, pero la solicitud no pudo coinciden a un patrón periódico existente. Puede que se quite el elemento periódico del calendario. Compruebe que el elemento aún existe y que está usando el identificador correcto.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |El atributo **RecurringMasterId** no corresponde a una repetición válida del elemento de **repetición** .  <br/> |El valor de **RecurringMasterId** que se especificó en la solicitud podría ser válido en la estructura, pero la solicitud no pudo coinciden a una ocurrencia del elemento existente. Es posible que se quiten la aparición del elemento desde el calendario. Compruebe que el elemento aún existe y que está usando el identificador correcto.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |El **identificador** que se pasó representa una carpeta en lugar de un elemento.  <br/> |El identificador puede ser válido en el formato, pero no lo que el servidor que se esperaba para la operación. Compruebe que se hace referencia el identificador correcto para la operación.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |El **identificador** que se pasó en representa un elemento en lugar de una carpeta.  <br/> |El identificador puede ser válido en el formato, pero no lo que el servidor que se esperaba para la operación. Compruebe que se hace referencia el **identificador** correcto para la operación.  <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Debe proporcionar una clave de cambio válido al realizar determinadas operaciones de actualización.  <br/> |O bien se omite un valor **ChangeKey** cuando se solicita una actualización o la clave de cambio era incorrecta. Compruebe que tiene la clave de cambio correcta cuando se realizan las operaciones de actualización.  <br/> |
|ErrorInvalidAttachmentId  <br/> |Los datos adjuntos no se encuentra dentro de la colección attachments del elemento.  <br/> |Es posible que reciba este código de respuesta si tiene un **identificador** de datos adjuntos y, a continuación, se eliminan los datos adjuntos y se intenta llamar a la [operación GetAttachment](http://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) en el identificador de datos adjuntos. Compruebe que los datos adjuntos existe en la colección de datos adjuntos.  <br/> |
|ErrorInvalidChangeKey  <br/> |Se ha pasado una clave de cambio no válido.  <br/> |Tenga en cuenta que muchas operaciones y métodos no requieren una clave de cambio que se pasan. Sin embargo, si tiene que proporcionar una clave de cambio, debe ser válido, aunque no necesariamente tiene que estar actualizada.  <br/> |
|ErrorInvalidFolderId  <br/> |El **identificador** de la carpeta está dañado.  <br/> |Asegúrese de que tiene un identificador con formato correcto y es válido.  <br/> |
|ErrorInvalidId  <br/> |La estructura de la clave de **identificador** o el cambio es incoherente internamente.  <br/> |Exchange detectó un problema con el **identificador de** una vez que se ha analizado. Es posible que ha habido un error en la conversión. Esto puede suceder, por ejemplo, si tiene un **IdFormatType.HexEntryId** para un elemento de Outlook, pero lo convierte a un pensando EwsId era un formato **IdFormatType.EntryId** . Asegúrese de que se utiliza el tipo de conversión correcta.  <br/> |
|ErrorInvalidIdEmpty  <br/> |La aplicación especifica un **identificador** que está vacío.  <br/> |La aplicación que se pasa en una cadena vacía para el identificador. Asegúrese de que tiene un identificador con formato correcto y es válido.  <br/> |
|ErrorInvalidIdMalformed  <br/> |La estructura del **identificador** es incoherente internamente.  <br/> |Exchange detectó un problema con el **identificador de** una vez que se ha analizado. Es posible que el identificador no se ha convertido correctamente. Asegúrese de que se utiliza el tipo de conversión correcta.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Se especificó una carpeta o elemento **identificador** que está usando el formato de Exchange 2007 para una solicitud con una versión de Exchange 2007 SP1 o posterior.  <br/> |No se puede usar los identificadores de 2007 de Exchange en Exchange 2007 SP1 o posterior solicitudes. Debe usar la operación de EWS [ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) o el método de la API administrada de EWS [ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) para convertirlos en primer lugar.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |La propiedad **AttachmentId** no hace referencia a un elemento de datos adjuntos.  <br/> |El identificador puede ser válido en el formato, pero no lo que el servidor que se esperaba para la operación. Compruebe que se hace referencia el identificador correcto para la operación.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Un contacto en su buzón de correo está dañado.  <br/> |La operación de EWS [ResolveNames](http://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) o el método de la API administrada de EWS [ResolveName](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) devuelve uno o varios identificadores, pero no son válidos. Es posible que necesite volver a crear el contacto.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |La estructura del **identificador** es incoherente internamente.  <br/> |Exchange detectó un problema con el **identificador de** una vez que se ha analizado. Es posible que el **identificador** no se ha convertido correctamente. Asegúrese de que se utiliza el tipo de conversión correcta.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Las jerarquías de los datos adjuntos superen el máximo de 255 niveles de profundidad.  <br/> |El valor de la propiedad **AttachmentId** que se especificó en la solicitud podría ser válido en la estructura, pero los datos adjuntos solicitado están demasiado profundo en la jerarquía. Es posible que el código ha intentado adjuntar un elemento más allá del límite de 255 niveles.  <br/> |
|ErrorInvalidImContactId  <br/> |Este error puede devolverse cuando el contacto no se encuentra en el grupo de mensajería instantánea cuando se usa la [operación RemoveImContactFromGroup](http://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx). Este error se aplica a los clientes que estén destinados a Exchange Online y versiones de Exchange a partir de Exchange 2013.  <br/> |El valor de la propiedad **ContactId** que se especificó en la solicitud podría ser válido en la estructura, pero no hay contactos en el buzón de correo que coincidan con esta estructura. Es posible que el contacto se han quitado ya.  <br/> |
|ErrorInvalidImGroupId  <br/> |Este error puede devolverse cuando el grupo no se encuentra en el buzón de correo cuando se utiliza la [operación RemoveImGroup](http://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx). Este error se aplica a los clientes que estén destinados a Exchange Online y versiones de Exchange a partir de Exchange 2013.  <br/> |El valor de la propiedad **GroupId** que se especificó en la solicitud podría ser válido en la estructura, pero no hay grupos en el buzón de correo coincide con esta estructura. Es posible que se han quitado el grupo ya.  <br/> |
|ErrorInvalidReferenceItem  <br/> |El identificador del elemento que se hace referencia no es un **tipo de mensaje** o **ExchangeWebServices.CalendarItemTypeType**o uno de sus descendientes. Es el identificador de elemento de referencia para un objeto de **CalendarItemType** y el organizador intenta responder o responder a todos.  <br/> |El identificador puede ser válido en el formato, pero no lo que el servidor que se esperaba para la operación. Compruebe que se hace referencia el identificador correcto para la operación.  <br/> |
|ErrorMissingManagedFolderId  <br/> |La propiedad de los identificadores de directiva, la etiqueta de la propiedad 0x6732, para la carpeta está ausente.  <br/> |La carpeta está dañada. Considere la posibilidad de volver a crearla.  <br/> |
   
## <a name="converting-identifiers"></a>Convertir identificadores
<a name="bk_ConvertingIdentifiers"> </a>

Es posible que necesite convertir un identificador de un formato a otro. Por ejemplo, es posible que necesite convertir un identificador de EWS externa, como un identificador que procede de una conexión de MAPI, a un formato que puede usar la aplicación. Para ello, puede usar la operación de EWS [ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) o el método de la API administrada de EWS [ConvertId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) . 
  
Por ejemplo, un EntryID es un identificador único generado por el almacén de mensajes MAPI que se asigna el almacén cuando se guarda el elemento. Para usar un EntryID en su aplicación, primero se debe convertir a un EwsId. 
  
Outlook Web App usa su propia versión de identificadores, denominados OwaId, en las direcciones URL para obtener acceso a las carpetas y elementos. Si la aplicación necesita tener acceso a los elementos de Outlook Web App, debe convertir el OwaId en un EwsId.
  
Puede usar el método o la operación de **ConvertId** para convertir varios formatos de identificador diferente. 
  
**Tabla 3. Formatos de identificador convertible en Exchange**

|**Formato**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |El EwsId que se aplica a Exchange 2007.  <br/> |
|EwsId  <br/> |El EwsId que se aplica a Exchange Online y versiones de Exchange a partir de Exchange 2007 SP1.  <br/> |
|StoreId  <br/> |El identificador de almacén de Exchange donde se almacenan los elementos y carpetas.  <br/> |
|OwaId  <br/> |El identificador de Outlook Web App que se utiliza con Outlook Web App en Exchange 2007 y Exchange 2010.  <br/> > [!NOTE]> Exchange Online y versiones de Exchange a partir de Exchange 2013 usan el EwsId para Outlook Web App.           |
|Propiedad EntryId  <br/> |Un identificador MAPI que se conoce como la propiedad de **entrada del objeto** de un mensaje MAPI.  <br/> |
|HexEntryId  <br/> |Una representación codificada en hexadecimal de la propiedad de **entrada del objeto** que se usa para el identificador de evento del calendario de disponibilidad. También es el formato de identificador que usa Outlook.  <br/> |
   
## <a name="see-also"></a>Vea también


- [Desarrollo de clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)
    
- [Operación ConvertId](http://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)
    
- [Depuracuión puede contener (enumeración)](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx)
    
- [Eliminación de elementos con EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    

