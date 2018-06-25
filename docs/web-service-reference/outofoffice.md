---
title: Fuera de la oficina
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OutOfOffice
api_type:
- schema
ms.assetid: fe1256ab-5c0f-467d-abb3-b38a2dc312ae
description: El elemento de fuera de la oficina representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta.
ms.openlocfilehash: 4e1e06ee332c44aeba03e1343c8c3258a2c9631e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836675"
---
# <a name="outofoffice"></a>Fuera de la oficina

El elemento de **fuera de la oficina** representa el mensaje de respuesta y un tiempo de duración para enviar el mensaje de respuesta. 
  
```XML
<OutOfOffice>
   <ReplyBody/>
   <Duration/>
</OutOfOffice>
```

 **OutOfOfficeMailTip**
## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Element**|**Descripción**|
|:-----|:-----|
|[ReplyBody](replybody.md) <br/> |Contiene un mensaje de fuera de oficina (OOF) y el idioma utilizado para el mensaje.  <br/> |
|[Duración (UserOofSettings)](duration-useroofsettings.md) <br/> |Contiene la duración que está habilitado el estado de fuera de la oficina si el elemento [OofState](oofstate.md) está establecido en programado.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[Sugerencias de correo electrónico](mailtips.md) <br/> |Representa los valores de distintos tipos de sugerencias de correo.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Ninguno.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   
## <a name="see-also"></a>Vea también



- [Elementos XML de EWS de Exchange](ews-xml-elements-in-exchange.md)

