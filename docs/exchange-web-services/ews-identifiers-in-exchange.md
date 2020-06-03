---
title: Identificadores de EWS en Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.assetid: 39b6b20b-e081-4347-9e15-9b8cf829fdf0
description: Obtenga información sobre los identificadores de Exchange y cómo puede usarlos en la API administrada de EWS y en las aplicaciones de EWS.
localization_priority: Priority
ms.openlocfilehash: 9fa2e31a3c67b0b4291b1e3f32a775655e2bf80a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528429"
---
# <a name="ews-identifiers-in-exchange"></a>Identificadores de EWS en Exchange

Obtenga información sobre los identificadores de Exchange y cómo puede usarlos en la API administrada de EWS y en las aplicaciones de EWS.
  
Cada objeto del almacén de Exchange tiene un identificador único. Puede usar el identificador de un objeto para hacer referencia al objeto y para distinguirlo de otros objetos. Los dos identificadores más comunes con los que puede trabajar son los identificadores de carpeta y de elemento. 
  
Para comprender los identificadores y el modo en que son importantes para la aplicación, es útil comprender la relación entre los objetos de Exchange. Cuando la aplicación de la API administrada de EWS o EWS se comunique con Exchange, trabajará con una jerarquía de objetos que incluye los objetos de elementos, carpetas y buzones de correo. Un almacén puede ser uno de estos tipos de objeto. Por lo general, es un buzón de correo en el servidor de Exchange, pero también puede ser una carpeta pública en el servidor de Exchange. (Tenga en cuenta que en Exchange Online, Exchange online como parte de Office 365 y las versiones de Exchange que comienzan con Exchange 2013, las carpetas públicas son solo otro tipo de buzón y no son un tipo de almacén diferente). El almacén contiene carpetas y las carpetas contienen elementos, y cada una de estas carpetas y elementos tiene un identificador, tal como se muestra en la figura siguiente. 
  
**Figura 1. Jerarquía de buzones de correo, carpeta y elementos**

![Ilustración que muestra la jerarquía de objetos del buzón. El buzón está en el nivel superior con la bandeja de entrada en el siguiente nivel. El diagrama muestra una carpeta que contiene los correos electrónicos. Se enumeran los identificadores y las claves de cambio para cada objeto, y aparecen acortadas.](media/Ex15_Identifier_diagram.png)
  
## <a name="ews-identifiers"></a>Identificadores de EWS
<a name="bk_CommonIdentifiers"> </a>

Los identificadores que EWS usa para carpetas y elementos se denominan identificadores EWS o EwsIds. EwsIds puede encontrarse en muchos objetos diferentes dentro de EWS, pero se les llama de diferentes objetos. Como puede usar estos objetos en la aplicación, es conveniente que comprenda cómo se relacionan los identificadores de estos objetos con el EwsId. 
  
Los identificadores de EWS también se aplican a la API administrada de EWS. En la API administrada de EWS, los identificadores son propiedades de los objetos y se administran de forma interna para asignarlos a los elementos de EWS.
  
**Tabla 1. Identificadores de objeto en EWS**

|**Objeto**|**Identificador**|**¿Cómo se relaciona con EwsId?**|
|:-----|:-----|:-----|
|[CalendarItem](https://msdn.microsoft.com/library/b0c1fd27-b6da-46e5-88b8-88f00c71ba80%28Office.15%29.aspx) <br/> |El elemento secundario [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) contiene el identificador único del elemento de calendario.  <br/> |El elemento secundario [Itemid](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) es el mismo que el EwsId de este elemento.  <br/> |
|[ConversationId](https://msdn.microsoft.com/library/d5f1ddb3-9af3-4677-a6ba-111b304a951e%28Office.15%29.aspx) <br/> |El atributo **ID** contiene el identificador de la conversación a la que pertenece este elemento.  <br/> |El atributo **ID** es el mismo que el EwsId de este elemento.  <br/> |
|[AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) <br/> |Proporciona el identificador único de los datos adjuntos. El atributo [RootItemId](https://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx) contiene el identificador único del elemento de almacén raíz al que se adjuntan los datos adjuntos.  <br/> |Los datos adjuntos pueden ser otros elementos del almacén de Exchange, en cuyo caso el [AttachmentId](https://msdn.microsoft.com/library/55a5fd77-60d1-40fa-8144-770600cedc6a%28Office.15%29.aspx) es el mismo que el EwsId. En todos los casos, el [RootItemId](https://msdn.microsoft.com/library/f613c705-17ce-48ce-aa64-4dc2cea25e31%28Office.15%29.aspx) es un EwsId porque hace referencia a un elemento del almacén.  <br/> |
|[PersonaId](https://msdn.microsoft.com/library/eec3a468-afd5-4d72-a61e-cd1964fb686c%28Office.15%29.aspx) <br/> |El atributo **ID** devuelve una cadena que contiene el identificador del rol.  <br/> |El atributo **ID** es el mismo que el EwsId del rol.  <br/> |
|[Contacto](https://msdn.microsoft.com/library/86f66275-1e39-48ed-bd89-ac3bffc465a7%28Office.15%29.aspx) <br/> |El atributo **ID** devuelve una cadena que contiene el identificador del contacto.  <br/> |El atributo **ID** es el mismo que el EwsId del contacto.  <br/> |
|[GroupId](https://msdn.microsoft.com/library/656d9b9a-8a65-4a75-8466-5b0d96512dab%28Office.15%29.aspx) <br/> |El atributo **ID** devuelve una cadena que contiene el identificador del grupo.  <br/> |El atributo **ID** es el mismo que el EwsId del grupo.  <br/> |
|[AssociatedCalendarItemId](https://msdn.microsoft.com/library/5b29898c-ea59-4e6a-914c-c011ec754032%28Office.15%29.aspx) <br/> |El atributo **ID** identifica el elemento de calendario que está asociado con [MeetingMessage](https://msdn.microsoft.com/library/c95956a8-7505-44b4-bea4-11d1f5182796%28Office.15%29.aspx), [MeetingRequest](https://msdn.microsoft.com/library/c44f8804-a355-473d-a837-48cc91617251%28Office.15%29.aspx), [MeetingResponse](https://msdn.microsoft.com/library/9f798e79-dafd-4d4d-9967-95fd8e5c0502%28Office.15%29.aspx)o [MeetingCancellation](https://msdn.microsoft.com/library/a9c61f7f-2ecd-4b21-9dce-24d9f61aeeea%28Office.15%29.aspx).  <br/> |El atributo **ID** es el mismo que el EwsId para el elemento de calendario.  <br/> |
|[UserConfigurationProperties](https://msdn.microsoft.com/library/c143a6ec-62ad-4d48-b844-b1ad88054bc1%28Office.15%29.aspx) <br/> |El valor de **ID** de este elemento especifica la propiedad Identifier.  <br/> |Este identificador no se asigna directamente a EwsId, ya que es un identificador de propiedad y no un elemento.  <br/> |
|[OccurrenceItemId](https://msdn.microsoft.com/library/4a15bbc3-5b93-4193-b9ec-da32f0a9a552%28Office.15%29.aspx) <br/> |El atributo **RecurringMasterId** identifica el patrón de un elemento periódico.  <br/> |El valor **OccurrenceItemId** no se asigna directamente a EwsId, pero el **RecurringMasterId** sí que hace referencia al objeto de nivel superior del elemento periódico.  <br/> |
|[StoreEntryId](https://msdn.microsoft.com/library/f536e264-8c4d-4cc5-bab8-22a4fa38de39%28Office.15%29.aspx) <br/> |Contiene el identificador de almacén de Exchange de un elemento.  <br/> |El valor **StoreEntryId** no se asigna a EwsId, pero proporciona el identificador del almacén donde se conservan los elementos.  <br/> |
   
## <a name="working-with-identifiers"></a>Trabajar con identificadores
<a name="bk_WorkingWithIdentifiers"> </a>

El servidor de Exchange controla los identificadores de muchas maneras diferentes. Al desarrollar la API administrada de EWS o la aplicación EWS, tenga en cuenta lo siguiente:
  
- El valor del elemento **Itemid** para carpetas y elementos distingue mayúsculas de minúsculas. Si observa el identificador de elemento de una carpeta o elemento que devuelve la [operación FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) (o el método [FINDITEMS](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) de la API administrada de EWS), es posible que piense que es un duplicado de otro identificador de elemento; sin embargo, uno o más caracteres de los identificadores de elemento para los dos elementos tendrán un caso diferente. 
    
- Si va a almacenar el identificador de elemento en una base de datos para recuperarla más adelante, se recomienda que el tamaño del campo sea de 512 bytes, de modo que sea lo suficientemente grande como para contener el GUID.
    
- No asuma que el identificador de elemento siempre será válido si necesita recuperar el elemento en un momento posterior. Si un elemento se mueve en el almacén, el identificador puede cambiar debido a la forma en que se controla el movimiento. Realmente se copia un elemento y se genera un nuevo identificador y, a continuación, [se elimina el elemento original](deleting-items-by-using-ews-in-exchange.md). Tenga en cuenta que los identificadores de carpeta son inmutables y no cambian cuando se mueven en la tienda.
    
- Los identificadores de Exchange son opacos. Por ejemplo, el EwsId se crea a partir de varios datos que no son importantes para usted como desarrollador, pero que son importantes para Exchange.
    
- Al trabajar con elementos en Exchange, otro valor que se debe tener en cuenta es el atributo **changekey** . Este valor, además del identificador de elemento, se usa para realizar un seguimiento del estado de un elemento. Cada vez que se cambia un elemento, se genera una nueva clave de cambio. Al realizar una [operación UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx), por ejemplo, puede usar el atributo **changekey** para que el servidor sepa que la actualización se está aplicando a la versión más reciente del elemento. Si otra aplicación realizó un cambio en el elemento que está actualizando, las claves de cambio no coincidirán y no podrá realizar la actualización. 
    
## <a name="distinguished-folder-ids"></a>Identificadores de carpeta distintivos
<a name="bk_DistinguishedFolderIds"> </a>

Exchange incluye varias carpetas de buzones predefinidas, a cada una de las cuales se ha asignado un identificador, conocido como el identificador de carpeta distintivo. Se definen mediante la enumeración de API administrada de EWS de [WellKnownFolderName](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) y el elemento EWS de [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) . Puede usar estos identificadores de carpeta distintivo para hacer referencia más fácilmente a una de las carpetas predefinidas. Por ejemplo, para la carpeta Bandeja de entrada, puede usar simplemente "bandeja de entrada" para el identificador, en lugar de determinar el identificador de la carpeta. 
  
Otras carpetas que cree para organizar los elementos de correo electrónico también tienen un identificador que es único en esa carpeta. El identificador no cambia incluso si se cambian otras propiedades de la carpeta.
  
Puede usar identificadores de carpeta distintivos como punto de entrada para el acceso delegado. Cuando se inicia el acceso delegado, se buscan elementos o carpetas y se proporciona el identificador de carpeta distintivo para especificar dónde buscar. Cuando un usuario delegado obtiene acceso al servidor, se usa un elemento [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) que es un elemento secundario del elemento **DistinguishedFolderId** para especificar explícitamente el buzón de correo al que tiene acceso el delegado. 
  
## <a name="handling-errors"></a>Administración de errores
<a name="bk_DealingWithErrors"> </a>

Todos los programas están enlazados para obtener un error cada ahora y, a continuación, y las aplicaciones basadas en EWS no son una excepción (pun pretendedas). Es posible que reciba algunos errores relacionados con el identificador en el elemento EWS de [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) o como parte de la enumeración de la API administrada de EWS de [ServiceError](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) . 
  
Los siguientes errores pueden producirse en la API administrada de EWS o en la aplicación de EWS. Si está trabajando con una aplicación de API administrada de EWS, los errores suelen ser problemas con los valores de las propiedades; para las aplicaciones de EWS, los errores están asociados a operaciones o valores de elementos XML.
  
**Tabla 2. Errores relacionados con los identificadores**

|**Error**|**Se produce cuando...**|**Descripción**|
|:-----|:-----|:-----|
|ErrorCalendarCannotUseIdForOccurrenceId  <br/> |El valor de **OccurenceID** no corresponde a un elemento de calendario periódico válido.  <br/> |El valor de **OccurenceId** que se especificó en la solicitud podría ser válido en la estructura, pero la solicitud no pudo hacer coincidir con un patrón recurrente existente. El elemento periódico puede quitarse del calendario. Compruebe que el elemento todavía existe y que usa el identificador correcto.  <br/> |
|ErrorCalendarCannotUseIdForRecurringMasterId  <br/> |El atributo **RecurringMasterId** no se corresponde con una ocurrencia válida del elemento **OccurrenceId** .  <br/> |El valor de **RecurringMasterId** que se especificó en la solicitud podría ser válido en la estructura, pero la solicitud no pudo hacer coincidir con una ocurrencia del elemento existente. Es posible que se elimine del calendario la ocurrencia del elemento. Compruebe que el elemento todavía existe y que usa el identificador correcto.  <br/> |
|ErrorCannotUseFolderIdForItemId  <br/> |El **identificador** que se ha pasado representa una carpeta en lugar de un elemento.  <br/> |El identificador puede tener un formato válido, pero no el servidor que esperaba para la operación. Compruebe que hace referencia al identificador correcto para la operación.  <br/> |
|ErrorCannotUseItemIdForFolderId  <br/> |El **identificador** que se ha pasado representa un elemento en lugar de una carpeta.  <br/> |El identificador puede tener un formato válido, pero no el servidor que esperaba para la operación. Compruebe que hace referencia al **identificador** correcto para la operación.  <br/> |
|ErrorChangeKeyRequiredForWriteOperations  <br/> |Se debe proporcionar una clave de cambio válida al realizar determinadas operaciones de actualización.  <br/> |Ha omitido un valor de **changekey** cuando solicitó una actualización o la clave de cambio era incorrecta. Compruebe que tiene la clave de cambio correcta al realizar operaciones de actualización.  <br/> |
|ErrorInvalidAttachmentId  <br/> |No se encontraron los datos adjuntos dentro de la colección de datos adjuntos del elemento.  <br/> |Puede recibir este código de respuesta si tiene un **identificador** de datos adjuntos y, a continuación, se eliminan los datos adjuntos e intenta llamar a la [operación GETATTACHMENT](https://msdn.microsoft.com/library/24d10a15-b942-415e-9024-a6375708f326%28Office.15%29.aspx) en el identificador de datos adjuntos. Compruebe que los datos adjuntos existen en la colección Attachments.  <br/> |
|ErrorInvalidChangeKey  <br/> |Se ha pasado una clave de cambio no válida.  <br/> |Tenga en cuenta que muchas operaciones y métodos no requieren que se pase una clave de cambio. Sin embargo, si se proporciona una clave de cambio, debe ser válida, aunque no tiene que estar actualizada necesariamente.  <br/> |
|ErrorInvalidFolderId  <br/> |El **identificador** de la carpeta está dañado.  <br/> |Asegúrese de que tiene un identificador válido y con formato correcto.  <br/> |
|ErrorInvalidId  <br/> |La estructura del **identificador** o de la clave de cambio es internamente incoherente.  <br/> |Exchange detectó un problema con el **identificador** después de su análisis. Es posible que se haya producido un error en la conversión. Esto puede ocurrir, por ejemplo, si tiene un **IdFormatType. HexEntryId** para un elemento en Outlook, pero lo convierte a un EwsId pensando que es un formato **IdFormatType. EntryId** . Asegúrese de usar el tipo de conversión correcto.  <br/> |
|ErrorInvalidIdEmpty  <br/> |La aplicación especificó un **identificador** que está vacío.  <br/> |La aplicación pasó en una cadena vacía para el identificador. Asegúrese de que tiene un identificador válido y con formato correcto.  <br/> |
|ErrorInvalidIdMalformed  <br/> |La estructura del **identificador** es internamente incoherente.  <br/> |Exchange detectó un problema con el **identificador** después de su análisis. Es posible que el identificador no se haya convertido correctamente. Asegúrese de usar el tipo de conversión correcto.  <br/> |
|ErrorInvalidIdMalformedEwsLegacyIdFormat  <br/> |Se ha especificado un **identificador** de carpeta o elemento que usa el formato de Exchange 2007 para una solicitud con una versión de Exchange 2007 SP1 o posterior.  <br/> |No puede usar identificadores de Exchange 2007 en solicitudes de Exchange 2007 SP1 o posteriores. Debe usar la operación de EWS de [ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) o el método de la API administrada de EWS de [ConvertId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) para convertirlos primero.  <br/> |
|ErrorInvalidIdNotAnItemAttachmentId  <br/> |La propiedad **AttachmentId** no hace referencia a datos adjuntos de elemento.  <br/> |El identificador puede tener un formato válido, pero no el servidor que esperaba para la operación. Compruebe que hace referencia al identificador correcto para la operación.  <br/> |
|ErrorInvalidIdReturnedByResolveNames  <br/> |Un contacto del buzón está dañado.  <br/> |La operación de EWS de [ResolveNames](https://msdn.microsoft.com/library/6b4eb4b3-9ad6-4804-a09f-7e20cfea4dbb%28Office.15%29.aspx) o el método de la API administrada de EWS de [ResolveName](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.resolvename%28v=exchg.80%29.aspx) devolvieron uno o más identificadores, pero no son válidos. Es posible que deba volver a crear el contacto.  <br/> |
|ErrorInvalidIdStoreObjectIdTooLong  <br/> |La estructura del **identificador** es internamente incoherente.  <br/> |Exchange detectó un problema con el **identificador** después de su análisis. Es posible que el **identificador** no se haya convertido correctamente. Asegúrese de usar el tipo de conversión correcto.  <br/> |
|ErrorInvalidIdTooManyAttachmentLevels  <br/> |Las jerarquías de datos adjuntos superan el máximo de 255 niveles de profundidad.  <br/> |El valor de la propiedad **AttachmentId** que se especificó en la solicitud podría ser válido en la estructura, pero los datos adjuntos solicitados son demasiado profundos en la jerarquía. Es posible que el código haya intentado adjuntar un elemento más allá del límite de 255 niveles.  <br/> |
|ErrorInvalidImContactId  <br/> |Este error puede devolverse cuando no se encuentra el contacto en el grupo de mensajería instantánea cuando usa la [operación RemoveImContactFromGroup](https://msdn.microsoft.com/library/a190bbec-c71b-4e6a-880b-55854c724d8c%28Office.15%29.aspx). Este error se aplica a los clientes destinados a Exchange Online y versiones de Exchange a partir de Exchange 2013.  <br/> |El valor de la propiedad **ContactId** que se especificó en la solicitud podría ser válido en estructura, pero ningún contacto en el buzón coincide con esta estructura. Es posible que el contacto ya se haya quitado.  <br/> |
|ErrorInvalidImGroupId  <br/> |Este error se puede devolver cuando no se encuentra el grupo en el buzón de correo cuando se usa la [operación RemoveImGroup](https://msdn.microsoft.com/library/5e788016-68e0-4a3f-9243-03f6b6c6b389%28Office.15%29.aspx). Este error se aplica a los clientes destinados a Exchange Online y versiones de Exchange a partir de Exchange 2013.  <br/> |El valor de la propiedad **GROUPID** que se especificó en la solicitud podría ser válido en estructura, pero ningún grupo del buzón coincidió con esta estructura. Es posible que el grupo ya se haya quitado.  <br/> |
|ErrorInvalidReferenceItem  <br/> |El identificador de elemento al que se hace referencia no es un **MessageType** ni **ExchangeWebServices. CalendarItemTypeType**, o uno de sus descendientes. El identificador de elemento de referencia es para un objeto **CalendarItemType** y el organizador está intentando responder o ReplyAll.  <br/> |El identificador puede tener un formato válido, pero no el servidor que esperaba para la operación. Compruebe que hace referencia al identificador correcto para la operación.  <br/> |
|ErrorMissingManagedFolderId  <br/> |Falta la propiedad IDs de Directiva, etiqueta de propiedad 0x6732, de la carpeta.  <br/> |La carpeta está dañada. Considere la posibilidad de volver a crearlo.  <br/> |
   
## <a name="converting-identifiers"></a>Convertir identificadores
<a name="bk_ConvertingIdentifiers"> </a>

Es posible que deba convertir un identificador de un formato a otro. Por ejemplo, es posible que necesite convertir un identificador de un EWS externo, como un identificador procedente de una conexión MAPI, con un formato que la aplicación puede usar. Para ello, puede usar la operación de EWS de [ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx) o el método de API administrada de EWS de [ConvertId](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.convertid%28v=exchg.80%29.aspx) . 
  
Por ejemplo, EntryID es un identificador único generado por el almacén de mensajes MAPI que asigna el almacén cuando se guarda el elemento. Para usar EntryID en la aplicación, primero debe convertirlo en un EwsId. 
  
Outlook Web App usa su propia versión de los identificadores, denominada OwaId, en direcciones URL para obtener acceso a carpetas y elementos. Si la aplicación necesita obtener acceso a elementos de Outlook Web App, debe convertir OwaId en un EwsId.
  
Puede usar la operación **ConvertId** o el método para convertir varios formatos de identificador diferentes. 
  
**Tabla 3. Formatos de identificadores convertibles en Exchange**

|**Formato**|**Descripción**|
|:-----|:-----|
|EwsLegacyId  <br/> |EwsId que se aplica a Exchange 2007.  <br/> |
|EwsId  <br/> |EwsId que se aplica a Exchange Online y versiones de Exchange a partir de Exchange 2007 SP1.  <br/> |
|StoreId  <br/> |El identificador del almacén de Exchange donde se almacenan las carpetas y los elementos.  <br/> |
|OwaId  <br/> |El identificador de Outlook Web App que se usa con Outlook Web App en Exchange 2007 y Exchange 2010. <br/><br/>**Nota**: Exchange Online y las versiones de Exchange que comienzan con Exchange 2013 usan EwsId para Outlook Web App.           |
|EntryId  <br/> |Identificador de MAPI conocido comúnmente como la propiedad **PR_ENTRYID** de un mensaje MAPI.  <br/> |
|HexEntryId  <br/> |Representación codificada en hexadecimal de la propiedad **PR_ENTRYID** que se usa para el identificador de evento del calendario de disponibilidad. También es el formato de identificador que usa Outlook.  <br/> |
   
## <a name="see-also"></a>Vea también

- [Desarrollar clientes de servicios web de Exchange](develop-web-service-clients-for-exchange.md)  
- [Operación ConvertId](https://msdn.microsoft.com/library/47d96cf6-9e2f-4fc0-9682-7258d3fbf918%28Office.15%29.aspx)  
- [Enumeración ServiceError](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceerror%28v=exchg.80%29.aspx) 
- [Eliminación de elementos mediante EWS en Exchange](deleting-items-by-using-ews-in-exchange.md)
    

