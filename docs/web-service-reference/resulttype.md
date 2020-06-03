---
title: ResultType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 488ee828-343f-4382-a5e8-eed1005f5dbc
description: El elemento ResultType contiene el tipo de búsqueda que se va a realizar. El tipo de búsqueda solo puede ser estadística o solo vista previa.
ms.openlocfilehash: 6617c8b4b64cd9b6728317d7247bcc5378e488f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465285"
---
# <a name="resulttype"></a>ResultType

El elemento **ResultType** contiene el tipo de búsqueda que se va a realizar. El tipo de búsqueda solo puede ser estadística o solo vista previa. 
  
```XML
<ResultType>StatisticsOnly | PreviewOnly</ResultType>
```

 **SearchResultType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

[SearchMailboxesResult](searchmailboxesresult.md)  |  [SearchMailboxes](searchmailboxes.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **ResultType** es el tipo de resultado que se devuelve para una búsqueda de detección. Un valor de texto de **StatisticsOnly** devolverá las estadísticas de búsqueda. Un valor de texto de **PreviewOnly** devolverá información de la vista previa del elemento. 
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |false  <br/> |
   

