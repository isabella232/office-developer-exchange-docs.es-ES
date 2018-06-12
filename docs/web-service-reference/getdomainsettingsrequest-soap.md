---
title: GetDomainSettingsRequest (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 5ac0ff6d-9e02-4e4c-973d-cd9e076661d5
description: El elemento GetDomainSettingsRequest representa una solicitud de operación GetDomainSettings operación (SOAP).
ms.openlocfilehash: 4de525a9ba47a0d9afb0d6db9200fe32845f31d0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764813"
---
# <a name="getdomainsettingsrequest-soap"></a>GetDomainSettingsRequest (SOAP)

El elemento **GetDomainSettingsRequest** representa una solicitud de operación de la [operación de GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md) . 
  
```XML
<GetDomainSettingsRequest>
   <Domains/>
   <RequestedSettings/>
   <RequestedVersion/>
</GetDomainSettingsRequest>
```

 **GetDomainSettingsRequest**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Dominios (SOAP)](domains-soap.md) <br/> |Representa una colección de identificadores de dominio.  <br/> |
|[RequestedSettings (SOAP)](requestedsettings-soap.md) <br/> |Contiene los nombres de las opciones de configuración de dominio solicitado.  <br/> |
|[RequestedVersion (SOAP)](requestedversion-soap.md) <br/> |Especifica la versión del servidor que va a usar el proveedor.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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



[Operación GetDomainSettings (SOAP)](getdomainsettings-operation-soap.md)

