---
title: SenderSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SenderSmtpAddress
api_type:
- schema
ms.assetid: e39c7df7-4bfa-455f-b4bb-1f1d05398eec
description: El elemento SenderSmtpAddress representa la dirección de correo electrónico SMTP correspondiente al buzón de correo que contiene la carpeta que se va a compartir.
ms.openlocfilehash: 73047dcecfbccb55d74e373891c3154bc7baeeba
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464899"
---
# <a name="sendersmtpaddress"></a>SenderSmtpAddress

El elemento **SenderSmtpAddress** representa la dirección de correo electrónico SMTP correspondiente al buzón de correo que contiene la carpeta que se va a compartir. 
  
```xml
<SenderSmtpAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetSharingMetadata](getsharingmetadata.md) <br/> |Define una solicitud para obtener un token de autenticación opaco que identifique la invitación de uso compartido.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Se necesita un valor de texto que represente una dirección SMTP.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de IIS que hospeda los servicios Web de Exchange del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.
  
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

