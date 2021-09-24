---
title: IsInline
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsInline
api_type:
- schema
ms.assetid: 5e7712c8-372a-4a16-be64-360c5ff3961a
description: El elemento IsInline representa si los datos adjuntos aparecen en línea dentro de un elemento.
ms.openlocfilehash: 0bf51c981f3c9d2a4e38939d349fe662a57b29ac
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518277"
---
# <a name="isinline"></a>IsInline

El **elemento IsInline** representa si los datos adjuntos aparecen en línea dentro de un elemento. 
  
```xml
<IsInline>true or false</IsInline>
```

 **boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[FileAttachment](fileattachment.md) <br/> |Representa un archivo adjunto a un elemento del Exchange almacén.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Representa un Exchange que se adjunta a otro Exchange elemento.  <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento puede ser **true** o **false**. El valor predeterminado es **False**.
  
## <a name="remarks"></a>Comentarios

El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



- [Elementos XML ews en Exchange](ews-xml-elements-in-exchange.md)

