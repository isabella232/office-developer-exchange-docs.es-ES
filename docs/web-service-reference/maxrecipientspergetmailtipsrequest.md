---
title: MaxRecipientsPerGetMailTipsRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MaxRecipientsPerGetMailTipsRequest
api_type:
- schema
ms.assetid: 8ff5df18-1989-4217-b4c0-599232911d0c
description: El elemento MaxRecipientsPerGetMailTipsRequest indica el número máximo de destinatarios que se pueden pasar a la operación GetMailTips.
ms.openlocfilehash: 27a67a5ff5a048dbd23bf5dc530a82f82b422e14
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524682"
---
# <a name="maxrecipientspergetmailtipsrequest"></a>MaxRecipientsPerGetMailTipsRequest

El **elemento MaxRecipientsPerGetMailTipsRequest** indica el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).
  
```XML
<MaxRecipientsPerGetMailTipsRequest/>
```

 **int**
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

El valor de texto es un entero que representa el número máximo de destinatarios que se pueden pasar a la [operación GetMailTips](getmailtips-operation.md).
  
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

