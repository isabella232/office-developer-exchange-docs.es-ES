---
title: Acciones
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Actions
api_type:
- schema
ms.assetid: c5aa96b1-2d8b-422f-8c2f-f118572ab23f
description: El elemento Actions representa el conjunto de acciones que están disponibles para su realización en un mensaje cuando se cumplan las condiciones.
ms.openlocfilehash: 2ac53778b583595fa8be07f2c5110a9e2df16eca
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465068"
---
# <a name="actions"></a>Acciones

El elemento **Actions** representa el conjunto de acciones que están disponibles para su realización en un mensaje cuando se cumplan las condiciones. 
  
[Regla (RuleType)](rule-ruletype.md)
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |Representa las categorías que se marcan en los mensajes de correo electrónico.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta en la que se copiarán los elementos de correo electrónico.  <br/> |
|[Eliminar](delete.md) <br/> |Indica si los mensajes se moverán a la carpeta elementos eliminados.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se deben reenviar los mensajes como datos adjuntos.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se van a reenviar los mensajes.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Especifica la importancia que se va a estampar en los mensajes.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Indica si los mensajes se deben marcar como leídos.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta a la que se moverán los elementos de correo electrónico.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Indica si los mensajes se eliminan permanentemente y no se guardan en la carpeta elementos eliminados.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Indica las direcciones de correo electrónico a las que se van a redirigir los mensajes.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Indica los números de teléfono móvil a los que se enviará una alerta de servicio de mensajes cortos (SMS).  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Indicar. IDENTIFICADOR del mensaje de plantilla que se va a enviar como respuesta a los mensajes entrantes.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Indica si las reglas posteriores se deben evaluar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Regla (RuleType)](rule-ruletype.md) <br/> |Representa una sola regla en el buzón de un usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Condiciones](conditions.md)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

