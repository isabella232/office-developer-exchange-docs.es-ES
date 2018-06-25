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
description: El elemento ResponseCode proporciona información acerca de por qué el destinatario no es válido.
ms.openlocfilehash: 3bff99dd1ac6603ce31d5ceb074e73ef48190bb2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837186"
---
# <a name="responsecode-invalidrecipientresponsecodetype"></a>ResponseCode (InvalidRecipientResponseCodeType)

El elemento **ResponseCode** proporciona información acerca de por qué el destinatario no es válido. 
  
```XML
<ResponseCode>OtherError or RecipientOrganizationNotFederated or CannotObtainTokenFromSTS or SystemPolicyBlocksSharingWithThisRecipient or RecipientOrganizationFederatedWithUnknownTokenIssuer</ResponseCode>
```

 **InvalidRecipientResponseCodeType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[InvalidRecipient](invalidrecipient.md) <br/> |Contiene la dirección SMTP del destinatario no válido y la información acerca de por qué el destinatario no es válido.  <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **ResponseCode** . 
  
|**Código**|**Descripción**|
|:-----|:-----|
|OtherError  <br/> |Indica que el error no se especifica por otro código de respuesta de error.  <br/> |
|RecipientOrganizationNotFederated  <br/> |Indica que una relación de uso compartida no está disponible con la organización especificada en la dirección de correo electrónico SMTP del destinatario.  <br/> |
|CannotObtainTokenFromSTS  <br/> |Indica que se ha producido un problema al obtener un token de seguridad desde el servidor de token.  <br/> |
|SystemPolicyBlocksSharingWithThisRecipient  <br/> |Indica que el administrador del sistema ha establecido una directiva del sistema que bloquea el uso compartido con el destinatario especificado.  <br/> |
|RecipientOrganizationFederatedWithUnknownTokenIssuer  <br/> |Indica que el servicio de token seguro que se usa el destinatario especificado es desconocido.  <br/> |
   
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación GetSharingMetadata](getsharingmetadata-operation.md)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

