---
title: OnlineMeetingSettings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4c7af00c-8dca-40f4-9420-e042a0b5303c
description: El elemento OnlineMeetingSettings especifica la configuración de las reuniones en línea.
ms.openlocfilehash: dd830330ba1a09f04aca933853f4169e0cd78838
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836647"
---
# <a name="onlinemeetingsettings"></a>OnlineMeetingSettings

El elemento **OnlineMeetingSettings** especifica la configuración de las reuniones en línea. 
  
```XML
<OnlineMeetingSettings>
   <LobbyBypass/>
   <AccessLevel/>
   <Presenters/>
</OnlineMeetingSettings>
```

 **OnlineMeetingSettingsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[LobbyBypass](lobbybypass.md) | [AccessLevel](accesslevel.md) | [los moderadores](presenters.md)
  
### <a name="parent-elements"></a>Elementos principales

[CalendarItem](calendaritem.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

