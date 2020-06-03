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
ms.openlocfilehash: 9b5d2646ec37b41cd88d7de61573bfb4a8746cdf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527176"
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

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Title](title.md) <br/> |Representa el título de un contacto.  <br/> |
|[FirstName](firstname.md) <br/> |Representa el primer nombre del contacto.  <br/> |
|[MiddleName](middlename.md) <br/> |Representa el segundo nombre de un contacto.  <br/> |
|[LastName](lastname.md) <br/> |Representa el apellido de un contacto.  <br/> |
|[Posnombre](suffix.md) <br/> |Representa un sufijo para el nombre de un contacto.  <br/> |
|[Iniciales](initials.md) <br/> |Representa las iniciales de un contacto.  <br/> |
|[FullName](fullname.md) <br/> |Representa el nombre completo de un contacto.  <br/> |
|[Llamamos](nickname.md) <br/> |Representa el alias de un contacto.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Representa el nombre usado en Japón para la escritura fonética o de búsqueda en un nombre fonético de japonés.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Representa el nombre usado en Japón para la ortografía que se pueden buscar o fonéticamente con un apellido en japonés.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contacto](contact.md) <br/> |Representa un elemento de contacto de Exchange.  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad CompleteName forma parte de la forma [predeterminada](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) . En la versión de lanzamiento inicial de Microsoft Exchange Server 2007, la [operación GetItem](getitem-operation.md)devuelve la propiedad CompleteName, pero no la [operación FindItem](finditem-operation.md). A partir de Exchange Server 2007 Service Pack 1 (SP1), la [operación FindItem](finditem-operation.md) también devuelve la propiedad CompleteName con la forma [predeterminada](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) . Este cambio no afecta al esquema. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (servicios Web de Exchange)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

