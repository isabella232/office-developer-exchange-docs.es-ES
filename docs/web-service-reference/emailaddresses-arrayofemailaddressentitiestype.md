---
title: EmailAddresses (ArrayOfEmailAddressEntitiesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2fc4a8e8-5377-4059-8fb4-3fdabfd30fe3
description: El elemento EmailAddresses especifica una matriz de entidades de la dirección de correo electrónico.
ms.openlocfilehash: 8d96d49ef2420f269197e47577efb956daa64e53
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764347"
---
# <a name="emailaddresses-arrayofemailaddressentitiestype"></a>EmailAddresses (ArrayOfEmailAddressEntitiesType)

El elemento **EmailAddresses** especifica una matriz de entidades de la dirección de correo electrónico. 
  
```XML
<EmailAddresses>
    <EmailAddressEntity></EmailAddressEntity>
</EmailAddresses>
```

 **ArrayOfEmailAddressEntitiesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[EmailAddressEntity](emailaddressentity.md) <br/> |Especifica una entidad de dirección de correo electrónico única.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[EntityExtractionResult](entityextractionresult.md) <br/> |Especifica la propiedad **EntityExtractionResult** de un elemento.  <br/> |
   
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

