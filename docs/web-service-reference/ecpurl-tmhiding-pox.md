---
title: EcpUrl-tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: El elemento EcpUrl-tmHiding especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio.
ms.openlocfilehash: 68b949db8b8d98caddbac3b9f96c5d5e55b104b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463534"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl-tmHiding (POX)

El elemento **EcpUrl-tmHiding** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para cancelar la suscripción del usuario a un buzón del sitio. El valor del elemento **EcpUrl-tmHiding** contiene los parámetros contenidos dentro de los caracteres ' < ' y ' > ' que el cliente sustituye, tal como se muestra en la siguiente tabla. 
  
|**Parámetro**|**Sustituto con**|
|:-----|:-----|
| _Id_ <br/> |La dirección de correo electrónico SMTP o el nombre distintivo X500 del buzón del sitio.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **EcpUrl-tmHiding** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

