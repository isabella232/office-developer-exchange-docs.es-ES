---
title: EndTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndTimeZone
api_type:
- schema
ms.assetid: 6c53c337-be60-4d22-9e9e-a0c140c5e913
description: El elemento EndTimeZone define la zona horaria para la hora de finalización de un CalendarItem o MeetingRequest.
ms.openlocfilehash: 6d34afdedfb8e4886526317afea6abc324bde3c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520699"
---
# <a name="endtimezone"></a>EndTimeZone

El **elemento EndTimeZone** define la zona horaria para la hora de finalización de [un CalendarItem](calendaritem.md) o [MeetingRequest](meetingrequest.md).
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 **TimeZoneDefinitionType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Representa el identificador único de la definición de zona horaria.  <br/> |
|Nombre  <br/> |Representa el nombre descriptivo de la definición de zona horaria.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Periods](periods.md) <br/> |Representa una matriz de [elementos Period](period.md) que definen el desplazamiento de hora en distintas fases de la zona horaria.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Representa una matriz de [elementos TransitionsGroup](transitionsgroup.md) que especifican transiciones de zona horaria.  <br/> |
|[Transitions](transitions.md) <br/> |Representa una matriz de transiciones de zona horaria.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Representa un Exchange de calendario.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Representa una solicitud de reunión en Exchange almacén.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

