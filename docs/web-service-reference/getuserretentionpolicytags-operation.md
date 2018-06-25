---
title: Operación GetUserRetentionPolicyTags
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 57c6ff23-5c2c-42ee-824b-5a1b6dafab8c
description: Busque información sobre la EWS GetUserRetentionPolicyTags operación.
ms.openlocfilehash: 2b1267ce6822c7bad05ad2ef88547ba75c632ab0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835700"
---
# <a name="getuserretentionpolicytags-operation"></a>Operación GetUserRetentionPolicyTags

Obtenga información acerca de la operación de EWS **GetUserRetentionPolicyTags** . 
  
La operación **GetUserRetentionPolicyTags** Obtiene una lista de todos los de forma predeterminada, carpeta del sistema y etiquetas personales que se asocian a un usuario por medio de una directiva del sistema o que se han aplicado por el usuario. 
  
Esta operación se introdujo en Exchange Server 2013.
  
## <a name="using-the-getuserretentionpolicytags-operation"></a>Mediante la operación GetUserRetentionPolicyTags

Esta operación devuelve el nombre para mostrar, identificador de retención, período de retención, tipo de retención, acción de retención y las etiquetas de descripción y los valores de las propiedades **IsVisible**, **OptedInto**y **IsArchive** . 
  
### <a name="getuserretentionpolicytags-operation-soap-headers"></a>Encabezados SOAP de operación de GetUserRetentionPolicyTags

La operación de **GetUserRetentionPolicyTags** puede utilizar los encabezados SOAP que se enumeran en la siguiente tabla. 
  
|**Nombre de encabezado**|**Element**|**Descripción**|
|:-----|:-----|:-----|
|**RequestVersion** <br/> |[RequestServerVersion](requestserverversion.md) <br/> |Identifica la versión del esquema para la solicitud de la operación. Esto es aplicable a una solicitud.  <br/> |
|**ServerVersion** <br/> |[ServerVersionInfo](serverversioninfo.md) <br/> |Identifica la versión del servidor que ha respondido a la solicitud. Esto es aplicable a una respuesta.  <br/> |
   
## <a name="getuserretentionpolicytags-operation-request-example"></a>Ejemplo de solicitud de operación de GetUserRetentionPolicyTags

El siguiente ejemplo de una solicitud de operación **GetUserRetentionPolicyTags** muestra cómo obtener una lista de etiquetas para el usuario actual. 
  
```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages">
   <soap:Header>
      <t:RequestServerVersion Version="Exchange2013" />
   </soap:Header>
   <soap:Body>
      <m:GetUserRetentionPolicyTags />
   </soap:Body>
</soap:Envelope>
```

La solicitud SOAP body contiene el elemento siguiente:
  
- [GetUserRetentionPolicyTags](getuserretentionpolicytags.md)
    
## <a name="successful-getuserretentionpolicytags-operation-response"></a>Respuesta es correcta de operación GetUserRetentionPolicyTags

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de operación **GetUserRetentionPolicyTags** . 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
   <s:Header>
      <h:ServerVersionInfo MajorVersion="15" 
                           MinorVersion="0" 
                           MajorBuildNumber="179" 
                           MinorBuildNumber="0" 
                           Version="Exchange2013" 
                           xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns:xsd="http://www.w3.org/2001/XMLSchema" 
                           xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
   </s:Header>
   <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <GetUserRetentionPolicyTagsResponse ResponseClass="Success" 
                                          xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
         <ResponseCode>NoError</ResponseCode>
         <RetentionPolicyTags>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>1 Year Delete</DisplayName>
               <RetentionId>e66252f9-794f-4b36-b55e-d6d95fdf87a3</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>true</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Personal 1 year move to archive</DisplayName>
               <RetentionId>b2a29464-649c-4174-932b-6aaac9811c89</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>MoveToArchive</RetentionAction>
               <Description/>
               <IsVisible>true</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>true</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Sent Items</DisplayName>
               <RetentionId>b0d32f1b-fbd0-4c1d-ba3e-ddd1086ea1d3</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>SentItems</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Default 1 year delete</DisplayName>
               <RetentionId>29fc9b9d-98b0-4c01-acf8-3996e2afce98</RetentionId>
               <RetentionPeriod>365</RetentionPeriod>
               <Type>All</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Two Year Retention</DisplayName>
               <RetentionId>a1a38957-2557-404e-9f32-53d77c948f62</RetentionId>
               <RetentionPeriod>730</RetentionPeriod>
               <Type>Personal</Type>
               <RetentionAction>DeleteAndAllowRecovery</RetentionAction>
               <Description>Use this tag for all items to be retained for two years.</Description>
               <IsVisible>true</IsVisible>
               <OptedInto>true</OptedInto>
               <IsArchive>false</IsArchive>
            </RetentionPolicyTag>
            <RetentionPolicyTag xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
               <DisplayName>Default two year move to archive</DisplayName>
               <RetentionId>75bc8dbe-a0e8-4e09-9fa3-fd4c21f49318</RetentionId>
               <RetentionPeriod>730</RetentionPeriod>
               <Type>All</Type>
               <RetentionAction>MoveToArchive</RetentionAction>
               <Description/>
               <IsVisible>false</IsVisible>
               <OptedInto>false</OptedInto>
               <IsArchive>true</IsArchive>
            </RetentionPolicyTag>
         </RetentionPolicyTags>
      </GetUserRetentionPolicyTagsResponse>
   </s:Body>
</s:Envelope>

```

La respuesta SOAP body contiene los siguientes elementos:
  
- [GetUserRetentionPolicyTagsResponse](getuserretentionpolicytagsresponse.md)
    
- [ResponseCode](responsecode.md)
    
- [RetentionPolicyTags](retentionpolicytags.md)
    
- [RetentionPolicyTag](retentionpolicytag.md)
    
- [DisplayName (cadena)](displayname-string.md)
    
- [RetentionId](retentionid.md)
    
- [RetentionPeriod](retentionperiod.md)
    
- [Tipo (ElcFolderType)](type-elcfoldertype.md)
    
- [RetentionAction](retentionaction.md)
    
- [Descripción](description.md)
    
- [IsVisible](isvisible.md)
    
- [OptedInto](optedinto.md)
    
- [IsArchive](isarchive.md)
    
## <a name="getuserretentionpolicytags-operation-error-response"></a>Respuesta de error de la operación de GetUserRetentionPolicyTags

Para los códigos de error que son genéricos de EWS, consulte [ResponseCode](responsecode.md).
  
## <a name="see-also"></a>Vea también



[Directivas de retención de EWS](http://msdn.microsoft.com/library/a132872f-0228-4bcb-aac2-bf64fb07e58e%28Office.15%29.aspx)

