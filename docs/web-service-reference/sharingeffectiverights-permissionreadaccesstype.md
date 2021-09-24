---
title: SharingEffectiveRights (PermissionReadAccessType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SharingEffectiveRights
api_type:
- schema
ms.assetid: 808bb4a1-aa2d-48c5-94b3-551b52c348bd
description: El elemento SharingEffectiveRights indica los permisos que el usuario tiene para los datos de contacto que se comparten.
ms.openlocfilehash: ecae44dd99f61e1e59648134d10190a758a28b17
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531782"
---
# <a name="sharingeffectiverights-permissionreadaccesstype"></a>SharingEffectiveRights (PermissionReadAccessType)

El **elemento SharingEffectiveRights** indica los permisos que el usuario tiene para los datos de contacto que se comparten. 
  
```XML
<SharingEffectiveRights>None | FullDetails</SharingEffectiveRights >
```

 **PermissionReadAccessType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ContactsFolder](contactsfolder.md) <br/> |Representa una carpeta Contactos que se encuentra en un buzón.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para **el elemento SharingEffectiveRights.** 
  
**Valores de texto del elemento SharingEffectiveRights**

|**Valor**|**Descripción**|
|:-----|:-----|
|Ninguno  <br/> |Indica que el usuario no tiene permiso para leer los elementos de la carpeta.  <br/> |
|FullDetails  <br/> |Indica que el usuario tiene permiso para leer todos los elementos de la carpeta.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

