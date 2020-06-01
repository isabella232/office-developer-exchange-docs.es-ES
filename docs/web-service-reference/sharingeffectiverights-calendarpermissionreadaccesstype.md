---
title: SharingEffectiveRights (CalendarPermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: b519f642-a9ef-4300-92e6-ed8202855fde
description: El elemento SharingEffectiveRights indica los permisos que tiene el usuario para los datos de calendario que se están compartiendo.
ms.openlocfilehash: 5581e9cc001608a124ae94e69eba836f6fd98520
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458582"
---
# <a name="sharingeffectiverights-calendarpermissionreadaccesstype"></a>SharingEffectiveRights (CalendarPermissionReadAccessType)

El elemento **SharingEffectiveRights** indica los permisos que tiene el usuario para los datos de calendario que se están compartiendo. 
  
```XML
<SharingEffectiveRights>None | TimeOnly | TimeAndSubjectAndLocation | FullDetails</SharingEffectiveRights>
```

 **CalendarPermissionReadAccessType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Hubiera](calendarfolder.md) <br/> |Representa una carpeta que contiene principalmente elementos de calendario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **SharingEffectiveRights** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Indica que el usuario no tiene permiso para ver los elementos del calendario.  <br/> |
|TimeOnly  <br/> |Indica que el usuario tiene permiso para ver solo la hora de disponibilidad en el calendario.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Indica que el usuario tiene permiso para ver la fecha de disponibilidad en el calendario y el asunto y la ubicación de las citas.  <br/> |
|FullDetails  <br/> |Indica que el usuario tiene permiso para ver todos los elementos del calendario, incluidos el asunto, la ubicación y la fecha de disponibilidad de las citas.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

