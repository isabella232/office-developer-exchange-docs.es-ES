---
title: Idioma (DiscoverySearchConfigurationType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 34eab81c-d832-4925-9f76-d69f24b36931
description: El elemento de idioma (DiscoverySearchConfigurationType) identifica la referencia cultural que se usará para el formato de referencias culturales específicas de los intervalos de fechas. También especifica el lenguaje utilizado en una consulta de búsqueda.
ms.openlocfilehash: 1e904ac4d7f525b2d12cfe83f0da33b9ed474066
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836197"
---
# <a name="language-discoverysearchconfigurationtype"></a>Idioma (DiscoverySearchConfigurationType)

El elemento de **idioma (DiscoverySearchConfigurationType)** identifica la referencia cultural que se usará para el formato de referencias culturales específicas de los intervalos de fechas. También especifica el lenguaje utilizado en una consulta de búsqueda. 
  
```XML
<Language />
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[DiscoverySearchConfiguration](discoverysearchconfiguration.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento de **idioma (DiscoverySearchConfigurationType)** es un idioma o referencia cultural. 
  
## <a name="remarks"></a>Notas

Este elemento especifica el formato de los intervalos de fechas especificado en la [operación de SearchMailboxes](searchmailboxes-operation.md) o la [operación SetHoldOnMailboxes](setholdonmailboxes-operation.md).
  
Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



[DiscoverySearchConfiguration](discoverysearchconfiguration.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

