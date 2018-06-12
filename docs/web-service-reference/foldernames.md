---
title: Nombres de carpetas
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderNames
api_type:
- schema
ms.assetid: 6cbe4083-5705-4695-a54e-8dab3e472662
description: El elemento de los nombres de carpetas contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo.
ms.openlocfilehash: 819b3c2df1cfcae3a5d4a48539e369a00b1f7229
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764684"
---
# <a name="foldernames"></a>Nombres de carpetas

El elemento de **los nombres de carpetas** contiene una matriz de las carpetas administradas con nombre para agregar a un buzón de correo. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[Nombres de carpetas](foldernames.md)
  
```xml
<FolderNames>
   <FolderName/>
</FolderNames>
```

 **NonEmptyArrayOfFolderNamesType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[FolderName](foldername.md) <br/> |Identifica una sola carpeta administrada para agregar al buzón de correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[CreateManagedFolder](createmanagedfolder.md) <br/> |El elemento raíz en una solicitud para agregar una carpeta administrada a un buzón de correo.  <br/> La siguiente es la expresión de XPath para este elemento:  <br/>  `/CreateManagedFolder` <br/> |
   
## <a name="remarks"></a>Notas

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Adición de las carpetas administradas](http://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

