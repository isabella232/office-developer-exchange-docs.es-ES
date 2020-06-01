---
title: Operación GetAppManifests
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 21a4987c-c24d-4a6e-ace4-e81edcda6303
description: Buscar información sobre la operación de EWS de GetAppManifests.
ms.openlocfilehash: 4d4c1d32f14cf144335ddfdf8c9cd4c88a4421d0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463009"
---
# <a name="getappmanifests-operation"></a>Operación GetAppManifests

Buscar información sobre la operación de EWS de **GetAppManifests** . 
  
La operación **GetAppManifests** recupera los manifiestos de la aplicación. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getappmanifests-operation"></a>Uso de la operación GetAppManifests

La operación **GetAppManifests** no toma ningún argumento para solicitar los manifiestos de aplicación de un buzón. La respuesta contendrá archivos de manifiesto XML codificados en base64 para cada aplicación que esté instalada en un buzón. 
  
### <a name="getappmanifests-operation-soap-headers"></a>Encabezados SOAP de operación GetAppManifests

La operación **GetAppManifests** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="getappmanifests-operation-request-example-get-the-app-manifests-for-a-mailbox"></a>Ejemplo de solicitud de operación GetAppManifests: obtener los manifiestos de aplicación de un buzón de correo

El siguiente ejemplo de una solicitud de operación de **GetAppManifests** muestra cómo obtener los manifiestos de aplicación para un buzón de correo. El elemento [ApiVersionSupported](apiversionsupported.md) y el elemento [SchemaVersionSupported](schemaversionsupported.md) son opcionales. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
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

El cuerpo SOAP de la solicitud contiene el siguiente elemento:
  
- [GetAppManifests](getappmanifests.md)
    
- [ApiVersionSupported](apiversionsupported.md)
    
- [SchemaVersionSupported](schemaversionsupported.md)
    
## <a name="successful-getappmanifests-operation-response"></a>Respuesta de operación GetAppManifests correcta

En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación de **GetAppManifests** para obtener los manifiestos de aplicación de un buzón. 
  
> [!NOTE]
> Todos los manifiestos de aplicación Base64 se han truncado arbitrariamente para preservar la legibilidad. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="918" 
                           MinorBuildNumber="07" 
                           Version="V2_10" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetAppManifestsResponse ResponseClass="Success" 
                               xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <m:Apps xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
          <t:App xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
            <t:Manifest>WNlQXBwPg==</t:Manifest>
          </t:App>
         </m:Apps>
      </GetAppManifestsResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [GetAppManifestsResponse](getappmanifestsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [Aplicaciones](apps.md)
    
- [App](app.md)
    
- [Manifiesto](manifest.md)
    
El cuerpo SOAP de respuesta también puede contener el siguiente elemento:
  
- [Manifiestos](manifests.md)
    
## <a name="getappmanifests-operation-error-response"></a>Respuesta de error de operación de GetAppManifests

Los errores devueltos para esta operación están relacionados con un formato no válido de los parámetros de entrada o son errores genéricos de EWS. Para los códigos de error que son genéricos para EWS y específicos de esta operación, vea [ResponseCode](responsecode.md).
  
```
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <ServerVersionInfo MajorVersion="15"
                       MinorVersion="0"
                       MajorBuildNumber="918"
                       MinorBuildNumber="07"
                       Version="V2_10"
                       xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <GetAppManifestsResponse ResponseClass="Error"
                             xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <MessageText>The apiVersionSupported parameter is invalid. 
                   It should be in the form of major version, minor 
                   version, separated by '.', for example '2.34'.</MessageText>
      <ResponseCode>ErrorInvalidRequest</ResponseCode>
      <DescriptiveLinkKey>0</DescriptiveLinkKey>
    </GetAppManifestsResponse>
  </s:Body>
</s:Envelope>

```

## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación DisableApp](disableapp-operation.md)
    
- [Operación InstallApp](installapp-operation.md)
    
- [Operación UninstallApp](uninstallapp-operation.md)
    
- [Operación GetAppMarketplaceUrl](getappmarketplaceurl-operation.md)
    

