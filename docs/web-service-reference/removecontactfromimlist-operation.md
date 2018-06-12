---
title: Operación RemoveContactFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 28ec96c3-45af-48ff-9f17-718a527dc0ad
description: Busque información sobre la EWS RemoveContactFromImList operación.
ms.openlocfilehash: 036b295a84e86ad74c467572cc52fdf6bbae5191
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837080"
---
# <a name="removecontactfromimlist-operation"></a>Operación RemoveContactFromImList

Obtenga información acerca de la operación de EWS **RemoveContactFromImList** . 
  
La operación **RemoveContactFromImList** quita los contactos de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removecontactfromimlist-operation"></a>Mediante la operación RemoveContactFromImList

La operación de **RemoveContactFromImList** acepta un argumento único que identifica un contacto para quitar de la lista de contactos de Lync almacenada en un servidor de Exchange. La lista de contactos que los objetivos de esta operación se denomina **Contactos de Lync** en Outlook 2013. 
  
> [!CAUTION]
> No use la [operación DeleteItem](deleteitem-operation.md) para quitar los contactos de una lista de contactos. Procesamiento de servidor adicional que tenga que se producen para admitir la eliminación de un contacto de la lista de **Contactos de Lync** . Tenga en cuenta que la lista de **Contactos de Lync** es el equivalente conceptual de la carpeta de buzón de correo de **Los contactos de Lync** predeterminada. 
  
### <a name="removecontactfromimlist-operation-soap-headers"></a>Encabezados SOAP de operación de RemoveContactFromImList

La operación de **RemoveContactFromImList** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="removecontactfromimlist-operation-request-example-remove-a-contact-from-the-lync-contacts-list"></a>Ejemplo de solicitud de operación de RemoveContactFromImList: quitar un contacto de la lista de contactos de Lync

El siguiente ejemplo de una solicitud de operación **RemoveContactFromImList** muestra cómo quitar un contacto de la lista de **Contactos de Lync** . La operación de **RemoveContactFromImList** acepta un único identificador de contacto único para identificar el contacto al que se ha quitado de la lista de **Contactos de Lync** . 
  
> [!NOTE]
> Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
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

En la solicitud SOAP body, se usan los siguientes elementos:
  
- [RemoveContactFromImList](removecontactfromimlist.md)
    
- [ID de contacto](contactid.md)
    
## <a name="successful-removecontactfromimlist-operation-response"></a>Respuesta es correcta de operación RemoveContactFromImList

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveContactFromImList** para quitar un contacto de la lista de **Contactos de Lync** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Success" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>
```

En la respuesta SOAP body, se usan los siguientes elementos:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removecontactfromimlist-operation-error-response"></a>Respuesta de error de la operación de RemoveContactFromImList

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveContactFromImList** . Esta es una respuesta a una solicitud para quitar un contacto de la lista de **Contactos de Lync** cuando el contacto ya no existe en la lista. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="8" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveContactFromImListResponse ResponseClass="Error" 
                                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveContactFromImListResponse>
   </s:Body>
</s:Envelope>

```

En el cuerpo del mensaje SOAP de respuesta de error se usan los siguientes elementos:
  
- [RemoveContactFromImListResponse](removecontactfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Ver también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    

