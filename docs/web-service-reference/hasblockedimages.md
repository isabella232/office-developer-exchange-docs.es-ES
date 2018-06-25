---
title: HasBlockedImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddeb11db-797d-4939-91d5-3e44be5f0778
description: El elemento HasBlockedImages especifica un valor booleano que indica si el elemento ha bloqueado las imágenes.
ms.openlocfilehash: fbe9967c898016aeef27e3c86e8a1cf603bd87fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835795"
---
# <a name="hasblockedimages"></a>HasBlockedImages

El elemento **HasBlockedImages** especifica un valor booleano que indica si el elemento ha bloqueado las imágenes. 
  
```XML
<HasBlockedImages> true | false </HasBlockedImages>
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
|[Item](item.md) <br/> |Representa un elemento genérico en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** para el elemento **HasBlockedImages** indica que el elemento ha bloqueado las imágenes. Un valor de **false** indica que el elemento no tiene ningún imágenes bloqueadas. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

