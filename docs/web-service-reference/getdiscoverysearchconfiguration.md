---
title: GetDiscoverySearchConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e15dbfca-3b9d-463e-94ec-4f1b6115bee3
description: El elemento GetDiscoverySearchConfiguration especifica una solicitud para recuperar la configuración de búsqueda de exhibición de documentos electrónicos.
ms.openlocfilehash: ff84e648e14b79f64cf2a769c83aae28791790ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519691"
---
# <a name="getdiscoverysearchconfiguration"></a>GetDiscoverySearchConfiguration

El **elemento GetDiscoverySearchConfiguration** especifica una solicitud para recuperar la configuración de búsqueda de exhibición de documentos electrónicos. 
  
```XML
<GetDiscoverySearchConfiguration>
    <SearchId/>
    <ExpandGroupMembership/>
</GetDiscoverySearchConfiguration>
```

 **GetDiscoverySearchConfigurationType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SearchId](searchid.md) <br/> |Especifica el identificador de la búsqueda.  <br/> |
|[ExpandGroupMembership](expandgroupmembership.md) <br/> |Contiene un valor booleano que indica si se va a expandir la pertenencia al grupo devuelto desde una **solicitud GetSearchableMailboxes.**  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

