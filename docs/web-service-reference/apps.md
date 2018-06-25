---
title: Aplicaciones
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6f0a2ca-22dd-4789-9eed-f0c1ec9036c4
description: El elemento de aplicaciones contiene información acerca de todos los archivos de manifiesto de XML para las aplicaciones que se instalan en un buzón de correo.
ms.openlocfilehash: 81b0cb76b02fcc9145f6d70eff12a0a0ac0ad51f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763542"
---
# <a name="apps"></a>Aplicaciones

El elemento de **aplicaciones** contiene información acerca de todos los archivos de manifiesto de XML para las aplicaciones que se instalan en un buzón de correo. 
  
```XML
<Apps>
    <App/>
</Apps>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[App](app.md)
  
### <a name="parent-elements"></a>Elementos principales

[GetAppManifestsResponse](getappmanifestsresponse.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |No disponible  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también

- [App](app.md)
- [GetAppManifestsResponse](getappmanifestsresponse.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

