---
title: CopyToFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CopyToFolder
api_type:
- schema
ms.assetid: 6fd8a6b8-d813-43ff-991b-0e9e782fe00e
description: El elemento CopyToFolder especifica el identificador de la carpeta a la que se pueden copiar los elementos de correo electrónico.
ms.openlocfilehash: a26072f6f316df1734d32cab24a0108ab3c513b3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543467"
---
# <a name="copytofolder"></a>CopyToFolder

El **elemento CopyToFolder** especifica el identificador de la carpeta a la que se pueden copiar los elementos de correo electrónico. 
  
```XML
<CopyToFolder>
    <FolderId></FolderId>
    <DistinguishedFolderId></DistinguisedFolderId>
</CopyToFolder>
```

 **TargetFolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Contiene el identificador de una carpeta de destino para un elemento o carpeta copiados o movidos.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifica una carpeta de destino con nombre para un elemento o carpeta copiados o movidos.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Actions](actions.md) <br/> |Representa el conjunto de acciones que están disponibles para realizarse en un mensaje cuando se cumplan las condiciones.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también



[MoveToFolder](movetofolder.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

