---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: El elemento BodyType identifica cómo se formatea el texto del cuerpo en la respuesta.
ms.openlocfilehash: e8952ac2774589e031280ce982ea8671b736a87d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526844"
---
# <a name="bodytype"></a>BodyType

El **elemento BodyType** identifica cómo se formatea el texto del cuerpo en la respuesta. 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades y el contenido del elemento que se incluirán en una respuesta GetItem, FindItem o SyncFolderItems.  <br/><br/>Las siguientes son las expresiones XPath de este elemento:<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifica propiedades de elementos extendidas adicionales para devolver en una respuesta a una [solicitud GetAttachment.](getattachment.md)  <br/><br/>A continuación se muestra la expresión XPath de este elemento:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

En la tabla siguiente se enumeran los valores posibles para el **elemento BodyType.** 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Procedimientos  <br/> |La respuesta devolverá el contenido más completo disponible del texto del cuerpo. Esto es útil si se desconoce si el contenido es texto o HTML.<br/><br/> El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato. De lo contrario, la respuesta devolverá HTML si el cuerpo almacenado está en formato HTML o RTF.<br/><br/> Este es el valor predeterminado.  <br/> |
|HTML  <br/> |La respuesta devolverá un cuerpo del elemento como HTML.  <br/> |
|Texto  <br/> |La respuesta devolverá un cuerpo del elemento como texto sin formato.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede identificar el tipo de cuerpo devuelto en la respuesta comprobando el **atributo BodyType** del [elemento Body.](body.md) El **atributo BodyType** identificará el cuerpo como HTML o texto. 
  
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo de una solicitud se muestra dónde se usa **un elemento BodyType.** 
  
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
        <t:BodyType>Best</t:BodyType>
      </AttachmentShape>
      <AttachmentIds>
        <t:AttachmentId Id="ASkAS="/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

El atributo Id se ha acortado para conservar la legibilidad.
  
## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   

