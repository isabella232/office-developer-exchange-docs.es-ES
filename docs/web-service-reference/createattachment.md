---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: El elemento CreateAttachment define una solicitud para crear datos adjuntos a un elemento del Exchange almacén.
ms.openlocfilehash: 6716a83b0d1ba9d7f39351da60f7009df04a3fa0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515876"
---
# <a name="createattachment"></a>CreateAttachment

El **elemento CreateAttachment** define una solicitud para crear datos adjuntos a un elemento en el Exchange almacén. 
  
```xml
<CreateAttachment>
   <ParentItemId/>
   <Attachments/>
</CreateAttachment>
```

 **CreateAttachmentType**
## <a name="attributes-and-elements"></a>Atributos y elementos

En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.
  
### <a name="attributes"></a>Atributos

Ninguno.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Identifica el elemento principal Exchange almacén que contiene los datos adjuntos creados. El [elemento ParentItemId](parentitemid.md) debe proporcionar el identificador de un elemento Exchange almacén real. Los elementos del almacén real se pueden recuperar mediante la [operación GetItem](getitem-operation.md); los datos adjuntos se recuperan mediante la [operación GetAttachment](getattachment-operation.md). Se produce un error si se pasa [ParentItemId](parentitemid.md) el identificador de un archivo adjunto. Si [ParentItemId representa](parentitemid.md) el identificador de los datos adjuntos de un elemento existente, la [operación CreateAttachment](createattachment-operation.md) agrega los nuevos datos adjuntos a los datos adjuntos existentes.  <br/> Este elemento es necesario para la [operación CreateAttachment](createattachment-operation.md).  <br/> |
|[Adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se adjuntarán a un elemento del Exchange almacén.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

Los datos adjuntos de un elemento no existen como elemento de almacén. Solo existe como datos adjuntos a un elemento u otros datos adjuntos. Los datos adjuntos de elementos solo se pueden recuperar mediante la [solicitud GetAttachment.](getattachment.md) 
  
Se pueden crear los siguientes datos adjuntos de elementos:
  
- Item
    
- Mensaje
    
- CalendarItem
    
- Contacto
    
- Tarea
    
- MeetingMessage
    
- MeetingRequest
    
El esquema que describe este elemento se encuentra en el directorio virtual EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor Acceso de cliente.
  
## <a name="example"></a>Ejemplo

En el ejemplo siguiente se muestra cómo crear y adjuntar un elemento a otro elemento del Exchange almacén.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" 
                  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="ASkAS"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>MyAttachment</t:Name>
          <t:Message>
            <t:ItemClass>IPM>Note</t:ItemClass>
            <t:Subject>My attachment subject</t:Subject>
            <t:Body BodyType="Text">My attachment body</t:Body>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

## <a name="element-information"></a>Información del elemento

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Nombre de esquema  <br/> |Esquema de mensajes  <br/> |
|Archivo de validación  <br/> |Messages.xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Ver también



[Operación CreateAttachment](createattachment-operation.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)
  
[Operación GetAttachment](getattachment-operation.md)

