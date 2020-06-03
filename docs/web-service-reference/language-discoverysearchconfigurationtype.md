---
title: Idioma (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: El elemento Language (DiscoverySearchConfigurationType) identifica la referencia cultural que se va a usar para el formato específico de la referencia cultural de los intervalos de fechas. También especifica el idioma usado en una consulta de búsqueda.
ms.openlocfilehash: 3cf85525147bec5d6dfc6fe2b2af5916d42c44be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463289"
---
# <a name="language-discoverysearchconfigurationtype"></a>Idioma (DiscoverySearchConfigurationType)

El elemento **Language (DiscoverySearchConfigurationType)** identifica la referencia cultural que se va a usar para el formato específico de la referencia cultural de los intervalos de fechas. También especifica el idioma usado en una consulta de búsqueda. 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **Language (DiscoverySearchConfigurationType)** es una referencia cultural o un lenguaje. 
  
## <a name="remarks"></a>Comentarios

Este elemento especifica el formato de los intervalos de fechas especificados en la [operación SearchMailboxes](searchmailboxes-operation.md) o en la [operación SetHoldOnMailboxes](setholdonmailboxes-operation.md).
  
Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

