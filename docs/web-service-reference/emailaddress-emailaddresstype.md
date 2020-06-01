---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: El elemento EmailAddress especifica la dirección SMTP completamente resuelta para el buzón de sitio o el rol asociado.
ms.openlocfilehash: 8b04b75e91cc16be7f88c9a0ac08c5e36855056e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463464"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

El elemento **EmailAddress** especifica la dirección SMTP completamente resuelta para el buzón de sitio o el rol asociado. 
  
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Name (cadena)](name-string.md) <br/> |Especifica un nombre de refinador de búsqueda o una clave o el nombre de un usuario de correo electrónico.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Define la dirección SMTP principal de un usuario de buzón de correo.  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |Especifica el tipo de enrutamiento de una dirección de correo electrónico.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Representa el tipo de buzón que se representa mediante la dirección de correo electrónico.  <br/> |
|[ItemId](itemid.md) <br/> |Contiene el identificador único y la clave de cambio de un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Rol](persona.md) <br/> |Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
El elemento **EmailAddress** se aplica a los clientes de Exchange Online y versiones de Microsoft Exchange Server que empiecen por Exchange 2013. 
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

