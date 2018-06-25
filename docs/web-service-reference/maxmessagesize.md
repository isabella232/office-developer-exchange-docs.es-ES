---
title: MaxMessageSize
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaxMessageSize
api_type:
- schema
ms.assetid: bb98ac72-9409-4332-81bb-ee3bebb9a00e
description: El elemento MaxMessageSize representa el tamaño máximo de mensaje que puede aceptar un destinatario.
ms.openlocfilehash: 13a5679a03420655356269a7e8b5e22950724164
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836383"
---
# <a name="maxmessagesize"></a>MaxMessageSize

El elemento **MaxMessageSize** representa el tamaño máximo de mensaje que puede aceptar un destinatario. 
  
```XML
<MaxMessageSize/>
```

 **int**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Sugerencias de correo electrónico](mailtips.md) <br/> |Representa los valores de distintos tipos de sugerencias de correo.  <br/> |
|[MailTipsConfiguration (MailTipsServiceConfiguration)](mailtipsconfiguration-mailtipsserviceconfiguration.md) <br/> |Contiene información de configuración de servicio para el servicio de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

El valor de texto es un número entero que representa el tamaño máximo de mensaje un destinatario puede aceptar. Este valor se puede medir en kilobytes o megabytes.
  
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



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

