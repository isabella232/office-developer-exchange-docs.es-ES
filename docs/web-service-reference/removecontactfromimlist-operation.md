---
title: Operación RemoveContactFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Buscar información sobre la operación de EWS de RemoveContactFromImList.
ms.openlocfilehash: 8b3d83a0b53bad169d9f3478540e5087901f3a12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458470"
---
# <a name="removecontactfromimlist-operation"></a>Operación RemoveContactFromImList

Buscar información sobre la operación de EWS de **RemoveContactFromImList** . 
  
La operación **RemoveContactFromImList** elimina contactos de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Uso de la operación RemoveContactFromImList

La operación **RemoveContactFromImList** acepta un único argumento que identifica un contacto para quitarlo de la lista de contactos de Lync almacenada en un servidor de Exchange. La lista de contactos a los que se dirige esta operación se denomina **contactos de Lync** en Outlook 2013. 
  
> [!CAUTION]
> No use la [operación DeleteItem](deleteitem-operation.md) para quitar contactos de una lista de contactos. Puede que sea necesario realizar un procesamiento adicional del servidor para admitir la eliminación de un contacto de la lista de **contactos de Lync** . Tenga en cuenta que la lista de **contactos de Lync** es el equivalente conceptual de la carpeta de buzones de contactos predeterminada de **Lync** . 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>Encabezados SOAP de operación RemoveContactFromImList

La operación **RemoveContactFromImList** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Este encabezado se aplica a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>Ejemplo de solicitud de operación RemoveContactFromImList: quitar un contacto de la lista de contactos de Lync

El siguiente ejemplo de una solicitud de operación de **RemoveContactFromImList** muestra cómo quitar un contacto de la lista de **contactos de Lync** . La operación **RemoveContactFromImList** acepta un único identificador de contacto único para identificar el contacto que se ha quitado de la lista de **contactos de Lync** . 
  
> [!NOTE]
> Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad. 
  
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
    
- [Contacto](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Respuesta de operación RemoveContactFromImList correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveContactFromImList** para quitar un contacto de la lista de **contactos de Lync** . 
  
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
    
## <a name="removecontactfromimlist-operation-error-response"></a>Respuesta de error de operación de RemoveContactFromImList

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveContactFromImList** . Se trata de una respuesta a una solicitud para quitar un contacto de la lista de **contactos de Lync** cuando el contacto ya no existe en la lista. 
  
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

Los siguientes elementos se usan en el cuerpo SOAP de respuesta de error:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    

