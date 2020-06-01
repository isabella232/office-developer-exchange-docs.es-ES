---
title: Contacto (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: El elemento Contact especifica un contacto en el almacén de contactos unificados.
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461523"
---
# <a name="contact-contacttype"></a>Contacto (ContactType)

El elemento **Contact** especifica un contacto en el almacén de contactos unificados. 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 **ContactType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |Especifica el nombre de una persona.  <br/> |
|[BusinessName](businessname.md) <br/> |Especifica el nombre de una empresa.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono de un contacto.  <br/> |
|[Urls](urls.md) <br/> |Especifica una matriz de direcciones URL para un rol.  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Especifica una matriz de direcciones de correo electrónico extraídas.  <br/> |
|[Direcciones (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Especifica una matriz de elementos **Address** .  <br/> |
|[ContactString](contactstring.md) <br/> |Especifica el nombre para mostrar de un contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contactos (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Especifica una matriz de contactos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

