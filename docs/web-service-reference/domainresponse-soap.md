---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: El elemento DomainResponse contiene la configuración solicitada para el dominio especificado.
ms.openlocfilehash: c40f33a278b5032913329a7cd64346b572f5df2f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764265"
---
# <a name="domainresponse-soap"></a>DomainResponse (SOAP)

El elemento **DomainResponse** contiene la configuración solicitada para el dominio especificado. 
  
```XML
<DomainResponse>
   <DomainSettingErrors/>
   <DomainSettings/>
   <RedirectTarget/>
   <ErrorCode/>
   <ErrorMessage/>
</DomainResponse>
```

 **DomainResponse**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Contiene información de error de configuración que no se pudo devolver.  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Representa la configuración de dominio que se ha enviado en una solicitud de detección automática o devueltas por una respuesta de detección automática.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Identifica el destino de la redirección. El destino puede ser una dirección URL o una dirección de correo electrónico.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Especifica el código de error que está asociado a la solicitud específico.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Especifica el mensaje de error que está asociado a la solicitud específico.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |Contiene una matriz de elementos de **DomainResponse** . Cada elemento **DomainResponse** contiene la configuración solicitada para el usuario especificado.  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contiene las respuestas para cada dominio.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

