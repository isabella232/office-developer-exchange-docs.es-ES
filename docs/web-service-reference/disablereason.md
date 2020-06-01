---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: El elemento DisableReason especifica el motivo por el que se deshabilita una aplicación.
ms.openlocfilehash: 1406d69647bde5389dc9bb61adf7537a57d5adfc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463674"
---
# <a name="disablereason"></a>DisableReason

El elemento **DisableReason** especifica el motivo por el que se deshabilita una aplicación. 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 **DisableReasonType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DisableApp](disableapp.md) <br/> |Especifica una solicitud para deshabilitar una aplicación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valor de texto del elemento DisableReason**

|**Valor**|**Descripción**|
|:-----|:-----|
|Noreason  <br/> |Sin motivo dado  <br/> |
|OutlookClientPerformance  <br/> |Mejorar el rendimiento del cliente de correo electrónico.  <br/> |
|OWAClientPerformance  <br/> |Para mejorar el rendimiento del cliente de la aplicación Web.  <br/> |
|MobileClientPerformance  <br/> |Mejorar el rendimiento del cliente móvil.  <br/> |
   
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

