---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: El elemento GetServerTimeZones es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del servidor de Exchange.
ms.openlocfilehash: 797e4543c94b0628242bcf544fe9a735ebaa5a63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460942"
---
# <a name="getservertimezones"></a>GetServerTimeZones

El elemento **GetServerTimeZones** es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del servidor de Exchange. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Especifica si la [operación GetServerTimeZones](getservertimezones-operation.md) devuelve la definición completa o solo el nombre y el identificador de cada zona horaria. Este atributo es opcional. El valor predeterminado es **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>Atributo ReturnFullTimeZoneData

|**Valor**|**Descripción**|
|:-----|:-----|
|**true** <br/> |Devuelve las definiciones completas para cada zona horaria.  <br/> |
|**false** <br/> |Devolver solo el nombre y el identificador de cada zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Falta](ids.md) <br/> |Contiene una matriz de identificadores de definición de zona horaria que especifica las definiciones de zona horaria solicitada. Este elemento es opcional. Si este elemento no se incluye en la solicitud de [operación GetServerTimeZones](getservertimezones-operation.md) , todas las definiciones de zona horaria que estén disponibles en el servidor se devolverán en la respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetServerTimeZones](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

