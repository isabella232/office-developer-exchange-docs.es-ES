---
title: MailboxQuery
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e4b496f7-63fa-479a-b045-73276573f64f
description: El elemento MailboxQuery especifica una consulta y el ámbito de una búsqueda de detección.
ms.openlocfilehash: 9ab2d44822012a264fe136f0c170c91ad5b62f22
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519341"
---
# <a name="mailboxquery"></a>MailboxQuery

El **elemento MailboxQuery** especifica una consulta y el ámbito de una búsqueda de detección. 
  
```XML
<MailboxQuery>
   <Query/>
   <MailboxSearchScopes/>
</MailboxQuery>
```

**MailboxQueryType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[Consulta](query.md)  |  [MailboxSearchScopes](mailboxsearchscopes.md)
  
### <a name="parent-elements"></a>Elementos principales

[SearchQueries](searchqueries.md)
  
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
   

