---
title: GetServerTimeZones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetServerTimeZones
api_type:
- schema
ms.assetid: 2a89098b-d89b-4d01-827b-50be00f7cbe9
description: El elemento GetServerTimeZones es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del Exchange servidor.
ms.openlocfilehash: b710334e5778f8bc27ba7ac07c6bf9c2e2d3392e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533542"
---
# <a name="getservertimezones"></a>GetServerTimeZones

El **elemento GetServerTimeZones** es el elemento raíz de una solicitud para recuperar definiciones de zona horaria del Exchange servidor. 
  
```xml
<GetServerTimeZones ReturnFullTimeZoneData="">   <Ids/></GetServerTimeZones>
```

 **GetServerTimeZonesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**ReturnFullTimeZoneData** <br/> |Especifica si la operación [GetServerTimeZones](getservertimezones-operation.md) devuelve la definición completa o solo el nombre y el identificador de cada zona horaria. Este atributo es opcional. El valor predeterminado es **true**.  <br/> |
   
#### <a name="returnfulltimezonedata-attribute"></a>Atributo ReturnFullTimeZoneData

|**Valor**|**Descripción**|
|:-----|:-----|
|**true** <br/> |Devuelve las definiciones completas de cada zona horaria.  <br/> |
|**false** <br/> |Devuelve solo el nombre y el identificador de cada zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Ids](ids.md) <br/> |Contiene una matriz de identificadores de definición de zona horaria que especifica las definiciones de zona horaria solicitadas. Este elemento es opcional. Si este elemento no se incluye en la solicitud de operación [GetServerTimeZones,](getservertimezones-operation.md) todas las definiciones de zona horaria disponibles en el servidor se devuelven en la respuesta.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetServerTimeZones](getservertimezones-operation.md)
  
[GetServerTimeZonesResponse](getservertimezonesresponse.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

