---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: El elemento EmwsUrl especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo.
ms.openlocfilehash: 19e1078ae8d08513e85d75d87e960a910986f727
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530673"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

El elemento **EmwsUrl** especifica la dirección URL de la mejor instancia de punto de conexión para los servicios web Exchange (EWS) para un usuario habilitado para correo. 
  
- [Detección automática (POX)](autodiscover-pox.md) 
- [Respuesta (POX)](response-pox.md) 
- [Cuenta (POX)](account-pox.md) 
- [Protocolo (POX)](protocol-pox.md) 
- [EmwsUrl (POX)](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
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

El valor de texto representa la dirección URL del extremo de EWS para el usuario. Es equivalente al elemento [EwsUrl (POX)](ewsurl-pox.md) . 
  
## <a name="remarks"></a>Comentarios

El elemento **EmwsUrl** es un elemento secundario opcional del elemento **Protocol** . 
  
## <a name="see-also"></a>Vea también

- [Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

