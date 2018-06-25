---
title: Contacto (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: El elemento de contacto, especifica un contacto en el almacén de contactos unificados.
ms.openlocfilehash: f1593da78a46851c7db43abc567eb66c0c74e0f2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763784"
---
# <a name="contact-contacttype"></a>Contacto (ContactType)

El elemento **de contacto** , especifica un contacto en el almacén de contactos unificados. 
  
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

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |Especifica el nombre de un individuo.  <br/> |
|[BusinessName](businessname.md) <br/> |Especifica el nombre de una empresa.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono de un contacto.  <br/> |
|[Direcciones URL](urls.md) <br/> |Especifica una matriz de direcciones URL para un rol.  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Especifica una matriz de direcciones de correo electrónico extraídos.  <br/> |
|[Direcciones (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Especifica una matriz de elementos de la **dirección** .  <br/> |
|[ContactString](contactstring.md) <br/> |Especifica el nombre para mostrar de un contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Contactos (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Especifica una matriz de los contactos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

