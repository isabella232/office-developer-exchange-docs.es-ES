---
title: FindMailboxStatisticsByKeywords
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cfe0f0ff-5fea-4db8-ac96-a5724c85ed2f
description: El elemento FindMailboxStatisticsByKeywords especifica una solicitud para buscar estadísticas de buzón por palabra clave.
ms.openlocfilehash: e22c7d8dc849d3fd45d6cb158030cbd82119437e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462531"
---
# <a name="findmailboxstatisticsbykeywords"></a>FindMailboxStatisticsByKeywords

El elemento **FindMailboxStatisticsByKeywords** especifica una solicitud para buscar estadísticas de buzón por palabra clave. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Buzones de correo (ArrayOfUserMailboxesType)](mailboxes-arrayofusermailboxestype.md) <br/> |Contiene una matriz de buzones que se ven afectados por la retención.  <br/> |
|[Keywords](keywords-ex15websvcsotherref.md) <br/> |Especifica palabras clave para una búsqueda.  <br/> |
|[Language](language.md) <br/> |Contiene el idioma usado para la consulta de búsqueda.  <br/> |
|[Remitentes](senders.md) <br/> |Especifica una matriz de direcciones SMTP.  <br/> |
|[Recipients (ArrayOfSmtpAddressType)](recipients-arrayofsmtpaddresstype.md) <br/> |Especifica una matriz de destinatarios de un mensaje.  <br/> |
|[FromDate](fromdate.md) <br/> |Especifica la fecha en que se envió el mensaje.  <br/> |
|[ToDate](todate.md) <br/> |Especifica la fecha en que se recibió el mensaje.  <br/> |
|[MessageTypes](messagetypes.md) <br/> |Especifica una matriz de mensajes para buscar.  <br/> |
|[SearchDumpster](searchdumpster.md) <br/> |Especifica si se deben buscar en los elementos eliminados.  <br/> |
|[IncludePersonalArchive](includepersonalarchive.md) <br/> |Especifica si se va a incluir el archivo personal en la búsqueda.  <br/> |
|[IncludeUnsearchableItems](includeunsearchableitems.md) <br/> |Especifica si se deben incluir los elementos que no se pueden buscar.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |messages. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

