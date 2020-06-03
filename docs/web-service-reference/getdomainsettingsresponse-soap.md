---
title: GetDomainSettingsResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 43ebd17b-3a70-4878-9254-97a4c2c87b77
description: El elemento GetDomainSettingsResponse representa la respuesta a una operación GetDomainSettings (SOAP), que devuelve la configuración del dominio.
ms.openlocfilehash: 94cb202948e6a0d5a34f5547132c052d1d1b6a40
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461880"
---
# <a name="getdomainsettingsresponse-soap"></a>GetDomainSettingsResponse (SOAP)

El elemento **GetDomainSettingsResponse** representa la respuesta a una [operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md), que devuelve la configuración del dominio.
  
```XML
<GetDomainSettingsResponse>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</GetDomainSettingsResponse>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contiene una matriz de respuestas para la configuración de cada dominio solicitado.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Representa un código de error devuelto por el servicio de detección automática.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Representa un mensaje que está asociado con un código de error devuelto por el servicio de detección automática.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
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

