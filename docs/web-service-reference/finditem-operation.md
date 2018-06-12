---
title: FindItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindItem
api_type:
- schema
ms.assetid: ebad6aae-16e7-44de-ae63-a95b24539729
description: Busque información sobre la EWS FindItem operación.
ms.openlocfilehash: b033ac2930981819a20f1336d40058a5f7c03b89
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764637"
---
# <a name="finditem-operation"></a>FindItem Operation

Obtenga información acerca de la operación de EWS **FindItem** . 
  
La operación **FindItem** busca los elementos que se encuentran en el buzón del usuario. Esta operación proporciona muchas maneras para filtrar y formato de cómo se devuelven los resultados de búsqueda para el autor de la llamada. 
  
## <a name="using-the-finditem-operation"></a>Mediante la operación FindItem

La solicitud de operación **FindItem** proporciona muchas formas de un buzón de correo y el formato de cómo se devuelven los datos en una respuesta de búsqueda. Puede especificar lo siguiente en una solicitud **FindItem** : 
  
- Si la búsqueda es un recorrido superficial o eliminado temporalmente. Es necesario especificar esto. Tenga en cuenta que un recorrido eliminado temporalmente combinado con una restricción de la búsqueda, se producirá en cero los elementos devueltos, incluso si hay elementos que coincidan con los criterios de búsqueda.
    
- La forma de respuesta de los elementos. Esto identifica las propiedades que se devuelven en la respuesta. Es necesario especificar esto.
    
- Las carpetas desde la que se va a realizar la búsqueda. Es necesario especificar esto.
    
- Los tipos de mecanismo y vista de paginación para devolver ver los datos en las páginas. Especificar esto es opcional.
    
- Opciones de agrupación y ordenación de los elementos que se devuelven. Especificar esto es opcional.
    
- Las restricciones de búsqueda o cadenas de sintaxis de consulta avanzada (AQS) para filtrar los elementos que se devuelven. Para obtener más información acerca del uso de AQS para las búsquedas de índice de contenido, vea [QueryString (String)](querystring-string.md). Especificar esto es opcional.
    
- El criterio de ordenación para los elementos devueltos en la respuesta. Especificar esto es opcional.
    
La operación **FindItem** devuelve sólo el primer 512 bytes de cualquier propiedad que se pueden transmitir. Para Unicode, devuelve los primeros 255 caracteres mediante el uso de una cadena Unicode terminada en null. No devolver cualquiera de los formatos de cuerpo de mensaje o las listas de destinatarios. **FindItem** devolverá a un destinatario resumen. Puede usar la [operación GetItem](getitem-operation.md) para obtener los detalles de un elemento. 
  
 **FindItem** devuelve sólo el elemento [nombre (EmailAddressType)](name-emailaddresstype.md) y no devuelve el elemento [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) en el elemento de [buzón de correo](mailbox.md) para los siguientes campos: 
  
- El campo [de](from.md) los mensajes 
    
- El campo de [remitente](sender.md) de mensajes 
    
- El campo [Organizador](organizer.md) para elementos de calendario 
    
> [!NOTE]
> La operación **FindItem** puede devolver los resultados en un elemento [CalendarView](calendarview.md) . El elemento **CalendarView** devuelve los elementos de calendario único y todas las apariciones de las reuniones periódicas. Si no se usa un elemento **CalendarView** , se devuelven los elementos de calendario único y elementos periódicos del calendario principal. Si no se usa un elemento **CalendarView** , las apariciones se deben expandir desde el maestro periódico. 
  
La operación **FindItem** puede usar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
**La tabla 1. Encabezados SOAP de FindItem operación**

|**Header**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**DateTimePrecision** <br/> |[DateTimePrecision](datetimeprecision.md) <br/> |Especifica la resolución de los valores de fecha y hora en las respuestas desde el servidor, en segundos o en milisegundos. Esto es aplicable a una solicitud.  <br/> |
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Esto es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural de RFC3066 va a usar para tener acceso al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Esto es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Esto es aplicable a una respuesta.  <br/> |
|**TimeZoneContext** <br/> |[TimeZoneContext](timezonecontext.md) <br/> |Identifica la zona horaria que se usará para todas las respuestas desde el servidor. Esto es aplicable a una solicitud.  <br/> |
   
## <a name="finditem-operation-request-example"></a>Ejemplo de solicitud de operación FindItem

El siguiente ejemplo de una solicitud de **FindItem** muestra cómo obtener el identificador del elemento que se define en la enumeración **IdOnly** del elemento [BaseShape](baseshape.md) para los elementos que se encuentran en la carpeta Elementos eliminados. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <FindItem xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

En la solicitud se usan los siguientes elementos: 
  
- [FindItem](finditem.md)
    
- [ItemShape](itemshape.md)
    
- [BaseShape](baseshape.md)
    
- [ParentFolderIds](parentfolderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
Para ver más opciones para un mensaje de solicitud **FindItem** , explore la jerarquía de esquema. Comenzar en el elemento de [FindItem](finditem.md) . 
  
## <a name="successful-finditem-operation-response"></a>Respuesta es correcta de operación FindItem

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud de **FindItem** . 
  
Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de EWS. Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) . Exchange no devuelve [el elemento de base](item.md) de las respuestas. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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
    
Para ver más opciones para un mensaje de respuesta **FindItem** , explore la jerarquía de esquema. Comenzar en el elemento de [FindItemResponse](finditemresponse.md) . 
  
## <a name="finditem-operation-error-response"></a>Respuesta de error de la operación FindItem

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de **FindItem** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="595" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                      xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

En la respuesta de error, se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [FindItemResponse](finditemresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [FindItemResponseMessage](finditemresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
Para ver más opciones para un mensaje de respuesta de error **FindItem** , explore la jerarquía de esquema. Comenzar en el elemento de [FindItemResponse](finditemresponse.md) . 
  
## <a name="version-differences"></a>Diferencias de versión

Las versiones de Exchange con la versión principal 15 iniciales y finales con generación 15.0.898.11 devuelto un valor de ErrorInvalidOperation en el elemento [ResponseCode](responsecode.md) cuando la operación **FindItem** se usa para buscar en varias carpetas de un buzón de archivo. 
  
## <a name="see-also"></a>Ver también

- [Buscar elementos](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)
    
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)
    
- **FindItemType**
    

