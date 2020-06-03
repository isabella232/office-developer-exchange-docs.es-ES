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
description: El elemento GetSharingMetadata define una solicitud para obtener un token de autenticación opaco que identifique la invitación para uso compartido. Este elemento es el elemento base para la operación GetSharingMetadata.
ms.openlocfilehash: 406908e566d6d4249003b1a19a9ce79b8b328c4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530849"
---
# <a name="getsharingmetadata"></a>GetSharingMetadata

El elemento **GetSharingMetadata** define una solicitud para obtener un token de autenticación opaco que identifique la invitación para uso compartido. Este elemento es el elemento base para la [operación GetSharingMetadata](getsharingmetadata-operation.md).
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[IdOfFolderToShare](idoffoldertoshare.md) <br/> |Representa el identificador de la carpeta en el servidor que se va a compartir. Se requiere este elemento.  <br/> |
|[SenderSmtpAddress](sendersmtpaddress.md) <br/> |Representa la dirección de correo electrónico SMTP que corresponde al buzón de correo que contiene la carpeta identificada por el elemento [IdOfFolderToShare](idoffoldertoshare.md) . Se requiere este elemento.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Representa las direcciones de correo electrónico SMTP de una o más entidades a las que se va a conceder acceso a los datos de la carpeta identificada por el elemento [IdOfFolderToShare](idoffoldertoshare.md) . Se requiere este elemento.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguna.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

