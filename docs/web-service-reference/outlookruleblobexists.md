---
title: OutlookRuleBlobExists
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutlookRuleBlobExists
api_type:
- schema
ms.assetid: ae1bc448-deb9-4b5b-ab38-4b276abcb650
description: El elemento OutlookRuleBlobExists indica si existe un BLOB de regla de Microsoft Outlook en el buzón de correo del usuario.
ms.openlocfilehash: 6a5c2a2ec0246d38b22279b86772972ea81922c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529031"
---
# <a name="outlookruleblobexists"></a>OutlookRuleBlobExists

El elemento **OutlookRuleBlobExists** indica si existe un BLOB de regla de Microsoft Outlook en el buzón de correo del usuario. 
  
[GetInboxRulesResponse](getinboxrulesresponse.md)
  
[OutlookRuleBlobExists](outlookruleblobexists.md)
  
```XML
<OutlookRuleBlobExists>true | false</OutlookRuleBlobExists>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetInboxRulesResponse](getinboxrulesresponse.md) <br/> |Representa una respuesta a una solicitud de [operación GetInboxRules](getinboxrules-operation.md) .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Un valor de texto de **true** indica que existe un BLOB de regla de Outlook. Un valor de texto de **false** indica que no existe un BLOB de regla de Outlook. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

