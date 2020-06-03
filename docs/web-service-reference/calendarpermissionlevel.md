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
description: El elemento CalendarPermissionLevel representa el nivel de permisos que tiene un usuario en una carpeta calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: 670f78e0b3cef7a40339c83d84916871f8969536
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527183"
---
# <a name="calendarpermissionlevel"></a>CalendarPermissionLevel

El elemento **CalendarPermissionLevel** representa el nivel de permisos que tiene un usuario en una carpeta calendario. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<CalendarPermissionLevel>None or Owner or PublishingEditor or Editor or PublishingAuthor or Author or NoneditingAuthor or Reviewer or Contributor or FreeBusyTimeOnly or FreeBusyTimeAndSubjectAndLocation or Custom</CalendarPermissionLevel>
```

 **CalendarPermissionLevelType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que tiene un usuario a una carpeta de calendario. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **CalendarPermissionLevel** . 
  
**Valores de texto del elemento CalendarPermissionLevel**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Indica que el usuario no tiene permisos para la carpeta.  <br/> |
|Owner  <br/> |Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta, así como crear subcarpetas. El usuario es el propietario de la carpeta y el contacto de la carpeta.  <br/> |
|Publishingeditorcreateitems  <br/> |Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta, así como crear subcarpetas.  <br/> |
|Editor  <br/> |Indica que el usuario puede crear, leer, editar y eliminar todos los elementos de la carpeta.  <br/> |
|Publishingauthorcreateitems  <br/> |Indica que el usuario puede crear y leer todos los elementos de la carpeta, editar y eliminar sólo los elementos que crea el usuario y crear subcarpetas.  <br/> |
|Autor  <br/> |Indica que el usuario puede crear y leer todos los elementos de la carpeta, y editar y eliminar sólo los elementos creados por el usuario.  <br/> |
|Noneditingauthorcreateitems  <br/> |Indica que el usuario puede crear y leer todos los elementos de la carpeta, y eliminar sólo los elementos que crea el usuario.  <br/> |
|Reviewer  <br/> |Indica que el usuario puede leer todos los elementos de la carpeta.  <br/> |
|Colaborador  <br/> |Indica que el usuario puede crear elementos en la carpeta. El contenido de la carpeta no aparece.  <br/> |
|FreeBusyTimeOnly  <br/> |Indica que el usuario puede ver solo la hora de disponibilidad en el calendario.  <br/> |
|FreeBusyTimeAndSubjectAndLocation  <br/> |Indica que el usuario puede ver la fecha de disponibilidad en el calendario y el asunto y la ubicación de las citas.  <br/> |
|Personalizado  <br/> |Indica que el usuario tiene permisos de acceso personalizados en la carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)


[Configuración de permisos de nivel de carpeta](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

