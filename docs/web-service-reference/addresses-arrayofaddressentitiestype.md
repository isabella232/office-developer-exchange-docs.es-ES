---
title: Direcciones (ArrayOfAddressEntitiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c1f3fd3-1b78-46ee-8dd4-b2aff51e767e
description: El elemento Addresses especifica una matriz de elementos AddressEntity.
ms.openlocfilehash: 48cf8c0fda6a8ef894ef8d3a4c154f7255b218bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463632"
---
# <a name="addresses-arrayofaddressentitiestype"></a>Direcciones (ArrayOfAddressEntitiesType)

El elemento **Addresses** especifica una matriz de elementos **AddressEntity** . 
  
```XML
<Addresses>
   <AddressEntity/>
</Addresses>
```

 **ArrayOfAddressEntitiesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AddressEntity](addressentity.md) <br/> |Especifica una única entidad de dirección.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |Especifica la propiedad **EntityExtractionResult** de un elemento.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

