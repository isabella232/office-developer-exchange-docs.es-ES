---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: El elemento OutlookRuleBlobExists indica si existe un blob de regla de microsoft Outlook en el buzón del usuario.
ms.openlocfilehash: ff8ac5d6ad30578dbbf18787409f3d19469cf6b7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521720"
---
# <a name="outlookruleblobexists"></a>OutlookRuleBlobExists

El **elemento OutlookRuleBlobExists** indica si existe un blob de regla de microsoft Outlook en el buzón del usuario. 
  
[GetInboxRulesResponse](getinboxrulesresponse.md)
  
[OutlookRuleBlobExists](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Representa una respuesta a una [solicitud de operación GetInboxRules.](getinboxrules-operation.md)  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto **de true** indica que existe Outlook blob de regla. Un valor de texto **de false** indica que no existe Outlook blob de regla. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

