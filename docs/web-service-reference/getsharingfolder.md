---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: El elemento GetSharingFolder define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada. Éste es el elemento base para la operación GetSharingFolder.
ms.openlocfilehash: 7c2f31aa27c1cbde6cdad2b41a341916b4bed2ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835669"
---
# <a name="getsharingfolder"></a>GetSharingFolder

El elemento **GetSharingFolder** define una solicitud para obtener el identificador de la carpeta local de una carpeta compartida especificada. Éste es el elemento base para la [operación de GetSharingFolder](getsharingfolder-operation.md).
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 **GetSharingFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Representa la dirección de correo electrónico SMTP de la otra parte en la relación de uso compartida. Se requiere este elemento.  <br/> |
|[DataType](datatype.md) <br/> |Describe el tipo de datos que se comparten por una carpeta compartida. Este elemento es opcional.  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |Representa el identificador de la carpeta compartida que se debe devolver cuyo identificador de la carpeta local. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Un elemento GetSharingFolder debe contener un elemento [SmtpAddress](smtpaddress.md) . Un elemento GetSharingFolder también debe contener un elemento de [tipo de datos](datatype.md) o un elemento [SharedFolderId](sharedfolderid.md) , pero no puede contener ambas. 
  
El esquema que describe este elemento se encuentra en el directorio Virtual de IIS que hospeda los servicios Web Exchange del equipo que ejecuta a Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingFolder](getsharingfolder-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

