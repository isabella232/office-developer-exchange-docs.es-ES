---
title: Internal (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 69c22546-ebd6-4a03-b0b4-bbac72ec5551
description: El elemento Internal contiene la colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde dentro de la red de la organización.
ms.openlocfilehash: f87c5e21eff87965c9b6ff6f3d59e2b3a37b87f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541122"
---
# <a name="internal-pox"></a>Internal (POX)

El **elemento Internal** contiene la colección de direcciones URL que un cliente puede usar para conectarse a Exchange desde dentro de la red de la organización. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[Internal (POX)](internal-pox.md)
  
```xml
<Internal>
   <OWAUrl/>
   <Protocol>
      <Type/>
      <ASUrl/>
   </Protocol>
</Internal>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Describe la dirección URL y el esquema de autenticación que se usa para obtener acceso a un equipo determinado que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente que hospeda Outlook Web Access.  <br/> |
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente. Este **elemento Protocol** solo tiene dos elementos secundarios: un elemento Type [(POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX),](asurl-pox.md) que especifica el extremo EWS para el servicio web de disponibilidad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento Internal** es un elemento secundario opcional del elemento **Protocol.** 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

