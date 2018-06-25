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
description: El elemento Actions representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones.
ms.openlocfilehash: 093d2f28135c6077b6cea488591573af0182934b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763388"
---
# <a name="actions"></a>Acciones

El elemento **Actions** representa el conjunto de acciones que están disponibles para ser tomadas en un mensaje cuando se cumplen las condiciones. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[AssignCategories](assigncategories.md) <br/> |Representa las categorías que están marcadas en mensajes de correo electrónico.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifica el identificador de la carpeta que se copiarán los elementos de correo electrónico a.  <br/> |
|[Eliminar](delete.md) <br/> |Indica si los mensajes se mueven a la carpeta Elementos eliminados.  <br/> |
|[ForwardAsAttachmentToRecipients](forwardasattachmenttorecipients.md) <br/> |Indica las direcciones de correo electrónico a la que los mensajes deben ser reenviado como datos adjuntos.  <br/> |
|[ForwardToRecipients](forwardtorecipients.md) <br/> |Indica las direcciones de correo electrónico a la que los mensajes se se transfieran.  <br/> |
|[MarkImportance](markimportance.md) <br/> |Especifica la importancia que se mostrará en los mensajes.  <br/> |
|[MarkAsRead](markasread.md) <br/> |Indica si los mensajes se marcan como leídos.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifica el identificador de la carpeta que se moverán los elementos de correo electrónico a.  <br/> |
|[PermanentDelete](permanentdelete.md) <br/> |Indica si los mensajes se eliminan permanentemente y no se ha guardado en la carpeta Elementos eliminados.  <br/> |
|[RedirectToRecipients](redirecttorecipients.md) <br/> |Indica las direcciones de correo electrónico a la que los mensajes se que se redirija.  <br/> |
|[SendSMSAlertToRecipients](sendsmsalerttorecipients.md) <br/> |Indica el número de teléfono móvil a los que es una alerta de servicio de mensajes cortos (SMS) que se envíen.  <br/> |
|[ServerReplyWithMessage](serverreplywithmessage.md) <br/> |Indica. el identificador del mensaje de plantilla que se envía como una respuesta a los mensajes entrantes.  <br/> |
|[StopProcessingRules](stopprocessingrules.md) <br/> |Indica si las reglas que siguen son que se deben evaluar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Regla (RuleType)](rule-ruletype.md) <br/> |Representa una sola regla en el buzón del usuario.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también

- [Condiciones](conditions.md)
- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

