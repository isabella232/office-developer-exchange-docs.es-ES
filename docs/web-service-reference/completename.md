---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: El elemento CompleteName representa el nombre completo de un contacto.
ms.openlocfilehash: 1f6c9ba68fe941f848d0e250a39aea6894fca61e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763754"
---
# <a name="completename"></a>CompleteName

El elemento **CompleteName** representa el nombre completo de un contacto. 
  
```xml
<CompleteName>
   <Title/>
   <FirstName/>
   <MiddleName/>
   <LastName/>
   <Suffix/>
   <Initials/>
   <FullName/>
   <Nickname/>
   <YomiFirstName/>
   <YomiLastName/>
</CompleteName>
```

 **CompleteNameType**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[Title](title.md) <br/> |Representa el título de un contacto.  <br/> |
|[FirstName](firstname.md) <br/> |Representa el nombre del contacto.  <br/> |
|[MiddleName](middlename.md) <br/> |Representa el segundo nombre de un contacto.  <br/> |
|[LastName (apellidos)](lastname.md) <br/> |Representa el último nombre de un contacto.  <br/> |
|[Suffix](suffix.md) <br/> |Representa un sufijo de nombre de un contacto.  <br/> |
|[Iniciales](initials.md) <br/> |Representa las iniciales del contacto.  <br/> |
|[FullName](fullname.md) <br/> |Representa el nombre completo de un contacto.  <br/> |
|[Alias](nickname.md) <br/> |Representa el alias de un contacto.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Representa el nombre utilizado en Japón para la ortografía que admite búsqueda o fonética de un nombre en japonés.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Representa el nombre utilizado en Japón para la ortografía que admite búsqueda o fonética del apellido en japonés.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad [CompleteName](completename.md) es parte de la forma [predeterminada](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx) . En la versión inicial de Microsoft Exchange Server 2007, la propiedad [CompleteName](completename.md) es devuelto por la [operación GetItem](getitem-operation.md), pero no la [operación FindItem](finditem-operation.md). A partir de Exchange Server 2007 Service Pack 1 (SP1), la [operación FindItem](finditem-operation.md) también devuelve la propiedad [CompleteName](completename.md) con la forma [predeterminada](https://msdn.microsoft.com/library/ExchangeWebServices.DefaultShapeNamesType.Default.aspx) . Este cambio no afecta el esquema. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



[CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
  
[CompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.ContactItemType.CompleteName.aspx)
  
[contactsCompleteName](https://msdn.microsoft.com/library/ExchangeWebServices.UnindexedFieldURIType.contactsCompleteName.aspx)


- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)


[Creación de contactos (servicios Web de Exchange)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

