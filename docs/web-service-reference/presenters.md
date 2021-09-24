---
title: Moderadores
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 01057872-4f1a-4246-86ba-73d10ef854a0
description: El elemento Presenters especifica los presentadores de una reunión en línea.
ms.openlocfilehash: 1c9bf9093450e675245b647c98d7b1d00101ce9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519147"
---
# <a name="presenters"></a>Moderadores

El **elemento Presenters** especifica los presentadores de una reunión en línea. 
  
```XML
<Presenters> Disabled | Internal | Everyone </Presenters>
```

 **PresentersType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[OnlineMeetingSettings](onlinemeetingsettings.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento Presenters** es el tipo de usuarios que pueden ser moderadores de una reunión en línea. Los valores de texto del **elemento Presenters** se describen en la tabla siguiente. 
  
**Valores de texto del elemento Presenters**

|**Valor**|**Descripción**|
|:-----|:-----|
|Deshabilitado  <br/> |Los presentadores están deshabilitados.  <br/> |
|Interno  <br/> |Solo los participantes internos pueden ser presentadores.  <br/> |
|Todos  <br/> |Cualquier participante puede ser moderador.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

