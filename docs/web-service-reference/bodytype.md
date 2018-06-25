---
title: BodyType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BodyType
api_type:
- schema
ms.assetid: d42ec77b-fb9f-404a-9bf2-1801e8744676
description: El elemento BodyType identifica cómo se da el formato de texto del cuerpo en la respuesta.
ms.openlocfilehash: f8be2e96390b40faa367cf0d34c533accc3b8afb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19763653"
---
# <a name="bodytype"></a>BodyType

El elemento **BodyType** identifica cómo se da el formato de texto del cuerpo en la respuesta. 
  
```xml
<BodyType>Best or HTML or Text</BodyType>
```

**BodyTypeResponseType**

## <a name="attributes-and-elements"></a>Atributos y elementos

Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

Ninguno.
  
### <a name="parent-elements"></a>Elementos principales

|**Element**|**Descripción**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> | Identifica las propiedades de elemento y el contenido que desea incluir en una respuesta GetItem, FindItem o SyncFolderItems.  <br/><br/>Los siguientes son las expresiones de XPath para este elemento:<br/><br/>  `/GetItem/ItemShape`<br/><br/>`/FindItem/ItemShape`<br/><br/>`/SyncFolderItems/ItemShape` <br/> |
|[AttachmentShape](attachmentshape.md) <br/> |Identifica las propiedades de elemento extendido adicional para devolver en una respuesta a una solicitud de [GetAttachment](getattachment.md) .  <br/><br/>La siguiente es la expresión de XPath para este elemento:<br/><br/>  `/GetAttachment/AttachmentShape` <br/> |
   
## <a name="text-value"></a>Valor de texto

En la siguiente tabla se enumera los valores posibles para el elemento **BodyType** . 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|Mejor  <br/> |La respuesta devolverá el contenido disponible más completa del texto del cuerpo. Esto es útil si se desconoce si el contenido es texto o HTML.<br/><br/> El cuerpo devuelto será texto si el cuerpo almacenado es texto sin formato. De lo contrario, la respuesta devolverá HTML si se encuentra el cuerpo almacenado en formato HTML o RTF.<br/><br/> Éste es el valor predeterminado.  <br/> |
|HTML  <br/> |La respuesta devolverá un cuerpo del elemento como HTML.  <br/> |
|Texto  <br/> |La respuesta devolverá un cuerpo del elemento como texto sin formato.  <br/> |
   
## <a name="remarks"></a>Comentarios

Puede identificar el tipo de cuerpo devuelto en la respuesta comprobando el atributo **BodyType** del elemento [Body](body.md) . El atributo **BodyType** identificará el cuerpo como HTML o texto. 
  
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.
  
## <a name="example"></a>Ejemplo

El siguiente ejemplo de una solicitud de muestra donde se usa un elemento **BodyType** . 
  
```xml
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" 
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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
|Espacio de nombres  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Nombre de esquema  <br/> |Esquema de tipos  <br/> |
|Archivo de validación  <br/> |Types.xsd  <br/> |
|Puede estar vacío  <br/> |False  <br/> |
   

