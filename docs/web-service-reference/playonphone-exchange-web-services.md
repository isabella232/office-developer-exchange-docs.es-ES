---
title: PlayOnPhone (servicios Web de Exchange)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 486612be-470c-4f99-929a-f2b283e055c1
description: El elemento PlayOnPhone representa una solicitud para leer un elemento en un teléfono.
ms.openlocfilehash: 75493a31940ea609fd6cf454e91ca5881fb7e678
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836816"
---
# <a name="playonphone-exchange-web-services"></a>PlayOnPhone (servicios Web de Exchange)

El elemento **PlayOnPhone** representa una solicitud para leer un elemento en un teléfono. 
  
```xml
<PlayOnPhone>   <ItemId/>   <DialString/></PlayOnPhone>
```

 **PlayOnPhoneType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Representa el identificador de un elemento que se reproducirán en un teléfono. Se requiere este elemento.  <br/> |
|[DialString (servicios Web de Exchange)](dialstring-exchange-web-services.md) <br/> |Representa la cadena de marcado del número de teléfono que se llama para reproducir un elemento por teléfono. Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2010 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

