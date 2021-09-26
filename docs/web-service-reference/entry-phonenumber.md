---
title: Entry (PhoneNumber)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: e3d0a4d5-8af8-4607-aa2e-ef3111b63b55
description: El elemento Entry representa un número de teléfono de un contacto.
ms.openlocfilehash: f9f8f08c8d167614bfc5772d6d74ebee77234c70
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545247"
---
# <a name="entry-phonenumber"></a>Entry (PhoneNumber)

El **elemento Entry** representa un número de teléfono de un contacto. 
  
```xml
<Entry Key=""/>
```

 **PhoneNumberDictionaryEntryType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

|**Atributo**|**Descripción**|
|:-----|:-----|
|**Clave** <br/> | Identifica el número de teléfono. El atributo Key es del tipo **PhoneNumberKeyType**.<br/><br/> Estos son los valores posibles para este atributo:<br/><br/>- AssistantPhone  <br/>- BusinessFax  <br/>- BusinessPhone  <br/>- BusinessPhone2  <br/>- Devolución de llamada  <br/>- CarPhone  <br/>- CompanyMainPhone  <br/>- HomeFax  <br/>- HomePhone  <br/>- HomePhone2  <br/>- Isdn  <br/>- MobilePhone  <br/>- OtherFax  <br/>- OtherTelephone  <br/>- Pager  <br/>- PrimaryPhone  <br/>- RadioPhone  <br/>- Telex  <br/>- TtyTddPhone  <br/> |
   
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[PhoneNumbers](phonenumbers.md) <br/> |Representa una colección de números de teléfono para un contacto.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Si se usa este elemento, se requiere un valor de texto que representa un número de teléfono.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre del esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Consulte también

- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)
- [Creación de contactos (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx) 
- [Actualizar contactos](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)  
- [Eliminación de contactos](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

