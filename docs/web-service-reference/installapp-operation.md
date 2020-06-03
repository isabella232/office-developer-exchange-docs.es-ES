---
title: Operación InstallApp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 596eae95-3e78-489a-8bb2-d2dd4a026405
description: Buscar información sobre la operación de EWS de InstallApp.
ms.openlocfilehash: ae6aab7f7176aa827bafa9abf1aa67d458d309d2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465691"
---
# <a name="installapp-operation"></a>Operación InstallApp

Buscar información sobre la operación de EWS de **InstallApp** . 
  
La operación **InstallApp** instala una aplicación de correo para Outlook en un buzón. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-installapp-operation"></a>Uso de la operación InstallApp

La operación **InstallApp** toma un argumento único que identifica una aplicación de correo que se va a instalar. El argumento contiene el manifiesto codificado en base64 para una aplicación de correo. 
  
### <a name="installapp-operation-soap-headers"></a>Encabezados SOAP de operación InstallApp

La operación **InstallApp** puede usar los encabezados SOAP que se enumeran en la tabla siguiente. 
  
|**Nombre de encabezado**|**Elemento**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de operación. Este encabezado se aplica a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que respondió a la solicitud. Este encabezado se aplica a una respuesta.  <br/> |
   
## <a name="installapp-operation-request-example-install-a-mail-app-in-a-mailbox"></a>Ejemplo de solicitud de operación InstallApp: instalar una aplicación de correo en un buzón

El siguiente ejemplo de una solicitud de operación de **InstallApp** muestra cómo instalar una aplicación de correo para Outlook. El manifiesto de la aplicación puede encontrarse mediante la [operación GetAppManifests](getappmanifests-operation.md).
  
> [!NOTE]
> El manifiesto de la aplicación codificado en Base64 se ha truncado arbitrariamente para preservar la legibilidad y no representa un manifiesto válido. 
  
```XML
<?xml version="1.0" encoding="UTF-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body >
      <m:InstallApp>
         <m:Manifest>TUwiIC8+CiAgPC9SdWxlPgo8L09mZmljZUFwcD4=</m:Manifest>
      </m:InstallApp>
   </soap:Body>
</soap:Envelope>

```

El cuerpo SOAP de la solicitud contiene los siguientes elementos:
  
- [InstallApp](installapp.md)
    
- [Manifiesto](manifest.md)
    
## <a name="successful-installapp-operation-response"></a>Respuesta de operación InstallApp correcta

En el siguiente ejemplo se muestra una respuesta correcta a una solicitud de operación **InstallApp** para instalar una aplicación de correo. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Success" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>
```

El cuerpo SOAP de respuesta contiene los siguientes elementos:
  
- [InstallAppResponse](installappresponse.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="installapp-operation-error-response"></a>Respuesta de error de operación de InstallApp

En el ejemplo siguiente se muestra una respuesta de error a una solicitud de operación **InstallApp** . Se trata de una respuesta a una solicitud que contiene un manifiesto no válido. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="556" 
                           MinorBuildNumber="14" 
                           Version="Exchange2013" 
                           xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <InstallAppResponse ResponseClass="Error" 
                          xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
         <MessageText>This app can't be installed. Missing OfficeApp element.</MessageText>
         <ResponseCode>ErrorInternalServerError</ResponseCode>
         <DescriptiveLinkKey>0</DescriptiveLinkKey>
      </InstallAppResponse>
   </s:Body>
</s:Envelope>

```

El cuerpo SOAP de respuesta de error contiene los siguientes elementos:
  
- [InstallAppResponse](installappresponse.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Vea también

- [Operaciones de EWS en Exchange](ews-operations-in-exchange.md)
    
- [Operación DisableApp](disableapp-operation.md)
    
- [Operación UninstallApp](uninstallapp-operation.md)
    
- [GetAppManifests](getappmanifests.md)
    
- [Operación GetAppMarketplaceUrl](getappmarketplaceurl-operation.md)
    

