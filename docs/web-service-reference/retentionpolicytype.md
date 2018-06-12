---
title: RetentionPolicyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: abce5b3e-971d-42fc-aeea-caa7202214de
description: El elemento RetentionPolicyType especifica el tipo de directiva de retención aplicado a los elementos en una conversación.
ms.openlocfilehash: dacb3fa75611cbd6e6e29eab7c791dfd8964c9ec
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837229"
---
# <a name="retentionpolicytype"></a>RetentionPolicyType

El elemento **RetentionPolicyType** especifica el tipo de directiva de retención aplicado a los elementos en una conversación. 
  
```XML
<RetentionPolicyType> Delete | Archive </RetentionPolicyType>
```

 **RetentionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

[ConversationAction](conversationaction.md)
  
## <a name="text-value"></a>Valor de texto

El valor de texto del elemento **RetentionPolicyType** es el tipo de retención aplicado a los elementos en una conversación. El valor de texto de **Eliminar** indica que los elementos de la conversación se eliminan cuando expire la suspensión de retención. El valor de texto del **archivo** indica que los elementos de la conversación se mueven al buzón de archivo cuando expire la suspensión de retención. 
  
## <a name="remarks"></a>Notas

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   

