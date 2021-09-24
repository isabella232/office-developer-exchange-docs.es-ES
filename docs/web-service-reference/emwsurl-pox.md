---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: El elemento EmwsUrl especifica la dirección URL de la mejor instancia de extremo para Exchange Web Services (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: d46438f600e226bce95c5e479aca91bfa942535e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538178"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

El **elemento EmwsUrl** especifica la dirección URL de la mejor instancia de extremo para Exchange Web Services (EWS) para un usuario habilitado para correo. 
  
- [AutoDiscover (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md) 
- [Account (POX)](account-pox.md) 
- [Protocol (POX)](protocol-pox.md) 
- [EmwsUrl (POX)](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
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

El valor de texto representa la dirección URL del extremo EWS para el usuario. Es equivalente al elemento [EwsUrl (POX).](ewsurl-pox.md) 
  
## <a name="remarks"></a>Comentarios

El **elemento EmwsUrl** es un elemento secundario opcional del **elemento Protocol.** 
  
## <a name="see-also"></a>Ver también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

