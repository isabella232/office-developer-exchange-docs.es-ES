---
title: IncludeMimeContent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IncludeMimeContent
api_type:
- schema
ms.assetid: 3f3c2300-55cd-41c0-900e-b470b290d52f
description: El elemento IncludeMimeContent especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta.
ms.openlocfilehash: 6198e4bef2dc59e6e56a8d3cbe463dad13e544e8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457196"
---
# <a name="includemimecontent"></a>IncludeMimeContent

El elemento **IncludeMimeContent** especifica si se devuelve el contenido de extensiones multipropósito de correo Internet (MIME) de un elemento o datos adjuntos en la respuesta. 
  
```xml
<IncludeMimeContent>true or false</IncludeMimeContent>
```

 **boolean**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguna.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[AttachmentShape](attachmentshape.md) <br/> | Identifica las propiedades adicionales que se van a devolver en una respuesta a una solicitud [GetAttachment](getattachment.md) .  <br/> <br/> La siguiente es la expresión XPath a este elemento:  <br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
|[ItemShape](itemshape.md) <br/> | Identifica el contenido y las propiedades de los elementos que se van a incluir en una respuesta GetItem, FindItem o SyncFolderItems.  <br/> <br/> Las siguientes son las expresiones XPath de este elemento:<br/>  <br/>  `/GetItem/ItemShape` <br/><br/>  `/FindItem/ItemShape` <br/><br/>  `/SyncFolderItems/ItemShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

Este elemento puede ser **true** o **false**. El valor predeterminado es **False**. Se trata de un tipo de datos Boolean.
  
## <a name="remarks"></a>Comentarios

Este elemento es opcional.
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud muestra cómo establecer el elemento **IncludeMimeContent** . 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape>
        <t:IncludeMimeContent>true</t:IncludeMimeContent>
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

El atributo de identificador de datos adjuntos se trunca para preservar la legibilidad.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

