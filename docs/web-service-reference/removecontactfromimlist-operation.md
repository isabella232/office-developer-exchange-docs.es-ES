---
title: Operación RemoveContactFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Busque información sobre la operación EWS RemoveContactFromImList.
ms.openlocfilehash: cc72dc1b0abf9032fabafbaac53d29f41968dafb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523591"
---
# <a name="removecontactfromimlist-operation"></a>Operación RemoveContactFromImList

Busque información sobre la **operación EWS RemoveContactFromImList.** 
  
La **operación RemoveContactFromImList** quita los contactos de la lista de mensajería instantánea (MI) de Lync cuando Lync usa Exchange para el almacén de contactos. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Uso de la operación RemoveContactFromImList

La **operación RemoveContactFromImList** acepta un único argumento que identifica un contacto para quitar de la lista de contactos de Lync almacenada en un Exchange servidor. La lista de contactos a los que se dirige esta operación se denomina Contactos de **Lync** en Outlook 2013. 
  
> [!CAUTION]
> No use la operación [DeleteItem para](deleteitem-operation.md) quitar contactos de una lista de contactos. Es posible que deba producirse un procesamiento adicional del lado servidor para admitir la eliminación de un contacto de la **lista de contactos de Lync.** Tenga en cuenta que **la lista de contactos** de Lync es el equivalente conceptual de la carpeta predeterminada del buzón contactos de **Lync.** 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>Encabezados SOAP de operación RemoveContactFromImList

La **operación RemoveContactFromImList** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>Ejemplo de solicitud de operación RemoveContactFromImList: Quitar un contacto de la lista de contactos de Lync

En el siguiente ejemplo de una **solicitud de operación RemoveContactFromImList** se muestra cómo quitar un contacto de la **lista de contactos de Lync.** La **operación RemoveContactFromImList** acepta un único identificador de contacto único para identificar el contacto que se quita de la lista **de contactos de Lync.** 
  
> [!NOTE]
> Todos los identificadores de elementos y las claves de cambio de este artículo se han acortado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:RemoveContactFromImList>
         <m:ContactId Id=""/>
      </m:RemoveContactFromImList>
   </soap:Body>
</soap:Envelope>

```

Los siguientes elementos se usan en el cuerpo SOAP de la solicitud:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ContactId](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Respuesta correcta de operación RemoveContactFromImList

En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación **RemoveContactFromImList** para quitar un contacto de la **lista de contactos de Lync.** 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

Los siguientes elementos se usan en el cuerpo SOAP de la respuesta:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a>Respuesta de error de operación RemoveContactFromImList

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveContactFromImList.** Esta es una respuesta a una solicitud para quitar un contacto de la lista de contactos de **Lync** cuando el contacto ya no existe en la lista. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

Los siguientes elementos se usan en el cuerpo SOAP de la respuesta de error:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Ver también

- [Operaciones ews en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    

