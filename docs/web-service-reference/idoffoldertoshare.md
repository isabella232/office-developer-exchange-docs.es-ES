---
title: IdOfFolderToShare
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IdOfFolderToShare
api_type:
- schema
ms.assetid: 199d1839-f061-4070-a977-874b0c08e5be
description: El elemento IdOfFolderToShare representa el identificador de la carpeta en el servidor que se van a compartir.
ms.openlocfilehash: 1e3e53819f23bbc5753ac21b9e3ea6593ac4826c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835853"
---
# <a name="idoffoldertoshare"></a>IdOfFolderToShare

El elemento **IdOfFolderToShare** representa el identificador de la carpeta en el servidor que se van a compartir. 
  
```
<IdOfFolderToShare Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Attribute**|**Descripción**|
|:-----|:-----|
|Id  <br/> |Contiene una cadena que identifica una carpeta en el almacén de Exchange. Este atributo es necesario.  <br/> |
|ChangeKey  <br/> |Contiene una cadena que identifica una versión de una carpeta que se identifica con el atributo Id. Este atributo es opcional. Use este atributo para asegurarse de que se usa la versión correcta de una carpeta.  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |Define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

