---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: El elemento FolderName identifica una sola carpeta personalizada administrada para agregar a un buzón de correo.
ms.openlocfilehash: 56a7a7d256624c5103c88a333222807519d21501
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764687"
---
# <a name="foldername"></a>FolderName

El elemento **FolderName** identifica una sola carpeta personalizada administrada para agregar a un buzón de correo. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[Nombres de carpetas](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Nombres de carpetas](foldernames.md) <br/> |Contiene una matriz de con nombre carpetas personalizadas administradas para agregar a un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa un nombre de carpeta.
  
## <a name="remarks"></a>Notas

Aunque puede usar servicios Web de Exchange para agregar carpetas personalizadas administradas a un buzón de correo, no puede usar la misma tecnología para tener acceso a la lista de carpetas personalizadas administradas disponibles. Puede obtener una lista de las carpetas personalizadas administradas mediante el uso de un comando de Shell de administración de Exchange o mediante el uso de una API que interactúa con el servicio de directorio de Active Directory. Nombre de la carpeta es el nombre del objeto de Active Directory correspondiente.
  
Puede usar la [operación FindFolder](findfolder-operation.md) para buscar carpetas personalizadas administradas. Usar la [operación DeleteFolder](deletefolder-operation.md) para eliminar las carpetas personalizadas administradas. 
  
Es importante tener en cuenta que **FolderName** es el nombre de una carpeta personalizada administrada existente en la organización. Un intento para agregar una carpeta que no está en la organización, se producirá en una respuesta de error. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de las carpetas administradas](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

