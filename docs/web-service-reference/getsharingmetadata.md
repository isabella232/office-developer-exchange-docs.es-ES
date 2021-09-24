---
title: GetSharingMetadata
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetSharingMetadata
api_type:
- schema
ms.assetid: b609ee26-6d28-4559-81b6-b8e8d4759a23
description: El elemento GetSharingMetadata define una solicitud para obtener un token de autenticación opaco que identifique la invitación para compartir. Este elemento es el elemento base de la operación GetSharingMetadata.
ms.openlocfilehash: 65da8371b25c42e59f898c79403f06fa17e5a24a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523058"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

El **elemento GetSharingMetadata** define una solicitud para obtener un token de autenticación opaco que identifique la invitación para compartir. Este elemento es el elemento base de la [operación GetSharingMetadata](getsharingmetadata-operation.md).
  
```XML
<GetSharingMetadata>
   <IdOfFolderToShare/>
   <SenderSmtpAddress/>
   <Recipients/>
</GetSharingMetadata>
```

 **GetSharingMetadataType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Representa el identificador de la carpeta en el servidor que se compartirá. Se requiere este elemento.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Representa la dirección de correo electrónico SMTP que corresponde al buzón que contiene la carpeta identificada por el [elemento IdOfFolderToShare.](idoffoldertoshare.md) Se requiere este elemento.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Representa las direcciones de correo electrónico SMTP de una o más entidades a las que se concederá acceso a los datos de la carpeta identificada por el [elemento IdOfFolderToShare.](idoffoldertoshare.md) Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

