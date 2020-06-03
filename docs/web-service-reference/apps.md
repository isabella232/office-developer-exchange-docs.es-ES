---
title: Aplicaciones
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f6f0a2ca-22dd-4789-9eed-f0c1ec9036c4
description: El elemento apps contiene información sobre todos los archivos de manifiesto XML para las aplicaciones instaladas en un buzón.
ms.openlocfilehash: b2d6f13241f68cbed449a9f9821f9a6ec6ff687a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527449"
---
# <a name="apps"></a>Aplicaciones

El elemento **apps** contiene información sobre todos los archivos de manifiesto XML para las aplicaciones instaladas en un buzón. 
  
```XML
<Apps>
    <App/>
</Apps>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
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
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |No aplicable  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [App](app.md)
- [GetAppManifestsResponse](getappmanifestsresponse.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

