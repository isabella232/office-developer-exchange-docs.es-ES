---
title: DomainResponse (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 6aa319be-3a01-4044-8dfc-8fa1318524c3
description: El elemento DomainResponse contiene la configuración solicitada para el dominio especificado.
ms.openlocfilehash: fb7288b55452d8499596ce09c3ada9cec4b88d5b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517206"
---
# <a name="domainresponse-soap"></a>DomainResponse (SOAP)

El **elemento DomainResponse** contiene la configuración solicitada para el dominio especificado. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DomainSettingErrors (SOAP)](domainsettingerrors-soap.md) <br/> |Contiene información de error para la configuración que no se pudo devolver.  <br/> |
|[DomainSettings (SOAP)](domainsettings-soap.md) <br/> |Representa la configuración de dominio enviada en una solicitud de detección automática o devuelta por una respuesta de detección automática.  <br/> |
|[RedirectTarget (SOAP)](redirecttarget-soap.md) <br/> |Identifica el destino del redireccionamiento. El destino puede ser una dirección URL o una dirección de correo electrónico.  <br/> |
|[ErrorCode (SOAP)](errorcode-soap.md) <br/> |Especifica el código de error asociado a la solicitud específica.  <br/> |
|[ErrorMessage (SOAP)](errormessage-soap.md) <br/> |Especifica el mensaje de error asociado a la solicitud específica.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ArrayOfDomainResponse (SOAP)](arrayofdomainresponse-soap.md) <br/> |Contiene una matriz de **elementos DomainResponse.** Cada **elemento DomainResponse** contiene la configuración solicitada para el usuario especificado.  <br/> |
|[DomainResponses (SOAP)](domainresponses-soap.md) <br/> |Contiene las respuestas de cada dominio.  <br/> |
   
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

- [Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

