---
title: SearchQueries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67328dab-321b-45ad-929e-cd83e65ad87e
description: El elemento SearchQueries contiene una lista de buzones y consultas asociadas para la búsqueda de detección.
ms.openlocfilehash: 66015d71238b4a1055a71aff539ca50150f2a247
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466916"
---
# <a name="searchqueries"></a>SearchQueries

El elemento **SearchQueries** contiene una lista de buzones y consultas asociadas para la búsqueda de detección. 
  
```XML
<SearchQueries>
   <MailboxQuery/>
</SearchQueries>
```

 ****
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

[MailboxQuery](mailboxquery.md)
  
### <a name="parent-elements"></a>Elementos principales

[SearchMailboxes](searchmailboxes.md)  |  [SearchMailboxesResult](searchmailboxesresult.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   

