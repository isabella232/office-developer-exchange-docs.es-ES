---
title: EcpUrl-MT (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: El elemento EcpUrl-MT especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico para un usuario habilitado para correo.
ms.openlocfilehash: 097811add5635bca14c659814652bca244a1398d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458715"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-MT (POX)

El elemento **EcpUrl-MT** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración de seguimiento de mensajes de correo electrónico para un usuario habilitado para correo. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[EcpUrl-MT (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para obtener acceso a la configuración del seguimiento de correo electrónico del usuario. El valor del elemento **EcpUrl-MT** contiene los parámetros contenidos dentro de los caracteres ' < ' y ' > ' que el cliente sustituye, tal como se muestra en la siguiente tabla. 
  
|**Parámetro**|**Sustituto con**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _MsgID_ <br/> |Identificador del mensaje de Internet del mensaje que se va a realizar un seguimiento según lo especificado por el encabezado del identificador de mensaje.  <br/> |
| _MBX_ <br/> |La dirección SMTP del propietario del buzón.  <br/> |
| _Sender_ <br/> |La dirección SMTP del remitente del mensaje.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **EcpUrl-MT** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

