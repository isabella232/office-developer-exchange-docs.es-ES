---
title: ExternalAccessAllowed (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 967df8c0-ee95-4202-b037-0c4b9fbbf5ee
description: El elemento ExternalAccessAllowed indica si una ubicación de uso compartido de documentos está disponible para conexiones externas.
ms.openlocfilehash: eb0ce0067a9ac9deea78b2778ce7f9e493ffb26f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457966"
---
# <a name="externalaccessallowed-soap"></a>ExternalAccessAllowed (SOAP)

El elemento **ExternalAccessAllowed** indica si una ubicación de uso compartido de documentos está disponible para conexiones externas. 
  
```XML
<ExternalAccessAllowed /> 
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Representa la información de ubicación y metadatos de una ubicación de uso compartido de documentos.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor booleano del elemento **ExternalAccessAllowed** indica si la ubicación de uso compartido está disponible para las conexiones externas. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)


[Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
  
[Elementos XML de detección automática de SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

