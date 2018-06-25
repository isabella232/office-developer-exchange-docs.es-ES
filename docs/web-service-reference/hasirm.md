---
title: HasIrm
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fedc04e0-cfd2-4652-a2a8-51de859ae847
description: El elemento HasIrm especifica si al menos un mensaje en la conversación y la carpeta actual es un mensaje protegido de IRM.
ms.openlocfilehash: c129370d7920da7cf1f9f32eed2f075e6c21cf8b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835803"
---
# <a name="hasirm"></a>HasIrm

El elemento **HasIrm** especifica si al menos un mensaje en la conversación y la carpeta actual es un mensaje protegido de IRM. 
  
```XML
<HasIrm> true | false </HasIrm>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[Conversación (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **HasIrm** es **true** si al menos un mensaje en la conversación y la carpeta actual tiene IRM. De lo contrario, el valor es **false**.
  
## <a name="remarks"></a>Comentarios

Este elemento se incorporó en Exchange Server 2013 Service Pack 1 (SP1).
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



[Conversación (ConversationType)](conversation-conversationtype.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

