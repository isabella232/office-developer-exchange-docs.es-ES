---
title: Operación GetAppManifests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Busque información sobre la EWS GetAppManifests operación.
ms.openlocfilehash: 9c919bac9ac0042890d1c439454b37e6b7c60876
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764741"
---
# <a name="getappmanifests-operation"></a>Operación GetAppManifests

Obtenga información acerca de la operación de EWS **GetAppManifests** . 
  
La operación **GetAppManifests** recupera manifiestos de aplicaciones. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getappmanifests-operation"></a>Mediante la operación GetAppManifests

La operación **GetAppManifests** no toma ningún argumento para solicitar los manifiestos de aplicación para un buzón de correo. La respuesta contendrá con codificación base64 archivos de manifiesto XML para cada aplicación que se instala en un buzón de correo. 
  
### <a name="getappmanifests-operation-soap-headers"></a>Encabezados SOAP de operación de GetAppManifests

La operación de **GetAppManifests** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Este encabezado es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Este encabezado es aplicable a una respuesta.  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a>Ejemplo de solicitud de operación de GetAppManifests: obtener los manifiestos de aplicación para un buzón de correo

El siguiente ejemplo de una solicitud de operación **GetAppManifests** muestra cómo obtener los manifiestos de aplicación para un buzón de correo. El elemento [ApiVersionSupported](apiversionsupported.md) y el elemento de [SchemaVersionSupported](schemaversionsupported.md) son opcionales. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013_SP1" />
      <t:MailboxCulture>en-US</t:MailboxCulture>
      <t:TimeZoneContext>
         <t:TimeZoneDefinition Id="GMT Standard Time"/>
      </t:TimeZoneContext>
   </soap:Header>
   <soap:Body >
      <m:GetAppManifests>
        <m:ApiVersionSupported>1.1</m:ApiVersionSupported>
        <m:SchemaVersionSupported>1.1</m:SchemaVersionSupported>
      </m:GetAppManifests>
   </soap:Body>
</soap:Envelope>

```

La solicitud SOAP body contiene el elemento siguiente:
  
- [GetAppManifests](getappmanifests.md)
    
- [ApiVersionSupported](apiversionsupported.md)
    
- [SchemaVersionSupported](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a>Respuesta es correcta de operación GetAppManifests

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetAppManifests** para obtener los manifiestos de aplicación para un buzón de correo. 
  
> [!NOTE]
> Se ha truncado arbitrariamente todos los manifiestos de aplicación de base64 para conservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetAppManifestsResponse](getappmanifestsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [Aplicaciones](apps.md)
    
- [App](app.md)
    
- [Manifest](manifest.md)
    
El cuerpo del mensaje SOAP de respuesta también puede contener el elemento siguiente:
  
- [Manifiestos](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a>Respuesta de error de la operación de GetAppManifests

Los errores devueltos para esta operación están relacionados con un formato no válido de los parámetros de entrada o son los errores EWS genéricos. Para códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a>Ver también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación DisableApp](disableapp-operation.md)
    
- [Operación InstallApp](installapp-operation.md)
    
- [Operación UninstallApp](uninstallapp-operation.md)
    
- [Operación GetAppMarketplaceUrl](getappmarketplaceurl-operation.md)
    

