---
title: ReadItems (CalendarPermissionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReadItems
api_type:
- schema
ms.assetid: bec01982-26a1-4373-b1e6-2e0c838d83c4
description: El elemento ReadItems indica si un usuario tiene permiso para leer elementos dentro de una carpeta Calendar. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1).
ms.openlocfilehash: a12b5316eaebfdf6d0d70468f172f227db7ab3ef
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519089"
---
# <a name="readitems-calendarpermissiontype"></a>ReadItems (CalendarPermissionType)

El **elemento ReadItems** indica si un usuario tiene permiso para leer elementos dentro de una carpeta Calendar. Este elemento se introdujo en Microsoft Exchange Server 2007 Service Pack 1 (SP1). 
  
```xml
<ReadItems>None or TimeOnly or TimeAndSubjectAndLocation or FullDetails</ReadItems>
```

 **CalendarPermissionReadAccessType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[CalendarPermission](calendarpermission.md) <br/> |Define el acceso que un usuario tiene a una carpeta Calendar. Este elemento se introdujo en Exchange 2007 SP1.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento ReadItems.** 
  
**Valores de texto del elemento ReadItems**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Indica que el usuario no tiene permiso para ver elementos en el calendario.  <br/> |
|TimeOnly  <br/> |Indica que el usuario tiene permiso para ver solo el tiempo de disponibilidad en el calendario.  <br/> |
|TimeAndSubjectAndLocation  <br/> |Indica que el usuario tiene permiso para ver el tiempo de disponibilidad en el calendario y el asunto y la ubicación de las citas.  <br/> |
|FullDetails  <br/> |Indica que el usuario tiene permiso para ver todos los elementos del calendario, incluidos el tiempo de disponibilidad y el asunto, la ubicación y los detalles de las citas.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)


[Configuración Folder-Level permisos](https://msdn.microsoft.com/library/c7530e86-5112-401c-b10a-9c054ae59f07%28Office.15%29.aspx)

