---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: El elemento RetentionPolicyType especifica el tipo de directiva de retención aplicado a los elementos de una conversación.
ms.openlocfilehash: 961f72c35443e9f265e9313166fa77c8cd93d654
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509388"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

El **elemento RetentionPolicyType** especifica el tipo de directiva de retención aplicado a los elementos de una conversación. 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 **RetentionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ConversationAction](conversationaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del **elemento RetentionPolicyType** es el tipo de retención aplicado a los elementos de una conversación. El valor de texto **de Delete** indica que los elementos de la conversación se eliminan cuando expira la retención. El valor de texto de **Archive** indica que los elementos de la conversación se mueven al buzón de archivo cuando expira la retención. 
  
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
   

