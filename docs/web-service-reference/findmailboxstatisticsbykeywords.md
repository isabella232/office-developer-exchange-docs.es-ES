---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: El elemento FindMailboxStatisticsByKeywords especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.
ms.openlocfilehash: e667f13b66e439dca88d73a5e05d74846183928c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764633"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

El elemento **FindMailboxStatisticsByKeywords** especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave. 
  
```XML
<FindMailboxStatisticsByKeywords>
    <Mailboxes/>
    <Keywords/>
    <Language/>
    <Senders/>
    <Recipients/>
    <FromDate/>
    <ToDate/>
    <MessageTypes/>
    <SearchDumpster/>
    <IncludePersonalArchive/>
    <IncludeUnsearchableItems/>
</FindMailboxStatisticsByKeywords>
```

 **FindMailboxStatisticsByKeywordsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Buzones de correo (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Contiene una matriz de los buzones afectados por la suspensión.  <br/> |
|[Palabras clave](keywords-ex15websvcsotherref.md) <br/> |Especifica las palabras clave para una búsqueda.  <br/> |
|[Idioma](language.md) <br/> |Contiene el idioma utilizado para la consulta de búsqueda.  <br/> |
|[Remitentes](senders.md) <br/> |Especifica una matriz de direcciones SMTP.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Especifica una matriz de destinatarios de un mensaje.  <br/> |
|[FromDate](fromdate.md) <br/> |Especifica la fecha en que se envió el mensaje.  <br/> |
|[ToDate](todate.md) <br/> |Especifica la fecha en que se recibió el mensaje.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Especifica una matriz de mensajes para buscar.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Especifica si se debe buscar en los elementos eliminados.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Especifica si se debe incluir el archivo personal en la búsqueda.  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Especifica si se incluyen los elementos que no se puede buscar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Observaciones

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensaje  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

