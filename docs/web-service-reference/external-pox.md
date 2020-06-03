---
title: Externa (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: El elemento external contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde fuera de la red de la organización.
ms.openlocfilehash: 45d7e72c5a43c5c468c1edd303a5e5ea8c2cb62e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457973"
---
# <a name="external-pox"></a>Externa (POX)

El elemento **external** contiene una colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde fuera de la red de la organización. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Externa (POX)](external-pox.md)
  
```XML
<External>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</External>

```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo concreto que ejecuta Microsoft Exchange Server que tiene instalada la función de servidor acceso de clientes que hospeda Outlook Web Access.  <br/> |
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes. Este elemento **Protocol** solo tiene dos elementos secundarios: un elemento [Type (POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX)](asurl-pox.md) , especificando el extremo de EWS para el servicio Web de disponibilidad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **external** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

