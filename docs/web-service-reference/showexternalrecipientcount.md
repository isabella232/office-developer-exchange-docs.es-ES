---
title: ShowExternalRecipientCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ShowExternalRecipientCount
api_type:
- schema
ms.assetid: db28dbcb-d051-4e5c-a9c2-4b8d5149b4e1
description: El elemento ShowExternalRecipientCount indica si los consumidores de la operación GetMailTips deben mostrar sugerencias de correo que indiquen el número de destinatarios externos a los que se dirige un mensaje.
ms.openlocfilehash: 30615dcb1091dff01cf13679e3e1ed68c8b25af9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539104"
---
# <a name="showexternalrecipientcount"></a>ShowExternalRecipientCount

El **elemento ShowExternalRecipientCount** indica si los consumidores de la operación [GetMailTips](getmailtips-operation.md) deben mostrar sugerencias de correo que indiquen el número de destinatarios externos a los que se dirige un mensaje. 
  
```XML
<ShowExternalRecipientCount>true | false</ShowExternalRecipientCount>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Contiene información de configuración de servicio para el servicio de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto de este elemento es **true** si los consumidores de la operación [GetMailTips](getmailtips-operation.md) tienen que mostrar sugerencias de correo que indican el número de destinatarios externos a los que se dirige un mensaje. El valor es **false** si los consumidores de la operación [GetMailTips](getmailtips-operation.md) no tienen que mostrar sugerencias de correo que indiquen el número de destinatarios externos a los que se dirige un mensaje. 
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación GetMailTips](getmailtips-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

