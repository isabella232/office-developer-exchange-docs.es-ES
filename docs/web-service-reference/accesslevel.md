---
title: AccessLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 09475586-00fa-4e82-a915-5ca263ab4d1c
description: El elemento AccessLevel especifica el nivel de acceso para una reunión en línea.
ms.openlocfilehash: 1bf0a191fad529b555117e4ff992c352615bc79b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764536"
---
# <a name="accesslevel"></a>AccessLevel

El elemento **AccessLevel** especifica el nivel de acceso para una reunión en línea. 
  
```XML
<AccessLevel/>
```

 **OnlineMeetingSettingsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |Especifica la configuración de las reuniones en línea.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores de texto para el elemento **AccessLevel** . 
  
**Valores de texto del elemento AccessLevel**

|**Valor**|**Descripción**|
|:-----|:-----|
|Todos los usuarios  <br/> |El nivel de acceso está abierto a todos.  <br/> |
|Interno  <br/> |El nivel de acceso sólo es interno.  <br/> |
|Invitados  <br/> |El nivel de acceso es sólo a los participantes invitados.  <br/> |
|Bloqueado  <br/> |El nivel de acceso está bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

