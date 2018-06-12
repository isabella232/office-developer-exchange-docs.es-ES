---
title: CalendarPermissionLevel
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarPermissionLevel
api_type:
- schema
ms.assetid: 6ac2b792-4326-4a3f-b6cb-977bf523b5b2
description: El elemento CalendarPermissionLevel representa el nivel de permisos que un usuario tiene en una carpeta de calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 646e4df3b70350a16cdd1f3e134260c2984a5161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763712"
---
# <a name="calendarpermissionlevel"></a>CalendarPermissionLevel

El elemento **CalendarPermissionLevel** representa el nivel de permisos que un usuario tiene en una carpeta de calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 **CalendarPermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que tiene un usuario a una carpeta de calendario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **CalendarPermissionLevel** . 
  
**Valores de texto de elemento CalendarPermissionLevel**

|**Valor**|**Descripción**|
|:-----|:-----|
|None  <br/> |Indica que el usuario no tiene permisos en la carpeta.  <br/> |
|Owner  <br/> |Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas. El usuario es el propietario de la carpeta y el contacto de la carpeta.  <br/> |
|PublishingEditor  <br/> |Indica que el usuario puede crear, leer, modificar y eliminar todos los elementos de la carpeta y crear subcarpetas.  <br/> |
|Editor  <br/> |Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta.  <br/> |
|PublishingAuthor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta, editar y eliminar sólo los elementos que crea el usuario y crear subcarpetas.  <br/> |
|Autor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta y editar y eliminar sólo los elementos que crea el usuario.  <br/> |
|NoneditingAuthor  <br/> |Indica que el usuario puede crear y leer todos los elementos en la carpeta y eliminar sólo los elementos que crea el usuario.  <br/> |
|Reviewer  <br/> |Indica que el usuario puede leer todos los elementos de la carpeta.  <br/> |
|Colaborador  <br/> |Indica que el usuario puede crear elementos en la carpeta. El contenido de la carpeta no aparecen.  <br/> |
|FreeBusyTimeOnly  <br/> |Indica que el usuario puede ver solo las horas de disponibilidad del calendario.  <br/> |
|FreeBusyTimeAndSubjectAndLocation  <br/> |Indica que el usuario puede ver el tiempo libre/ocupada en el calendario y el asunto y la ubicación de las citas.  <br/> |
|Personalizado  <br/> |Indica que el usuario tiene permisos de acceso personalizados en la carpeta.  <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Establecimiento de permisos de nivel de carpeta](http://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

