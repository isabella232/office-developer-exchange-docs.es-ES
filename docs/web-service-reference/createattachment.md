---
title: CreateAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachment
api_type:
- schema
ms.assetid: e33b403a-b7d3-48ee-8d24-6b7abf0d70bc
description: El elemento CreateAttachment define una solicitud para crear datos adjuntos a un elemento en el almacén de Exchange.
ms.openlocfilehash: 4cba1b8865dae5da58b9617b249a29314c67331a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466440"
---
# <a name="createattachment"></a>CreateAttachment

El elemento **CreateAttachment** define una solicitud para crear datos adjuntos a un elemento en el almacén de Exchange. 
  
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

Ninguna.
  
### <a name="child-elements"></a>Elementos secundarios

|**Elemento**|**Descripción**|
|:-----|:-----|
|[ParentItemId](parentitemid.md) <br/> |Identifica el elemento de almacén de Exchange primario que contiene los datos adjuntos creados. El elemento [ParentItemId](parentitemid.md) debe proporcionar el identificador de un elemento real del almacén de Exchange. Los elementos de almacenamiento reales se pueden recuperar mediante la [operación GetItem](getitem-operation.md); los datos adjuntos se recuperan mediante la [operación GetAttachment](getattachment-operation.md). Se produce un error si se pasa el identificador de un archivo adjunto a [ParentItemId](parentitemid.md) . Si el [ParentItemId](parentitemid.md) representa el identificador de un dato adjunto del elemento existente, la [operación CreateAttachment](createattachment-operation.md) agrega los nuevos datos adjuntos a los datos adjuntos existentes.  <br/> Este elemento es obligatorio para la [operación CreateAttachment](createattachment-operation.md).  <br/> |
|[Datos adjuntos](attachments-ex15websvcsotherref.md) <br/> |Contiene los elementos o archivos que se van a adjuntar a un elemento en el almacén de Exchange.  <br/> |
   
### <a name="parent-elements"></a>Elementos principales

Ninguno.
  
## <a name="remarks"></a>Comentarios

No existe un elemento adjunto como elemento de almacén. Sólo existe como datos adjuntos a un elemento u otros datos adjuntos. Los datos adjuntos de elemento solo se pueden recuperar mediante la solicitud [GetAttachment](getattachment.md) . 
  
Se pueden crear los siguientes datos adjuntos de elementos:
  
- Elemento
    
- Mensaje
    
- CalendarItem
    
- Contacto
    
- Tarea
    
- MeetingMessage
    
- MeetingRequest
    
El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.
  
## <a name="example"></a>Ejemplo

En el siguiente ejemplo, se muestra cómo crear y adjuntar un elemento a otro elemento del almacén de Exchange.
  
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
|Archivo de validación  <br/> |Messages. xsd  <br/> |
|Puede estar vacío  <br/> |Falso  <br/> |
   
## <a name="see-also"></a>Vea también



[Operación CreateAttachment](createattachment-operation.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)
  
[Operación GetAttachment](getattachment-operation.md)

