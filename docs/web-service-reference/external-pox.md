---
title: Externo (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8eed1f79-6eb3-4a88-80fb-d4edf9f34fda
description: El elemento externo contiene una colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde fuera de la red de la organización.
ms.openlocfilehash: 7f01fc29b5ce63b02de0a4a6e42887dcffbb4b82
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764532"
---
# <a name="external-pox"></a>Externo (POX)

El elemento **externo** contiene una colección de direcciones URL que puede utilizar un cliente para conectarse a Exchange desde fuera de la red de la organización. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[Externo (POX)](external-pox.md)
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[OWAUrl (POX)](owaurl-pox.md) <br/> |Describe la dirección URL y el esquema de autenticación que se usa para tener acceso a un determinado equipo que ejecuta a Microsoft Exchange Server que tiene el rol de servidor de acceso de cliente instalado que aloja Outlook Web Access.  <br/> |
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente. Este elemento de **protocolo** tiene sólo dos elementos secundarios: un elemento de [Tipo (POX)](type-pox.md) que especifica el protocolo de conexión y un elemento [ASUrl (POX)](asurl-pox.md) , que especifica el extremo EWS para el servicio web de disponibilidad.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.  <br/> |
   
## <a name="remarks"></a>Notas

El elemento **externo** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Ver también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

