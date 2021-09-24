---
title: EcpUrl-um (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 455c77c6-c03f-49a7-a8ca-aa0023b6e73b
description: El elemento EcpUrl-um especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de correo de voz de un usuario habilitado para correo.
ms.openlocfilehash: 33037765750581f20bd993254fed83e202e538a9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528655"
---
# <a name="ecpurl-um-pox"></a>EcpUrl-um (POX)

El **elemento EcpUrl-um** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de correo de voz de un usuario habilitado para correo. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-um (POX)](ecpurl-um-pox.md)
  
```XML
<EcpUrl-um/>
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
|[Protocol (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración del correo de voz del usuario. 
  
## <a name="remarks"></a>Comentarios

El **elemento EcpUrl-um** es un elemento secundario opcional del **elemento Protocol.** 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

