---
title: Error (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: El elemento Error contiene una respuesta de error de detección automática.
ms.openlocfilehash: 2f96f8b9d6d154aac6f10924095b5a5864e76750
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530892"
---
# <a name="error-pox"></a>Error (POX)

El **elemento Error** contiene una respuesta de error de detección automática. 
  
[AutoDiscover (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Account (POX)](account-pox.md)
  
[Error (POX)](error-pox.md)
  
```xml
<Error Time="" Id="">
   <ErrorCode/>
   <Message/>
   <DebugData/>
</Error>
```

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Hora  <br/> |Representa la hora en que se devolvió la respuesta de error.  <br/> |
|Id  <br/> |Representa un hash del nombre del equipo que se ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Contiene el código de error de una respuesta de detección automática de errores.  <br/> |
|[Message (POX)](message-pox.md) <br/> |Contiene el mensaje de error de una respuesta de detección automática de errores.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Contiene los datos de depuración de una respuesta de detección automática de errores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Account (POX)](account-pox.md) <br/> |Contiene una respuesta de error de detección automática.  <br/> |
   
## <a name="see-also"></a>Ver también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

