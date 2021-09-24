---
title: EcpUrl-mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: El elemento EcpUrl-mt especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico de un usuario habilitado para correo.
ms.openlocfilehash: bb0a60f3b3a2d65421164e40537e7514df20e357
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520818"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-mt (POX)

El **elemento EcpUrl-mt** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico de un usuario habilitado para correo. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-mt (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de correo electrónico del usuario. El valor del elemento **EcpUrl-mt** contiene parámetros contenidos en los caracteres "<" y ">" que el cliente sustituye como se muestra en la tabla siguiente. 
  
|**Parámetro**|**Sustituir por**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _MsgID_ <br/> |Identificador de mensaje de Internet del mensaje que se va a realizar un seguimiento según lo especificado por el encabezado Message-ID.  <br/> |
| _Mbx_ <br/> |La dirección SMTP del propietario del buzón.  <br/> |
| _Sender_ <br/> |La dirección SMTP del remitente del mensaje.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento EcpUrl-mt** es un elemento secundario opcional del **elemento Protocol.** 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

