---
title: Operación RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Busque información sobre la EWS RemoveImContactFromGroup operación.
ms.openlocfilehash: 8c9af251014dbddabb439ed5bf5dc35580da6a90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837099"
---
# <a name="removeimcontactfromgroup-operation"></a>Operación RemoveImContactFromGroup

Obtenga información acerca de la operación de EWS **RemoveImContactFromGroup** . 
  
La operación **RemoveImContactFromGroup** quita un único contacto de mensajería instantánea de un grupo de mensajería instantánea. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removeimcontactfromgroup-operation"></a>Mediante la operación RemoveImContactFromGroup

La operación **RemoveImContactFromGroup** toma dos argumentos: un identificador de elemento de contacto y el grupo (IM) desde la que se quita el contacto de mensajería de instantánea correspondiente. 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a>Encabezados SOAP de operación de RemoveImContactFromGroup

La operación de **RemoveImContactFromGroup** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario que está realizando la suplantación de la aplicación cliente. Este encabezado es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón. Este encabezado es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a>Ejemplo de solicitud de operación de RemoveImContactFromGroup

El siguiente ejemplo de una solicitud de operación **RemoveImContactFromGroup** muestra cómo quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea. 
  
> [!NOTE]
> Los identificadores de grupo y contactos se han abreviado para conservar la legibilidad. 
  
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
      <m:RemoveImContactFromGroup>
         <m:ContactId Id="AAMkAGQ1MjJjMTBkLTcAAAAvcAAA="
                      ChangeKey="EQAAABYAAABtF8oI7iVOQ"/>
         <m:GroupId Id="AAMkAGQ1MjJjMTBkbWAAAAAAQKAAA="
                    ChangeKey="EgAAAA=="/>
      </m:RemoveImContactFromGroup>
   </soap:Body>
</soap:Envelope>
```

La solicitud SOAP body contiene los siguientes elementos:
  
- [RemoveImContactFromGroup](removeimcontactfromgroup.md)
    
- [ID de contacto](contactid.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a>Respuesta es correcta de operación RemoveImContactFromGroup

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **RemoveImContactFromGroup** . 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a>Operación RemoveImContactFromGroup respuesta de error de ErrorInvalidImContactId

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImContactFromGroup** . La siguiente respuesta de error se produce cuando se realiza un intento para quitar un elemento de contacto que no existe en el grupo de mensajería instantánea. 
  
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
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Ver también

- [Las personas y los contactos de EWS en Exchange](http://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [AddDistributionGroupToImList](adddistributiongrouptoimlist-operation.md)
    
- [AddImContactToGroup](addimcontacttogroup-operation.md)
    
- [Operación AddImGroup](addimgroup-operation.md)
    
- [Operación AddNewImContactToGroup](addnewimcontacttogroup-operation.md)
    
- [Operación GetImItemList](getimitemlist-operation.md)
    
- [GetImItems](getimitems-operation.md)
    
- [RemoveContactFromImList](removecontactfromimlist-operation.md)
    
- [RemoveDistributionGroupFromImList](removedistributiongroupfromimlist-operation.md)
    
- [Operación RemoveImGroup](removeimgroup-operation.md)
    
- [Operación SetImGroup](setimgroup-operation.md)
    
- [SetImListMigrationCompleted](setimlistmigrationcompleted-operation.md)
    

