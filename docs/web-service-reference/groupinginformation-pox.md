---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: El elemento GroupingInformation contiene un valor que se usa para agrupar el buzón del usuario para mantener la afinidad al suscribirse a notificaciones en varios buzones.
ms.openlocfilehash: 14e751adcd0b966907ce495a2753b2b26d812a86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525887"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

El **elemento GroupingInformation** contiene un valor que se usa [](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) para agrupar el buzón del usuario para mantener la afinidad al suscribirse a notificaciones en varios buzones. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al Exchange servidor.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto se compara con el valor del **elemento GroupingInformation** para otros buzones. Los buzones que tienen el mismo valor y usan el mismo punto de conexión de Exchange Web Services (EWS) se pueden agrupar para mantener la afinidad. Para obtener más información, vea [Maintain affinity between a group of subscriptions and the Mailbox server in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).
  
## <a name="remarks"></a>Comentarios

El **elemento GroupingInformation** solo se aplica a los **elementos Protocol** que tienen un elemento secundario Type [(POX)](type-pox.md) con un valor de "EXPR". 
  
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Mantener la afinidad entre un grupo de suscripciones y el servidor del buzón de Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

