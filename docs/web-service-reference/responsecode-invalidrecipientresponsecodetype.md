---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: El elemento ResponseCode proporciona información sobre por qué el destinatario no es válido.
ms.openlocfilehash: d78de64de7725007ec51a55dad13d1cc892a25e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529724"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

El elemento **ResponseCode** proporciona información sobre por qué el destinatario no es válido. 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Contiene la dirección SMTP del destinatario no válido e información sobre por qué el destinatario no es válido.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumeran los valores posibles para el elemento **ResponseCode** . 
  
|**Código**|**Descripción**|
|:-----|:-----|
|OtherError  <br/> |Indica que el error no está especificado por otro código de respuesta de error.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Indica que una relación de uso compartido no está disponible en la organización especificada en la dirección de correo electrónico SMTP del destinatario.  <br/> |
|CannotObtainTokenFromSTS  <br/> |Indica que hubo un problema al obtener un token de seguridad del servidor de tokens.  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |Indica que el administrador del sistema ha establecido una directiva del sistema que bloquea el uso compartido con el destinatario especificado.  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |Indica que el servicio de token seguro que usa el destinatario especificado es desconocido.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

