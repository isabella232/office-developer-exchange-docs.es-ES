---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: El elemento GroupingInformation contiene un valor que se usa para agrupar el buzón del usuario para mantener la afinidad al suscribirse a las notificaciones a través de varios buzones de correo.
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835781"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

El elemento **GroupingInformation** contiene un valor que se usa para el buzón del usuario para [mantener la afinidad](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) de grupo al suscribirse a las notificaciones a través de varios buzones de correo. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente con el servidor de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto se compara con el valor del elemento **GroupingInformation** para otros buzones de correo. Los buzones que tienen el mismo valor y usar el mismo extremo de servicios Web de Exchange (EWS) se pueden agrupar para mantener la afinidad. Para obtener más detalles, vea [mantener la afinidad entre un grupo de suscripciones y el servidor de buzones en Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).
  
## <a name="remarks"></a>Comentarios

El elemento **GroupingInformation** sólo es aplicable a los elementos de **protocolo** que tienen un elemento secundario de [Tipo (POX)](type-pox.md) con un valor de "EXPR". 
  
## <a name="see-also"></a>Vea también

- [Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Mantener la afinidad entre un grupo de suscripciones y el servidor de buzones de Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

