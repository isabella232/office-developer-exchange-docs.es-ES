---
title: DocumentSharingLocations (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 394f6015-721b-4800-9286-039d430f09b3
description: El elemento DocumentSharingLocations contiene una lista de la ubicación y la información de metadatos de una ubicación de uso compartido de documentos.
ms.openlocfilehash: 179ad59e51b0519fa95b4031f5c9df52a44dba1a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538341"
---
# <a name="documentsharinglocations-soap"></a>DocumentSharingLocations (SOAP)

El **elemento DocumentSharingLocations** contiene una lista de la ubicación y la información de metadatos de una ubicación de uso compartido de documentos. 
  
```XML
<DocumentSharingLocations>
   <DocumentSharingLocation />
</DocumentSharingLocations>
```

 **DocumentSharingLocations**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocation (SOAP)](documentsharinglocation-soap.md) <br/> |Contiene la ubicación y los metadatos de una ubicación de uso compartido de documentos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DocumentSharingLocationCollectionSetting (SOAP)](documentsharinglocationcollectionsetting-soap.md) <br/> |Representa una configuración de usuario que es una colección de ubicaciones y metadatos de uso compartido de documentación.  <br/> |
   
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|Nombre de esquema  <br/> |Esquema de detección automática  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también

- [Operación GetUserSettings (SOAP)](getusersettings-operation-soap.md)
- [Referencia del servicio web de Detección automática para Exchange](autodiscover-web-service-reference-for-exchange.md)
- [Elementos XML de detección automática soap para Exchange 2013](soap-autodiscover-xml-elements-for-exchange-2013.md)

