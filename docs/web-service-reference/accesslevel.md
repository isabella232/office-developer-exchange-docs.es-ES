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
ms.openlocfilehash: 3c1375ef37ea666c6c4fafce7daa46ae0d0a2696
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462342"
---
# <a name="accesslevel"></a>AccessLevel

El elemento **AccessLevel** especifica el nivel de acceso para una reunión en línea. 
  
```XML
<AccessLevel/>
```

 **OnlineMeetingSettingsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OnlineMeetingSettings](onlinemeetingsettings.md) <br/> |Especifica la configuración de las reuniones en línea.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores de texto para el elemento **AccessLevel** . 
  
**Valores de texto del elemento AccessLevel**

|**Valor**|**Descripción**|
|:-----|:-----|
|Todos  <br/> |El nivel de acceso está abierto a todos.  <br/> |
|Interno  <br/> |El nivel de acceso es solo interno.  <br/> |
|Invitado  <br/> |El nivel de acceso solo es participante invitado.  <br/> |
|Bloqueado  <br/> |El nivel de acceso está bloqueado.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
Este elemento se introdujo en Exchange Server 2013.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

