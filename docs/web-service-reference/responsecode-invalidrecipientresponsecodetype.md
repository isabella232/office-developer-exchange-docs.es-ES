---
title: ResponseCode (InvalidRecipientResponseCodeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ResponseCode
api_type:
- schema
ms.assetid: 582e9caa-d2bc-4be1-a460-739294f9ef18
description: El elemento ResponseCode proporciona información sobre por qué el destinatario no es válido.
ms.openlocfilehash: 33cd05aca672e250f288aec72d876734132d2e36
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544811"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

El **elemento ResponseCode** proporciona información sobre por qué el destinatario no es válido. 
  
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

En la tabla siguiente se enumeran los valores posibles para el **elemento ResponseCode.** 
  
|**Código**|**Descripción**|
|:-----|:-----|
|OtherError  <br/> |Indica que otro código de respuesta de error no especifica el error.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Indica que una relación de uso compartido no está disponible con la organización especificada en la dirección de correo electrónico SMTP del destinatario.  <br/> |
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
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

