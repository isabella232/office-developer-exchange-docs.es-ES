---
title: Operación AddImGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6df6e504-b7c8-4773-b10f-ffa5defac229
description: Busque información sobre la operación EWS AddImGroup.
ms.openlocfilehash: 9aba6a22502c1006da06ce4a9bc925f13b5b5100
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544363"
---
# <a name="addimgroup-operation"></a>Operación AddImGroup

Busque información sobre la **operación EWS AddImGroup.** 
  
La **operación AddImGroup** Exchange Web Services (EWS) agrega un nuevo grupo de mensajería instantánea (MI) a un buzón. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-addimgroup-operation"></a>Uso de la operación AddImGroup

La **operación AddImGroup** solo toma un único argumento de nombre para mostrar. 
  
Esta operación devuelve el nombre para mostrar, el tipo de grupo y el Exchange de almacén del nuevo grupo.
  
La **operación AddImGroup** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
**Tabla 1. Encabezados SOAP de operación AddImGroup**

|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**Suplantación** <br/> |[ExchangeImpersonation](exchangeimpersonation.md) <br/> |Identifica el usuario al que la aplicación cliente está suplantando. Esto es aplicable a una solicitud.  <br/> |
|**MailboxCulture** <br/> |[MailboxCulture](mailboxculture.md) <br/> |Identifica la referencia cultural, tal como se define en RFC 3066, "Etiquetas para la identificación de idiomas", que se usará para tener acceso al buzón. Esto es aplicable a una solicitud.  <br/> |
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Esto es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Esto es aplicable a una respuesta.  <br/> |
   
## <a name="addimgroup-operation-request-example-create-a-new-im-group"></a>Ejemplo de solicitud de operación AddImGroup: Crear un nuevo grupo de mensajería instantánea

En el siguiente ejemplo de una **solicitud de operación AddImGroup** se muestra cómo crear un grupo de mensajería instantánea denominado MyCustomerGroup. 
  
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
      <m:AddImGroup>
         <m:DisplayName>MyCustomGroup</m:DisplayName>
      </m:AddImGroup>
   </soap:Body>
</soap:Envelope>
```

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [AddImGroup](addimgroup.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
## <a name="successful-addimgroup-operation-response"></a>Respuesta de operación addImGroup correcta

En el ejemplo siguiente se muestra una respuesta correcta a una **solicitud de operación AddImGroup.** 
  
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
      <AddImGroupResponse ResponseClass="Success"
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <ImGroup>
            <DisplayName xmlns="https://schemas.microsoft.com/exchange/services/2006/types">MyCustomGroup</DisplayName>
            <GroupType xmlns="https://schemas.microsoft.com/exchange/services/2006/types">IPM.DistList.MOC.UserGroup</GroupType>
            <ExchangeStoreId Id="AAMkAGQ1MjJjMTBkLTc4Y2UtNDA5Ny04ZjU5LWI3MAAA="
                             ChangeKey="EgAAAA=="
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/types"/>
         </ImGroup>
      </AddImGroupResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de la respuesta contiene los siguientes elementos:
  
- [AddImGroupResponse](addimgroupresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [ImGroup](imgroup.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [GroupType](grouptype.md)
    
- [ExchangeStoreId](exchangestoreid.md)
    
## <a name="addimgroup-operation-error-response"></a>Respuesta de error de operación AddImGroup

En el ejemplo siguiente se muestra una respuesta de error a una **solicitud de operación AddImGroup.** Esta es una respuesta a una solicitud que contiene un carácter que no se puede usar en un nombre para mostrar. Tenga en cuenta que se trata de un error SOAP y no un mensaje de error basado en esquema. El nombre para mostrar enviado en la solicitud es ~!@#$%^ y el &amp; error se produce en el &amp; carácter. El &amp; carácter se produjo en la línea 11 y el carácter 33 en la carga de la solicitud. La respuesta se devolvió con un código HTTP 500. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Body>
      <s:Fault>
         <faultcode xmlns:a="https://schemas.microsoft.com/exchange/services/2006/types">a:ErrorSchemaValidation</faultcode>
         <faultstring xml:lang="en-US">The request failed schema validation: An error occurred while parsing EntityName. Line 11, position 33.</faultstring>
         <detail>
            <e:ResponseCode xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">ErrorSchemaValidation</e:ResponseCode>
            <e:Message xmlns:e="https://schemas.microsoft.com/exchange/services/2006/errors">The request failed schema validation.</e:Message>
            <t:MessageXml xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
               <t:LineNumber>11</t:LineNumber>
               <t:LinePosition>33</t:LinePosition>
               <t:Violation>An error occurred while parsing EntityName. Line 11, position 33.</t:Violation>
            </t:MessageXml>
         </detail>
      </s:Fault>
   </s:Body>
</s:Envelope>
```

## <a name="see-also"></a>Consulte también

- [Personas y contactos de EWS en Exchange](https://msdn.microsoft.com/library/043c33be-a0d1-4bad-a840-85715eda4813%28Office.15%29.aspx)
    
- [Operación RemoveImGroup](removeimgroup-operation.md)
    
- [SetImGroup](setimgroup.md)
    

