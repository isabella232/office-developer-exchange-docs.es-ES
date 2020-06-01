---
title: Operación RemoveImContactFromGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a190bbec-c71b-4e6a-880b-55854c724d8c
description: Buscar información sobre la operación de EWS de RemoveImContactFromGroup.
ms.openlocfilehash: 4750ef57794c3da540ac36baa8ef6ef093939ea1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466972"
---
# <a name="removeimcontactfromgroup-operation"></a>Operación RemoveImContactFromGroup

Buscar información sobre la operación de EWS de **RemoveImContactFromGroup** . 
  
La operación **RemoveImContactFromGroup** quita un solo contacto de mensajería instantánea de un grupo de mensajería instantánea. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-removeimcontactfromgroup-operation"></a>Uso de la operación RemoveImContactFromGroup

La operación **RemoveImContactFromGroup** toma dos argumentos: un identificador de elemento de contacto y el grupo de mensajería instantánea (mi) correspondiente del que se quita el contacto. 
  
### <a name="removeimcontactfromgroup-operation-soap-headers"></a>Encabezados SOAP de operación RemoveImContactFromGroup

La operación **RemoveImContactFromGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica al usuario que está suplantando la aplicación cliente. Este encabezado se aplica a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón. Este encabezado se aplica a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="removeimcontactfromgroup-operation-request-example"></a>Ejemplo de solicitud de operación RemoveImContactFromGroup

El siguiente ejemplo de una solicitud de operación de **RemoveImContactFromGroup** muestra cómo quitar un contacto de mensajería instantánea de un grupo de mensajería instantánea. 
  
> [!NOTE]
> Los identificadores de grupo y contacto se han abreviado para preservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [RemoveImContactFromGroup](removeimcontactfromgroup.md)
    
- [Contacto](contactid.md)
    
- [GroupId](groupid.md)
    
## <a name="successful-removeimcontactfromgroup-operation-response"></a>Respuesta de operación RemoveImContactFromGroup correcta

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación de **RemoveImContactFromGroup** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImContactFromGroupResponse ResponseClass="Success" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="removeimcontactfromgroup-operation-errorinvalidimcontactid-error-response"></a>RemoveImContactFromGroup Operation ErrorInvalidImContactId error Response

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **RemoveImContactFromGroup** . La siguiente respuesta de error se produce cuando se realiza un intento de quitar un elemento de contacto que no existe en el grupo de mensajería instantánea. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="349" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <RemoveImContactFromGroupResponse ResponseClass="Error" 
                                        xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>The specified Im Contact Id is invalid.</MessageText>
         <ResponseCode>ErrorInvalidImContactId</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </RemoveImContactFromGroupResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [RemoveImContactFromGroupResponse](removeimcontactfromgroupresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Personas y contactos de EWS en Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
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
    

