---
title: Contact (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: El elemento Contact especifica un contacto en el Almacén de contactos unificado.
ms.openlocfilehash: e52573841f934a11c05a1da9e19f91146ed9c774
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511996"
---
# <a name="contact-contacttype"></a>Contact (ContactType)

El **elemento Contact** especifica un contacto en el Almacén de contactos unificado. 
  
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

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |Especifica el nombre de una persona.  <br/> |
|[BusinessName](businessname.md) <br/> |Especifica el nombre de una empresa.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono para un contacto.  <br/> |
|[Urls](urls.md) <br/> |Especifica una matriz de direcciones URL para una persona.  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Especifica una matriz de direcciones de correo electrónico extraídas.  <br/> |
|[Addresses (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Especifica una matriz de **elementos Address.**  <br/> |
|[ContactString](contactstring.md) <br/> |Especifica el nombre para mostrar de un contacto.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contacts (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Especifica una matriz de contactos.  <br/> |
   
## <a name="remarks"></a>Comentarios

Este elemento se introdujo en Exchange Server 2013.
  
El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipo  <br/> |
|Archivo de validación  <br/> |types.xsd  <br/> |
|Puede estar vacío  <br/> ||
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

