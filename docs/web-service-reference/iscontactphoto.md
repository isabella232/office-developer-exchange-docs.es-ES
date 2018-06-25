---
title: IsContactPhoto
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsContactPhoto
api_type:
- schema
ms.assetid: ae36b5f9-a787-4863-9dbc-258ad724801d
description: El elemento IsContactPhoto indica si el archivo adjunto es una imagen del contacto.
ms.openlocfilehash: a015cd9bdb34ea9275952d5fe252a30cacf888ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835999"
---
# <a name="iscontactphoto"></a>IsContactPhoto

El elemento **IsContactPhoto** indica si el archivo adjunto es una imagen del contacto. 
  
```xml
<IsContactPhoto>true or false</IsContactPhoto>
```

 **boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo que se adjunta a un elemento en el almacén de Exchange.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento puede ser **true** o **false**. El valor predeterminado es **false**.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalada la función del servidor acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

