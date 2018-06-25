---
title: Operación RemoveDistributionGroupFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Busque información sobre la EWS RemoveDistributionGroupFromImList operación.
ms.openlocfilehash: 9999f98a5698dd33c22e22fdf86bd00a2d053b52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837096"
---
# <a name="removedistributiongroupfromimlist-operation"></a>Operación RemoveDistributionGroupFromImList

Obtenga información acerca de la operación de EWS **RemoveDistributionGroupFromImList** . 
  
La operación **RemoveDistributionGroupFromImList** quita un grupo de distribución de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a>Mediante la operación RemoveDistributionGroupFromImList

La operación de **RemoveDistributionGroupFromImList** acepta un argumento único que identifica un grupo de distribución para quitar de la lista de Lync IM almacenada en un servidor de Exchange. 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a>Encabezados SOAP de operación de RemoveDistributionGroupFromImList

La operación de **RemoveDistributionGroupFromImList** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a>Ejemplo de solicitud de operación de RemoveDistributionGroupFromImList: quitar un grupo de distribución de una lista de mensajería instantánea

El siguiente ejemplo de una solicitud de operación **RemoveDistributionGroupFromImList** muestra cómo quitar un grupo de distribución de un grupo de mensajería instantánea. La operación **RemoveDistributionGroupFromImList** acepta el identificador del grupo único para identificar el grupo de distribución para quitar de la lista de mensajería instantánea. El elemento [ExchangeStoreId](exchangestoreid.md) que se devuelve en la respuesta de la [operación de GetImItemList](getimitemlist-operation.md) y la [operación de AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md) identifica los grupos de distribución que se pueden quitar de la lista de mensajería instantánea. 
  
> [!NOTE]
> Todos los identificadores de artículo y cambiar claves en este artículo se han abreviado para conservar la legibilidad. 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:RemoveDistributionGroupFromImList>
         <m:GroupId Id="AAMkADEzO4QrAABmEh5oAAA="/>
      </m:RemoveDistributionGroupFromImList>
   </soap:Body>
</soap:Envelope>
```

En la solicitud SOAP body, se usan los siguientes elementos:
  
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a>Respuesta es correcta de operación RemoveDistributionGroupFromImList

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **RemoveDistributionGroupFromImList** a una quitar un grupo de distribución desde un grupo de mensajería instantánea. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

En la respuesta SOAP body, se usan los siguientes elementos:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a>Ejemplo de respuesta de error de operación de RemoveDistributionGroupFromImList

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveDistributionGroupFromImList** . Esta es una respuesta a una solicitud para quitar un grupo de distribución que ya se ha quitado el buzón de correo. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

En el cuerpo del mensaje SOAP de respuesta de error se usan los siguientes elementos:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    
- [Operación AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md)
    
- [Las personas y los contactos de EWS en Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

