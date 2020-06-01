---
title: Entrada (PhoneNumber)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: El elemento entry representa un número de teléfono de un contacto.
ms.openlocfilehash: 62f7091bb750dc7ca74b1e5637a437e2cdad4f1c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459640"
---
# <a name="entry-phonenumber"></a>Entrada (PhoneNumber)

El elemento **entry** representa un número de teléfono de un contacto. 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Key** <br/> | Identifica el número de teléfono. El atributo key es del tipo **PhoneNumberKeyType**.<br/><br/> A continuación se muestran los valores posibles para este atributo:<br/><br/>- AssistantPhone  <br/>- BusinessFax  <br/>- BusinessPhone  <br/>- BusinessPhone2  <br/>-Callback  <br/>- CarPhone  <br/>- CompanyMainPhone  <br/>- HomeFax  <br/>-HomePhone  <br/>- HomePhone2  <br/>ISDN (RDSI)  <br/>-MobilePhone  <br/>-OtherFax  <br/>-OtherTelephone  <br/>-Buscapersonas  <br/>- PrimaryPhone  <br/>-Radioteléfono  <br/>-Télex  <br/>- TtyTddPhone  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono de un contacto.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, es necesario un valor de texto que representa un número de teléfono.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también

- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (servicios Web de Exchange)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [Actualizar contactos](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Eliminación de contactos](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

