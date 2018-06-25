---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: El elemento EmailAddress especifica la dirección SMTP completa resuelta para el buzón de sitio o de la persona asociada.
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764332"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

El elemento **EmailAddress** especifica la dirección SMTP completa resuelta para el buzón de sitio o de la persona asociada. 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Name (cadena)](name-string.md) <br/> |Especifica un nombre de búsqueda refinador o clave o el nombre de un usuario de correo electrónico.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección SMTP principal de un usuario de buzón de correo.  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |Especifica el tipo de distribución de una dirección de correo electrónico.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Representa el tipo de buzón de correo que está representada por la dirección de correo electrónico.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el único identificador y cambiar la clave de un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
El elemento **EmailAddress** es aplicable para los clientes que estén destinados a Exchange Online y versiones de Exchange 2013 a partir de Microsoft Exchange Server. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

