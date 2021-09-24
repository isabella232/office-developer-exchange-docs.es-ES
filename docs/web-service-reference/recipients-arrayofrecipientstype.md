---
title: Recipients (ArrayOfRecipientsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Recipients
api_type:
- schema
ms.assetid: f4b71403-cbae-4176-8b2e-3597048c057b
description: El elemento Recipients representa una colección de destinatarios que reciben una copia del mensaje.
ms.openlocfilehash: 232dbb88f54cb551f4f8017ff9d18049a4984783
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529546"
---
# <a name="recipients-arrayofrecipientstype"></a>Recipients (ArrayOfRecipientsType)

El **elemento Recipients** representa una colección de destinatarios que reciben una copia del mensaje. 
  
```XML
<Recipients>
   <Mailbox/>
</Recipients>
```

 **ArrayOfRecipientsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzón](mailbox.md) <br/> |Identifica un objeto de Active Directory habilitado para correo.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[GetMailTips](getmailtips.md) <br/> |Contiene los destinatarios y los tipos de sugerencias de correo que se recuperarán.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
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

