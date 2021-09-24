---
title: MailboxStatisticsSearchResult
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 73499df7-3d50-4e39-895d-6e15dd8b2777
description: El elemento MailboxStatisticsSearchResult contiene los resultados de una búsqueda de palabras clave.
ms.openlocfilehash: f73a789d0931e9c15d052444f6a191ae70cbff24
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511125"
---
# <a name="mailboxstatisticssearchresult"></a>MailboxStatisticsSearchResult

El **elemento MailboxStatisticsSearchResult** contiene los resultados de una búsqueda de palabras clave. 
  
```XML
<MailboxStatisticsSearchResult>
   <UserMailbox/>
   <KeywordStatisticsSearchResult/>
</MailboxStatisticsSearchResult>
```

**MailboxStatisticsSearchResultType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

[UserMailbox](usermailbox.md)  |  [KeywordStatisticsSearchResult](keywordstatisticssearchresult.md)
  
### <a name="parent-elements"></a>Elementos principales

[FindMailboxStatisticsByKeywordsResponseMessage](findmailboxstatisticsbykeywordsresponsemessage.md)
  
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre del esquema  <br/> |esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

