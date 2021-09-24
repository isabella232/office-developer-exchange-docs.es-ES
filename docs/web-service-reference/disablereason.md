---
title: DisableReason
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f41b5be6-9b79-4e83-8cdb-aa779e13cb3f
description: El elemento DisableReason especifica el motivo para deshabilitar una aplicación.
ms.openlocfilehash: 8156dac17e81dd1c3f49575491924185b04d53e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528839"
---
# <a name="disablereason"></a>DisableReason

El **elemento DisableReason** especifica el motivo para deshabilitar una aplicación. 
  
```XML
<DisableReason> NoReason | OutlookClientPerformance | OWAClientPerformance | MobileClientPerformance </DisableReason>
```

 **DisableReasonType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[DisableApp](disableapp.md) <br/> |Especifica una solicitud para deshabilitar una aplicación.  <br/> |
   
## <a name="text-value"></a>Valor de texto

**Valor de texto del elemento DisableReason**

|**Valor**|**Descripción**|
|:-----|:-----|
|NoReason  <br/> |No se ha dado ninguna razón  <br/> |
|OutlookClientPerformance  <br/> |Para mejorar el rendimiento del cliente de correo electrónico.  <br/> |
|OWAClientPerformance  <br/> |Para mejorar el rendimiento del cliente de la aplicación web.  <br/> |
|MobileClientPerformance  <br/> |Para mejorar el rendimiento del cliente móvil.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

