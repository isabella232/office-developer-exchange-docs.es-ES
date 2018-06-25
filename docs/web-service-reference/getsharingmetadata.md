---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: El elemento GetSharingMetadata define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir. Este elemento es el elemento base para la operación GetSharingMetadata.
ms.openlocfilehash: 5283d35e11350ef10ed8cc01527e787ef54be927
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835677"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

El elemento **GetSharingMetadata** define una solicitud para obtener un token de autenticación opaco que identifica la invitación para compartir. Este elemento es el elemento base para la [operación de GetSharingMetadata](getsharingmetadata-operation.md).
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Representa el identificador de la carpeta en el servidor que se van a compartir. Se requiere este elemento.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Representa la dirección de correo electrónico SMTP que corresponde al buzón que contiene la carpeta que se identifica con el elemento [IdOfFolderToShare](idoffoldertoshare.md) . Se requiere este elemento.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Representa las direcciones de correo electrónico SMTP de una o varias entidades que se concederá acceso a los datos de la carpeta que se identifica con el elemento [IdOfFolderToShare](idoffoldertoshare.md) . Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
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

