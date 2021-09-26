---
title: CompleteName
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CompleteName
api_type:
- schema
ms.assetid: 22d30d1f-a84d-48bb-ad8f-ce13f8e76604
description: El elemento CompleteName representa el nombre completo de un contacto.
ms.openlocfilehash: 873d372657089d21e86025cdf7812659ac505491
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543558"
---
# <a name="completename"></a>CompleteName

El **elemento CompleteName** representa el nombre completo de un contacto. 
  
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
|[Posnombre](suffix.md) <br/> |Representa un sufijo al nombre de un contacto.  <br/> |
|[Iniciales](initials.md) <br/> |Representa las iniciales de un contacto.  <br/> |
|[FullName](fullname.md) <br/> |Representa el nombre completo de un contacto.  <br/> |
|[Alias](nickname.md) <br/> |Representa el sobrenombre de un contacto.  <br/> |
|[YomiFirstName](yomifirstname.md) <br/> |Representa el nombre usado en Japón para la ortografía fonética o de búsqueda de un nombre en japonés.  <br/> |
|[YomiLastName](yomilastname.md) <br/> |Representa el nombre usado en Japón para la ortografía fonética o de búsqueda de un apellido japonés.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Contact](contact.md) <br/> |Representa un Exchange de contacto.  <br/> |
   
## <a name="remarks"></a>Comentarios

La propiedad CompleteName forma parte de [la forma](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) Predeterminada. En la versión de lanzamiento inicial de Microsoft Exchange Server 2007, la operación [GetItem](getitem-operation.md)devuelve la propiedad CompleteName, pero no [la operación FindItem](finditem-operation.md). A partir Exchange Server 2007 Service Pack 1 (SP1), la operación [FindItem](finditem-operation.md) también devuelve la propiedad CompleteName con la [forma](https://docs.microsoft.com/dotnet/api/exchangewebservices.defaultshapenamestype?view=exchange-ews-proxy) Default. Este cambio no afecta al esquema. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [CompleteNameType](https://msdn.microsoft.com/library/ExchangeWebServices.CompleteNameType.aspx)
- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)

