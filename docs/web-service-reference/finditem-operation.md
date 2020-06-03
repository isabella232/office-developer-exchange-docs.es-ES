---
title: Operación FindItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Busca información sobre la operación de EWS de FindItem.
localization_priority: Priority
ms.openlocfilehash: 499d1ee80ef323c883fa86eb125d8c037fb37d4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462559"
---
# <a name="finditem-operation"></a>Operación FindItem

Busca información sobre la operación de EWS de **FindItem** . 
  
La operación **FindItem** busca elementos que se encuentran en el buzón de un usuario. Esta operación proporciona muchas maneras de filtrar y dar formato a cómo se devuelven los resultados de la búsqueda al autor de la llamada. 
  
## <a name="using-the-finditem-operation"></a>Uso de la operación FindItem

La solicitud de operación **FindItem** proporciona muchas formas de buscar en un buzón de correo y dar formato a cómo se devuelven los datos en una respuesta. Puede especificar lo siguiente en una solicitud **FindItem** : 
  
- Si la búsqueda es un recorrido superficial o eliminado temporalmente. Es necesario especificar esto. Tenga en cuenta que un recorrido de eliminación temporal combinado con una restricción de búsqueda dará como resultado la devolución de elementos cero, incluso si hay elementos que coinciden con los criterios de búsqueda.
    
- Forma de respuesta de los elementos. Identifica las propiedades que se devuelven en la respuesta. Es necesario especificar esto.
    
- Las carpetas desde las que se va a realizar la búsqueda. Es necesario especificar esto.
    
- El mecanismo de paginación y los tipos de vista para devolver los datos de la vista en las páginas. Especificar esto es opcional.
    
- Opciones para agrupar y ordenar los elementos que se devuelven. Especificar esto es opcional.
    
- Restricciones de búsqueda o cadenas de sintaxis de consulta avanzada (AQS) para filtrar los elementos que se devuelven. Para obtener más información sobre el uso de AQS para búsquedas de índice de contenido, consulte [QueryString (cadena)](querystring-string.md). Especificar esto es opcional.
    
- Criterio de ordenación de los elementos devueltos en la respuesta. Especificar esto es opcional.
    
La operación **FindItem** devuelve sólo los primeros 512 bytes de cualquier propiedad streamable. Para Unicode, devuelve los primeros 255 caracteres mediante una cadena Unicode terminada en NULL. No devuelve ninguno de los formatos del cuerpo del mensaje o las listas de destinatarios. **FindItem** devolverá un resumen de destinatarios. Puede usar la [operación GetItem](getitem-operation.md) para obtener los detalles de un elemento. 
  
 **FindItem** solo devuelve el elemento [Name (EmailAddressType)](name-emailaddresstype.md) y no devuelve el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en el elemento [Mailbox](mailbox.md) para los siguientes campos: 
  
- El campo [de](from.md) para los mensajes 
    
- El campo [Sender](sender.md) para los mensajes 
    
- El campo [Organizer](organizer.md) para los elementos de calendario 
    
> [!NOTE]
> La operación **FindItem** puede devolver resultados en un elemento [CalendarView](calendarview.md) . El elemento **CalendarView** devuelve elementos de calendario únicos y todas las repeticiones de reuniones periódicas. Si no se usa un elemento **CalendarView** , se devuelven los elementos de calendario únicos y los elementos de calendario principal periódicos. Las repeticiones deben expandirse desde el maestro periódico si no se usa un elemento **CalendarView** . 
  
La operación **FindItem** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
**Tabla 1. Encabezados SOAP de la operación FindItem**

|**Header**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Especifica la resolución de los valores de datos/tiempo en respuestas del servidor, en segundos o en milisegundos. Esto es aplicable a una solicitud.  <br/> |
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Esto es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural RFC3066 que se va a usar para obtener acceso al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Esto es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Esto es aplicable a una respuesta.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se va a usar para todas las respuestas del servidor. Esto es aplicable a una solicitud.  <br/> |
   
## <a name="finditem-operation-request-example"></a>Ejemplo de solicitud de operación de FindItem

El siguiente ejemplo de una solicitud **FindItem** muestra cómo obtener el identificador de elemento definido por la enumeración **IdOnly** del elemento [BaseShape](baseshape.md) para los elementos que se encuentran en la carpeta elementos eliminados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
              Traversal="Shallow">
      <ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
      </ItemShape>
      <ParentFolderIds>
        <t:DistinguishedFolderId Id="deleteditems"/>
      </ParentFolderIds>
    </FindItem>
  </soap:Body>
</soap:Envelope>
```

Los siguientes elementos se usan en la solicitud: 
  
- [FindItem](finditem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
Para obtener más opciones para un mensaje de solicitud **FindItem** , explore la jerarquía del esquema. Comienza en el elemento [FindItem](finditem.md) . 
  
## <a name="successful-finditem-operation-response"></a>Respuesta correcta a la operación FindItem

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **FindItem** . 
  
Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no tienen establecimiento inflexible de tipos en el esquema EWS. Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) . Exchange no devuelve el elemento de [elemento](item.md) base en las respuestas. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder TotalItemsInView="10" IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="AS4AUn=" ChangeKey="fsVU4==" />
              </t:Message>
              <t:Message>
                <t:ItemId Id="AS4AUM=" ChangeKey="fsVUA==" />
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootFolder (FindItemResponseMessage)](rootfolder-finditemresponsemessage.md)
    
- [Items](items.md)
    
- [Message](message-ex15websvcsotherref.md)
    
- [ItemId](itemid.md)
    
Para obtener más opciones para un mensaje de respuesta **FindItem** , explore la jerarquía del esquema. Empiece en el elemento [FindItemResponse](finditemresponse.md) . 
  
## <a name="finditem-operation-error-response"></a>Respuesta de error de la operación FindItem

En el ejemplo siguiente se muestra una respuesta de error a una solicitud **FindItem** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Error">
          <m:MessageText>Id is malformed.</m:MessageText>
          <m:ResponseCode>ErrorInvalidIdMalformed</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </FindItemResponse>
  </soap:Body>
</soap:Envelope>
```

Los siguientes elementos se usan en la respuesta de error:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para obtener más opciones para un mensaje de respuesta de error de **FindItem** , explore la jerarquía del esquema. Empiece en el elemento [FindItemResponse](finditemresponse.md) . 
  
## <a name="version-differences"></a>Diferencias de versión

Las versiones de Exchange que comienzan con la versión principal 15 y terminan con la compilación 15.0.898.11 devuelven un valor de ErrorInvalidOperation en el elemento [ResponseCode](responsecode.md) cuando se usa la operación **FindItem** para buscar en varias carpetas de un buzón de archivo. 
  
## <a name="see-also"></a>Vea también

- [Buscar elementos](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

