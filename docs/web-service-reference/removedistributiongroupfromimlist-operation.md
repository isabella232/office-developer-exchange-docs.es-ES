---
title: Operación RemoveDistributionGroupFromImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 252bddf2-98b6-4824-b548-2fba2bda5384
description: Buscar información sobre la operación de EWS de RemoveDistributionGroupFromImList.
ms.openlocfilehash: 66220f0cab99f404e17136bbb7836ca13d569b53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459605"
---
# <a name="removedistributiongroupfromimlist-operation"></a>Operación RemoveDistributionGroupFromImList

Buscar información sobre la operación de EWS de **RemoveDistributionGroupFromImList** . 
  
La operación **RemoveDistributionGroupFromImList** quita un grupo de distribución de la lista de mensajería instantánea (mi) de Lync cuando Lync usa Exchange para el almacén de contactos. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removedistributiongroupfromimlist-operation"></a>Uso de la operación RemoveDistributionGroupFromImList

La operación **RemoveDistributionGroupFromImList** acepta un único argumento que identifica un grupo de distribución que se quitará de la lista de mensajería instantánea de Lync almacenada en un servidor de Exchange. 
  
### <a name="removedistributiongroupfromimlist-operation-soap-headers"></a>Encabezados SOAP de operación RemoveDistributionGroupFromImList

La operación **RemoveDistributionGroupFromImList** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Este encabezado se aplica a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="removedistributiongroupfromimlist-operation-request-example-remove-a-distribution-group-from-an-im-list"></a>Ejemplo de solicitud de operación RemoveDistributionGroupFromImList: quitar un grupo de distribución de una lista de mensajes instantáneos

El siguiente ejemplo de una solicitud de operación de **RemoveDistributionGroupFromImList** muestra cómo quitar un grupo de distribución de un grupo de mensajería instantánea. La operación **RemoveDistributionGroupFromImList** acepta el identificador de grupo único para identificar el grupo de distribución que se va a quitar de la lista de mensajería instantánea. El elemento [ExchangeStoreId](exchangestoreid.md) que se devuelve en la respuesta de la [operación GetImItemList](getimitemlist-operation.md) y la [operación AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md) identifica los grupos de distribución que pueden quitarse de la lista de mi. 
  
> [!NOTE]
> Todos los identificadores de elemento y las claves de cambio de este artículo se han reducido para preservar la legibilidad. 
  
```XML
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Los siguientes elementos se usan en el cuerpo SOAP de la solicitud:
  
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removedistributiongroupfromimlist-operation-response"></a>Respuesta de operación RemoveDistributionGroupFromImList correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **RemoveDistributionGroupFromImList** en un grupo de distribución de mensajería instantánea. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Success" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Los siguientes elementos se usan en el cuerpo SOAP de la respuesta:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removedistributiongroupfromimlist-operation-error-response-example"></a>Ejemplo de respuesta de error de operación RemoveDistributionGroupFromImList

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveDistributionGroupFromImList** . Se trata de una respuesta a una solicitud para quitar un grupo de distribución que ya se ha quitado del buzón. 
  
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
      <RemoveDistributionGroupFromImListResponse ResponseClass="Error" 
                                                 xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified object was not found in the store.</MessageText>
         <ResponseCode>ErrorItemNotFound</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveDistributionGroupFromImListResponse>
   </s:Body>
</s:Envelope>
```

Los siguientes elementos se usan en el cuerpo SOAP de respuesta de error:
  
- [RemoveDistributionGroupFromImListResponse](removedistributiongroupfromimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    
- [Operación AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md)
    
- [Personas y contactos de EWS en Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx#What)
    

