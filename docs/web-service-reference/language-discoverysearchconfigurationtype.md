---
title: Language (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: El elemento Language (DiscoverySearchConfigurationType) identifica la referencia cultural que se usará para el formato específico de la referencia cultural de los intervalos de fechas. También especifica el idioma usado en una consulta de búsqueda.
ms.openlocfilehash: 5d51960aa00b2c47d96972abc05e4d6027eeecb3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540898"
---
# <a name="language-discoverysearchconfigurationtype"></a>Language (DiscoverySearchConfigurationType)

El **elemento Language (DiscoverySearchConfigurationType)** identifica la referencia cultural que se usará para el formato específico de la referencia cultural de los intervalos de fechas. También especifica el idioma usado en una consulta de búsqueda. 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Language (DiscoverySearchConfigurationType)** es una referencia cultural o un idioma. 
  
## <a name="remarks"></a>Comentarios

Este elemento especifica el formato de intervalos de fechas especificado en la operación [SearchMailboxes](searchmailboxes-operation.md) o en la [operación SetHoldOnMailboxes](setholdonmailboxes-operation.md).
  
Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

