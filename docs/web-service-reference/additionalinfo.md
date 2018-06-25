---
title: AdditionalInfo
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 50bebbab-2fef-4a27-a5a9-32d7200820b6
description: El elemento AdditionalInfo especifica información adicional sobre el estado de espera de un buzón de correo.
ms.openlocfilehash: 6fbe24d5d3e41f2ba9c81657b2c38240d10eefed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763405"
---
# <a name="additionalinfo"></a>AdditionalInfo

El elemento **AdditionalInfo** especifica información adicional sobre el estado de espera de un buzón de correo. 
  
```XML
<AdditionalInfo></AdditionalInfo>
```

 **xs: String**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[MailboxHoldStatus](mailboxholdstatus.md) <br/> |Especifica el estado de retención del buzón.  <br/> |
|[NonIndexableItemDetail](nonindexableitemdetail.md) <br/> |Especifica los detalles de un elemento que no se pueden indizar.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento AdditionalInfo es información adicional sobre el estado de espera de un buzón de correo.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
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

