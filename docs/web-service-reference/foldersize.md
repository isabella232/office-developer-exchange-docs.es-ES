---
title: FolderSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderSize
api_type:
- schema
ms.assetid: 27e5f0cd-e23a-4ddd-943a-9f17bf0fd87b
description: El elemento cafolders describe el tamaño total de todo el contenido de una carpeta administrada.
ms.openlocfilehash: 8ed493cfb0c2cabd02d28354c115a73662992473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461341"
---
# <a name="foldersize"></a>FolderSize

El elemento **Cafolders** describe el tamaño total de todo el contenido de una carpeta administrada. 
  
```xml
<FolderSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Contiene información acerca de una carpeta administrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto representa el tamaño total de la carpeta en megabytes.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateManagedFolder](createmanagedfolder-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

