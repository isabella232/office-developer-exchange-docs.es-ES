---
title: Response (GetDomainSettings) (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a5b052df-93bd-4fe1-ac30-83de9a3dfcd7
description: El elemento Response representa la respuesta a una llamada GetDomainSettings para un dominio individual.
ms.openlocfilehash: e8f76127d5e812bc6805430544fe334eabd29ffa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540555"
---
# <a name="response-getdomainsettings-soap"></a>Response (GetDomainSettings) (SOAP)

El **elemento Response** representa la respuesta a una llamada **GetDomainSettings** para un dominio individual. 
  
```XML
<Response>
   <DomainResponses/>
   <ErrorCode/>
   <ErrorMessage/>
</Response>
```

 **GetDomainSettingsResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contiene la respuesta para cada dominio solicitado en una **solicitud GetDomainSettings.**  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Contiene el código de error asociado a la respuesta, si procede.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Contiene el mensaje de error asociado a la respuesta, si procede.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetDomainSettingsResponseMessage (SOAP)](getdomainsettingsresponsemessage-soap.md) <br/> |Devuelve al autor de la llamada las opciones de configuración del dominio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

