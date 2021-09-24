---
title: FolderName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderName
api_type:
- schema
ms.assetid: c5a2cd55-ac47-43bf-94b5-3ab3a4c28a62
description: El elemento FolderName identifica una única carpeta personalizada administrada que se agregará a un buzón.
ms.openlocfilehash: 76263d56c423411a58ea45d691ce93e2b3202571
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511568"
---
# <a name="foldername"></a>FolderName

El **elemento FolderName** identifica una única carpeta personalizada administrada que se agregará a un buzón. 
  
[CreateManagedFolder](createmanagedfolder.md)
  
[FolderNames](foldernames.md)
  
[FolderName](foldername.md)
  
```xml
<FolderName>...</FolderName>
```

 **string**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderNames](foldernames.md) <br/> |Contiene una matriz de carpetas personalizadas administradas con nombre para agregar a un buzón.  <br/> A continuación se muestra la expresión XPath de este elemento:  <br/>  `/CreateManagedFolder/FolderNames` <br/> |
   
## <a name="text-value"></a>Valor de texto

Se requiere un valor de texto. El valor de texto representa un nombre de carpeta.
  
## <a name="remarks"></a>Comentarios

Aunque puede usar Exchange Web Services para agregar carpetas personalizadas administradas a un buzón, no puede usar la misma tecnología para obtener acceso a la lista de carpetas personalizadas administradas disponibles. Puede obtener una lista de carpetas personalizadas administradas mediante un comando del Shell de administración de Exchange o mediante una API que interfaces con el servicio de directorio de Active Directory. El nombre de la carpeta es el nombre del objeto de Active Directory correspondiente.
  
Puede usar la operación [FindFolder para](findfolder-operation.md) buscar carpetas personalizadas administradas. Use la [operación DeleteFolder para](deletefolder-operation.md) eliminar carpetas personalizadas administradas. 
  
Es importante tener en cuenta que **FolderName** es el nombre de una carpeta personalizada administrada existente en la organización. Si se intenta agregar una carpeta que no está en la organización, se producirá una respuesta de error. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación FindFolder](findfolder-operation.md)


[Buscar carpetas](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)
  
[Agregar carpetas administradas](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

