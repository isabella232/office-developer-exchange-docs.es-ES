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
description: El elemento GetServerTimeZones es el elemento raíz en una solicitud para recuperar las definiciones de zona horaria desde el servidor de Exchange.
ms.openlocfilehash: 1ad503ff312497189f57bce9a3670571aedad5ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764978"
---
# <a name="getservertimezones"></a>GetServerTimeZones

El elemento **GetServerTimeZones** es el elemento raíz en una solicitud para recuperar las definiciones de zona horaria desde el servidor de Exchange. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Especifica si la [operación de GetServerTimeZones](getservertimezones-operation.md) devuelve la definición completa o sólo el nombre y el identificador de cada zona horaria. Este atributo es opcional. El valor predeterminado es **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>Atributo ReturnFullTimeZoneData

|**Valor**|**Descripción**|
|:-----|:-----|
|**True** <br/> |Devolver las definiciones de completadas para cada zona horaria.  <br/> |
|**False** <br/> |Devolver solo el nombre y el identificador de cada zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Identificadores de](ids.md) <br/> |Contiene una matriz de identificadores de definición de zona horaria que especifica las definiciones de zona horaria solicitado. Este elemento es opcional. Si este elemento no está incluido en la solicitud de la [operación de GetServerTimeZones](getservertimezones-operation.md) , se devuelven todas las definiciones de zona horaria que están disponibles en el servidor en la respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetServerTimeZones](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

