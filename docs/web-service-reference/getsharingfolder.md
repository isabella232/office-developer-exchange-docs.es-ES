---
title: GetSharingFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingFolder
api_type:
- schema
ms.assetid: ed5bb61f-89c7-4baa-83ee-30f06a49ff9b
description: El elemento GetSharingFolder define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada. Es el elemento base de la operación GetSharingFolder.
ms.openlocfilehash: 5d6362dff3ff29b0dc5100780cc70b21ec9bee9d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509773"
---
# <a name="getsharingfolder"></a>GetSharingFolder

El **elemento GetSharingFolder** define una solicitud para obtener el identificador de carpeta local de una carpeta compartida especificada. Es el elemento base de la [operación GetSharingFolder](getsharingfolder-operation.md).
  
```xml
<GetSharingFolder>   <SmtpAddress/>   <DataType/>   <SharedFolderId/></GetSharingFolder>
```

 **GetSharingFolderType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Representa la dirección de correo electrónico SMTP de la otra parte en la relación de uso compartido. Se requiere este elemento.  <br/> |
|[DataType](datatype.md) <br/> |Describe el tipo de datos que comparte una carpeta compartida. Este elemento es opcional.  <br/> |
|[SharedFolderId](sharedfolderid.md) <br/> |Representa el identificador de la carpeta compartida cuyo identificador de carpeta local debe devolverse. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Un elemento GetSharingFolder debe contener un [elemento SmtpAddress.](smtpaddress.md) Un elemento GetSharingFolder también debe contener un [elemento DataType](datatype.md) o [un elemento SharedFolderId,](sharedfolderid.md) pero no puede contener ambos. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda Exchange Servicios web del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetSharingFolder](getsharingfolder-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

