---
title: Operación AddDistributionGroupToImList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5aa9bec8-71cf-4a6e-8ec8-b4965b40fd4a
description: Busque información sobre la EWS AddDistributionGroupToImList operación.
ms.openlocfilehash: 7c562c317890a4cffb9e5844ea41c1096a8595b4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763393"
---
# <a name="adddistributiongrouptoimlist-operation"></a>Operación AddDistributionGroupToImList

Obtenga información acerca de la operación de EWS **AddDistributionGroupToImList** . 
  
La operación de Exchange Web Services (EWS) **AddDistributionGroupToImList** agrega un grupo de distribución a la lista (IM) en el almacén de contactos unificados de mensajería instantánea. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-adddistributiongrouptoimlist-operation"></a>Mediante la operación AddDistributionGroupToImList

La operación de **AddDistributionGroupToImList** toma un argumento único que identifica un grupo de distribución para agregar a la lista de mensajería instantánea. Esta operación no crea un grupo de distribución; el grupo de distribución debe estar ya creado. 
  
Esta operación puede usar los encabezados SOAP que se enumeran en la siguiente tabla.
  
**La tabla 1. Encabezados SOAP de operación de AddDistributionGroupToImList**

|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Esto es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Esto es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Esto es aplicable a una respuesta.  <br/> |
   
## <a name="adddistributiongrouptoimlist-operation-request-example"></a>Ejemplo de solicitud de operación de AddDistributionGroupToImList

El siguiente ejemplo de una solicitud de operación **AddDistributionGroupToImList** muestra cómo agregar un grupo de distribución a la lista de mensajería instantánea. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
   </soap:Header>
   <soap:Body >
      <m:AddDistributionGroupToImList>
         <m:SmtpAddress>distributionlist1@example.com</m:SmtpAddress>
      </m:AddDistributionGroupToImList>
   </soap:Body>
</soap:Envelope>
```

La solicitud SOAP body contiene los siguientes elementos:
  
- [AddDistributionGroupToImList](adddistributiongrouptoimlist.md)   
- [SmtpAddress](smtpaddress.md)
    
## <a name="successful-adddistributiongrouptoimlist-operation-response"></a>Respuesta es correcta de operación AddDistributionGroupToImList

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **AddDistributionGroupToImList** . 
  
La respuesta correcta contiene el nombre para mostrar de grupo de distribución, la clase de almacén de Exchange para el grupo de distribución y el identificador de EWS del nuevo grupo de distribución.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/"
            xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
            xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <s:Header>
      <t:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013"/>
   </s:Header>
   <s:Body>
      <m:AddDistributionGroupToImListResponse ResponseClass="Success">
         <m:ResponseCode>NoError</m:ResponseCode>
         <m:ImGroup>
            <t:DisplayName>distributionlist1@example.com</t:DisplayName>
            <t:GroupType>IPM.DistList.MOC.DG</t:GroupType>
            <t:ExchangeStoreId Id="AAMkAGQ1MjJjAA=" 
                             ChangeKey="EgAAAA=="/>
      </m:ImGroup>
      </m:AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [ImGroup](imgroup.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [GroupType](grouptype.md)
    
- [ExchangeStoreId](exchangestoreid.md)
    
## <a name="adddistributiongrouptoimlist-operation-errorinvalidimdistributiongroupsmtpaddress-error-response"></a>Operación AddDistributionGroupToImList respuesta de error de ErrorInvalidImDistributionGroupSmtpAddress

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **AddDistributionGroupToImList** . La siguiente respuesta de error se produce cuando se realiza un intento para agregar un grupo de distribución que no existe en el almacén de Exchange. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <AddDistributionGroupToImListResponse ResponseClass="Error" 
                                            xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified IM distribution group SMTP address is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImDistributionGroupSmtpAddress</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </AddDistributionGroupToImListResponse>
   </s:Body>
</s:Envelope>
```

La respuesta de error SOAP body contiene los siguientes elementos:
  
- [AddDistributionGroupToImListResponse](adddistributiongrouptoimlistresponse.md)
    
- [MessageText](messagetext.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Las personas y los contactos de EWS en Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)   
- [AddImGroup](addimgroup-operation.md)   
- [RemoveImGroup](removeimgroup-operation.md)
    

