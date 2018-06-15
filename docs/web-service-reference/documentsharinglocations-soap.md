---
title: DocumentSharingLocations (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 394f6015-721b-4800-9286-039d430f09b3
description: El elemento DocumentSharingLocations contiene una lista de ubicación y la información de metadatos de un documento de ubicación de uso compartido.
ms.openlocfilehash: 72d1ae9f01ad45441b4e255f2fb6353be2dc8d28
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19764260"
---
# <a name="documentsharinglocations-soap"></a>DocumentSharingLocations (SOAP)

El elemento **DocumentSharingLocations** contiene una lista de ubicación y la información de metadatos de un documento de ubicación de uso compartido. 
  
```XML
<DocumentSharingLocations>
   <DocumentSharingLocation />
</DocumentSharingLocations>
```

 **DocumentSharingLocations**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Contiene la ubicación y los metadatos de un documento de ubicación de uso compartido.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md) <br/> |Representa un usuario de configuración, es decir, una colección de documentación de uso compartido de las ubicaciones y los metadatos.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Referencia de servicio web de detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Elementos de Autodiscover XML SOAP para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

