---
title: BccRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BccRecipient
api_type:
- schema
ms.assetid: 4ef0cff5-8a5a-4d76-9d2b-938774d8fc1b
description: El elemento BccRecipient representa un destinatario para recibir una copia de carbón ciego (CCO) de un mensaje de correo electrónico.
ms.openlocfilehash: 178606d9c27becbf6fea5e7a9a694fb67feadc49
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526868"
---
# <a name="bccrecipient"></a>BccRecipient

El **elemento BccRecipient** representa un destinatario para recibir una copia de carbón ciego (CCO) de un mensaje de correo electrónico. 
  
```XML
<BccRecipient>true | false</BccRecipient>
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
|[RecipientTrackingEvent](recipienttrackingevent.md) <br/> |Contiene información para un único evento para un destinatario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento puede ser **true** o **false**. Un valor de **true** indica que el destinatario es carbón ciego copiado; un valor de **false** indica que el destinatario no está copiado en carbono ciego. 
  
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



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

