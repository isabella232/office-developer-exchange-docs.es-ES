---
title: Request (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 3ea026fc-74f1-4118-86ae-908ed4f82a4b
description: El elemento request contiene una solicitud para devolver la configuración del dominio.
ms.openlocfilehash: c5f666102be8aaeee001a23706732e9e6c44b560
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459591"
---
# <a name="request-getdomainsettings-soap"></a>Request (GetDomainSettings) (SOAP)

El elemento **request** contiene una solicitud para devolver la configuración del dominio. 
  
```xml
<Request>
   <Domains/>
   <RequestedSettings/>
</Request>
```

 **GetDomainSettingsRequest**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa los dominios de las configuraciones que se devuelven en una [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) o los dominios que la organización ha federado en una [operación GetFederationInformation (SOAP)](getfederationinformation-operation-soap.md).  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración solicitadas.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetDomainSettingsRequestMessage (SOAP)](getdomainsettingsrequestmessage-soap.md) <br/> |Representa una solicitud de [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md).  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

