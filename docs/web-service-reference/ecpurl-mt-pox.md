---
title: EcpUrl-mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: El elemento EcpUrl mt especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de seguimiento de mensajes de correo electrónico.
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764292"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-mt (POX)

El elemento **EcpUrl mt** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración de un usuario habilitado para correo de seguimiento de mensajes de correo electrónico. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
[Protocolo (POX)](protocol-pox.md)
  
[EcpUrl-mt (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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
|[Protocolo (POX)](protocol-pox.md) <br/> |Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para tener acceso a la configuración para el usuario de seguimiento de correo electrónico. El valor del elemento **EcpUrl mt** contiene parámetros contenidos en ' <' y ' >' caracteres que se sustituyen por el cliente, como se muestra en la siguiente tabla. 
  
|**Parámetro**|**Sustituir con**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _ID mensaje_ <br/> |Identificador de mensaje de Internet del mensaje para su seguimiento según se especifica en el encabezado de identificador de mensaje.  <br/> |
| _Buzones_ <br/> |La dirección SMTP del propietario del buzón.  <br/> |
| _Sender_ <br/> |La dirección SMTP del remitente del mensaje.  <br/> |
   
## <a name="remarks"></a>Comentarios

El elemento **EcpUrl mt** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también



[Elementos de Autodiscover XML POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

