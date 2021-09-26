---
title: Acciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: El elemento Actions representa el conjunto de acciones que están disponibles para realizarse en un mensaje cuando se cumplan las condiciones.
ms.openlocfilehash: 7f6608af5b8a9eb2772228a638fc42b9558f1e42
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546864"
---
# <a name="actions"></a>Acciones

El **elemento Actions** representa el conjunto de acciones que están disponibles para realizarse en un mensaje cuando se cumplan las condiciones. 
  
[Rule (RuleType)](rule-ruletype.md)
  
```XML
<Actions>
    <AssignCategories>
    <CopyToFolder>
    <Delete>
    <ForwardAsAttachmentToRecipients>
    <ForwardToRecipients>
    <MarkImportance>
    <MarkAsRead>
    <MoveToFolder>
    <PermanentDelete>
    <RedirectToRecipients>
    <SendSMSAlertToRecipients>
    <ServerReplyWithMessage>
    <StopProcessingRules>
</Actions>
```

 **RuleActionsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |Representa las categorías que se marcan en los mensajes de correo electrónico.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta a la que se copiarán los elementos de correo electrónico.  <br/> |
|[Eliminar](delete.md) <br/> |Indica si los mensajes se van a mover a la carpeta Elementos eliminados.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se reenviarán los mensajes como datos adjuntos.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se van a reenviar los mensajes.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Especifica la importancia que debe marcarse en los mensajes.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Indica si los mensajes se marcarán como leídos.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta a la que se van a mover los elementos de correo electrónico.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Indica si los mensajes se eliminarán permanentemente y no se guardarán en la carpeta Elementos eliminados.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se redirigirán los mensajes.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Indica los números de teléfono móvil a los que se enviará una alerta del Servicio de mensajes cortos (SMS).  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Indica. el identificador del mensaje de plantilla que se va a enviar como respuesta a los mensajes entrantes.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Indica si se van a evaluar las reglas posteriores.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rule (RuleType)](rule-ruletype.md) <br/> |Representa una sola regla en el buzón de un usuario.  <br/> |
   
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
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Condiciones](conditions.md)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

