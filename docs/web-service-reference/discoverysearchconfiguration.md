---
title: DiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 085384f9-dca4-4534-82e2-dd782471d0da
description: El elemento DiscoverySearchConfiguration especifica la configuración de la búsqueda de exhibición de documentos electrónicos.
ms.openlocfilehash: 8819d951f35ccc215bdf0128d2a16b60bbf20f2a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529059"
---
# <a name="discoverysearchconfiguration"></a>DiscoverySearchConfiguration

El elemento **DiscoverySearchConfiguration** especifica la configuración de la búsqueda de exhibición de documentos electrónicos. 
  
```XML
<DiscoverySearchConfiguration>
    <SearchId></SearchId>
    <SearchQuery></SearchQuery>
    <SearchableMailboxes></SearchableMailboxes>
</DiscoverySearchConfiguration>
```

 **DiscoverySearchConfigurationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |Especifica el identificador de la búsqueda.  <br/> |
|[SearchQuery](searchquery.md) <br/> |Especifica el nombre de una consulta de búsqueda de exhibición de documentos electrónicos.  <br/> |
|[SearchableMailboxes](searchablemailboxes.md) <br/> |Contiene una lista de los buzones devueltos por una solicitud **GetSearchableMailboxes** .  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DiscoverySearchConfigurations](discoverysearchconfigurations.md) <br/> |Especifica una matriz de elementos **DiscoverySearchConfiguration** .  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

