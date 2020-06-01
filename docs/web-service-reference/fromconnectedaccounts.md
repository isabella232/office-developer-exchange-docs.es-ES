---
title: FromConnectedAccounts
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FromConnectedAccounts
api_type:
- schema
ms.assetid: d4d7ddd7-078d-4f1a-a26b-22dce0c49f3a
description: El elemento FromConnectedAccounts representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.
ms.openlocfilehash: 159ae064827c2f9c2b470580ad5457264e8dae93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464052"
---
# <a name="fromconnectedaccounts"></a>FromConnectedAccounts

El elemento **FromConnectedAccounts** representa los nombres de cuenta de correo electrónico desde los que se deben agregar los mensajes entrantes para que se aplique la condición o excepción. 
  
```XML
<FromConnectedAccounts>
    <String/>
</FromConnectedAccounts>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[String](string.md) <br/> |Representa un nombre de cuenta de correo electrónico desde el que se deben agregar los mensajes entrantes para que se aplique la condición o excepción.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[Condiciones](conditions.md) <br/> |Representa las condiciones que, cuando se cumplan, desencadenarán las acciones de regla de una regla.  <br/> |
|[Excepciones](exceptions.md) <br/> |Representa las excepciones que representan todas las condiciones de excepción de regla disponibles para una regla de bandeja de entrada.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Verdadero  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS en Exchange](ews-xml-elements-in-exchange.md)

