---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: El elemento GroupingInformation contiene un valor que se usa para agrupar el buzón del usuario con el fin de mantener la afinidad al suscribirse a las notificaciones en varios buzones.
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530081"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

El elemento **GroupingInformation** contiene un valor que se usa para agrupar el buzón del usuario con el fin de [mantener la afinidad](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) al suscribirse a las notificaciones en varios buzones. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al servidor de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto se compara con el valor del elemento **GroupingInformation** para otros buzones de correo. Los buzones que tienen el mismo valor y usan el mismo punto de conexión de servicios web Exchange (EWS) se pueden agrupar para mantener la afinidad. Para obtener más información, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).
  
## <a name="remarks"></a>Comentarios

El elemento **GroupingInformation** solo se aplica a los elementos de **Protocolo** que tienen un elemento secundario [tipo (POX)](type-pox.md) con un valor de "expr". 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de correo de Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

