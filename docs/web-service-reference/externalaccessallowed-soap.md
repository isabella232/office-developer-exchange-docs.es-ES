---
title: ExternalAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 967df8c0-ee95-4202-b037-0c4b9fbbf5ee
description: El elemento ExternalAccessAllowed indica si un documento de ubicación de uso compartido está disponible a fuera de las conexiones.
ms.openlocfilehash: 7d2a4027fe6de0c24191272d65605310af6a16bf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764550"
---
# <a name="externalaccessallowed-soap"></a>ExternalAccessAllowed (SOAP)

El elemento **ExternalAccessAllowed** indica si un documento de ubicación de uso compartido está disponible a fuera de las conexiones. 
  
```XML
<ExternalAccessAllowed /> 
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Representa información de ubicación y los metadatos de un documento de ubicación de uso compartido.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de tipo Boolean del elemento **ExternalAccessAllowed** indica si la ubicación de uso compartida está disponible a fuera de las conexiones. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)


[Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

