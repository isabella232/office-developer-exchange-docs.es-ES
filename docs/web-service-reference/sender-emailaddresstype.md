---
title: Sender (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Sender
api_type:
- schema
ms.assetid: 717eb6d0-d167-4b20-92e2-5d08b96186c4
description: El elemento Sender representa la dirección de correo electrónico del remitente del mensaje.
ms.openlocfilehash: dbec27c3e21e956cf822821133ae8d435b5f2bfa
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510872"
---
# <a name="sender-emailaddresstype"></a>Sender (EmailAddressType)

El **elemento Sender** representa la dirección de correo electrónico del remitente del mensaje. 
  
```XML
<Sender>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Sender>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Representa el nombre del usuario del buzón. Este elemento es opcional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección principal del Protocolo simple de transferencia de correo (SMTP) de un usuario de buzón de correo. Este elemento es opcional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Representa el protocolo de enrutamiento del destinatario. El valor predeterminado es SMTP. Este elemento es opcional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Representa el tipo de buzón representado por la dirección de correo electrónico. Este elemento es opcional.  <br/> |
|[ItemId](itemid.md) <br/> |Define el identificador de elemento de una lista de contactos o distribución privada para los destinatarios de la carpeta Contactos de un usuario. Este elemento es opcional.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FindMessageTrackingReport](findmessagetrackingreport.md) <br/> |Especifica los criterios para los tipos de mensajes que se deben buscar.  <br/> |
|[MessageTrackingSearchResult](messagetrackingsearchresult.md) <br/> |Contiene un único resultado de mensaje para un [elemento FindMessageTrackingReportResponse.](findmessagetrackingreportresponse.md)  <br/> |
|[MessageTrackingReport](messagetrackingreport.md) <br/> |Contiene un único mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).  <br/> |
   
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



[Operación GetMessageTrackingReport](getmessagetrackingreport-operation.md)


- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

