---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: El elemento DeleteFolder define una solicitud para eliminar carpetas de un buzón del Exchange almacén.
ms.openlocfilehash: d1d64b84604acec54d9153144e5bfd7abaece94c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542480"
---
# <a name="deletefolder"></a>DeleteFolder

El **elemento DeleteFolder** define una solicitud para eliminar carpetas de un buzón del Exchange almacén. 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**DeleteType** <br/> |Describe cómo se elimina una carpeta. Este atributo es obligatorio.  <br/> |
   
#### <a name="deletetype-attribute"></a>Atributo DeleteType

|**Valor**|**Descripción**|
|:-----|:-----|
|HardDelete  <br/> |Una carpeta se quita permanentemente del almacén.  <br/> |
|SoftDelete  <br/> |Si el contenedor está habilitado, se mueve una carpeta al contenedor.  <br/> |
|MoveToDeletedItems  <br/> |Se mueve una carpeta a la carpeta Elementos eliminados.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Contiene una matriz de identificadores de carpeta que se usan para identificar las carpetas que se van a eliminar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Las **opciones MoveToDeletedItems** y **HardDelete** son transaccionales, lo que significa que cuando finaliza una llamada de servicio web, la base de datos ha movido el elemento a la carpeta Elementos eliminados o ha quitado permanentemente el elemento de la base de datos Exchange. Este comportamiento es el mismo para MicrosoftExchange Server 2007 y Exchange Server 2010. 
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Operación DeleteFolder](deletefolder-operation.md)

