---
title: Error (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 91c63b62-ab68-4c32-a2f7-5a87c188335b
description: El elemento error contiene una respuesta de error de detección automática.
ms.openlocfilehash: 1a1a3e83898674e605921cb75371036a8a561a95
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530652"
---
# <a name="error-pox"></a>Error (POX)

El elemento **error** contiene una respuesta de error de detección automática. 
  
[Detección automática (POX)](autodiscover-pox.md)
  
[Respuesta (POX)](response-pox.md)
  
[Cuenta (POX)](account-pox.md)
  
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
|Id  <br/> |Representa un hash del nombre del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ErrorCode (POX)](errorcode-pox.md) <br/> |Contiene el código de error para una respuesta de detección automática de errores.  <br/> |
|[Mensaje (POX)](message-pox.md) <br/> |Contiene el mensaje de error de una respuesta de detección automática de errores.  <br/> |
|[DebugData (POX)](debugdata-pox.md) <br/> |Contiene los datos de depuración para una respuesta de detección automática de errores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Cuenta (POX)](account-pox.md) <br/> |Contiene una respuesta de error de detección automática.  <br/> |
   
## <a name="see-also"></a>Vea también



[Elementos XML de detección automática de POX para Exchange](pox-autodiscover-xml-elements-for-exchange.md)

