---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: El elemento EcpUrl-tmEditing especifica una dirección URL parcial que se puede combinar con el valor del elemento EcpUrl (POX) para generar una dirección URL que se puede usar para editar un buzón de sitio existente.
ms.openlocfilehash: e615e8ae09c3a9422f753a71070917a41f40741b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531095"
---
# <a name="ecpurl-tmediting-pox"></a>EcpUrl-tmEditing (POX)

El **elemento EcpUrl-tmEditing** especifica una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Protocol (POX)](protocol-pox.md)
  
[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
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

El valor de texto representa una dirección URL parcial que se puede combinar con el valor del elemento [EcpUrl (POX)](ecpurl-pox.md) para generar una dirección URL que se puede usar para editar un buzón de sitio existente. El valor del elemento **EcpUrl-tmEditing** contiene parámetros contenidos en los caracteres "<" y ">" que el cliente sustituye como se muestra en la tabla siguiente. 
  
|**Parámetro**|**Sustituir por**|
|:-----|:-----|
| _Id_ <br/> |La dirección de correo electrónico SMTP o el nombre distintivo X500 del buzón del sitio.  <br/> |
   
## <a name="remarks"></a>Comentarios

El **elemento EcpUrl-tmEditing** es un elemento secundario opcional del **elemento Protocol.** 
  
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

