---
title: Operación GetAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetAttachment
api_type:
- schema
ms.assetid: 24d10a15-b942-415e-9024-a6375708f326
description: La operación GetAttachment se usa para recuperar los datos adjuntos de existentes en los elementos en el almacén de Exchange.
ms.openlocfilehash: c260033208bf49c60463c09041d8ffcc52a8f5c2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764759"
---
# <a name="getattachment-operation"></a>Operación GetAttachment

La operación GetAttachment se usa para recuperar los datos adjuntos de existentes en los elementos en el almacén de Exchange.
  
## <a name="getattachment-request-example"></a>Ejemplo de solicitud de GetAttachment

### <a name="description"></a>Descripción

El siguiente ejemplo de solicitud de GetAttachment muestra cómo obtener datos adjuntos.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El elemento [AttachmentShape](attachmentshape.md) permite especificar qué información de datos adjuntos que se debe devolver. Un elemento [AttachmentShape](attachmentshape.md) vacío es válido y representará los datos adjuntos sin contenido MIME para los datos adjuntos de elemento, con un tipo de cuerpo de texto y sin las propiedades adicionales. 
  
La colección de [AttachmentIds](attachmentids.md) permite especificar uno o varios identificadores de datos adjuntos para devolver. Tenga en cuenta que estos son de tipo RequestAttachmentIdType, por lo que cualquier AttachmentIds que reciba de **CreateAttachment** debe tener los atributos **RootItemId** y **RootItemChangeKey** se quita antes de pasarlas a **GetAttachment**.
  
> [!NOTE]
> El identificador de datos adjuntos y la clave de cambio se han abreviado para conservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>Ejemplo de respuesta de GetAttachment

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud de GetAttachment. En este ejemplo se devuelve un archivo adjunto.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:GetAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
              <t:Name>SomeFile</t:Name>
              <t:Content>AQIDBAU=</t:Content>
            </t:FileAttachment>
          </m:Attachments>
        </m:GetAttachmentResponseMessage>
      </m:ResponseMessages>
    </GetAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

Los mensajes de respuesta para GetAttachment siempre va a contener los datos adjuntos completo; es decir, todas las propiedades siempre se incluirán. Los archivos adjuntos, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md)y [contenido](content.md). Los datos adjuntos de elemento, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [ContentId](contentid.md), [ContentLocation](contentlocation.md) y todas las propiedades del elemento, tal y como si se hubiera utilizado la forma de **AllProperties** en una llamada GetItem. El elemento [AttachmentShape](attachmentshape.md) , si está presente, le permitirá que una aplicación de consumidor solicitar propiedades extendidas adicionales para los datos adjuntos del elemento. 
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [GetAttachmentResponse](getattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [GetAttachmentResponseMessage](getattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Datos adjuntos](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
- [Nombre (AttachmentType)](name-attachmenttype.md)
    
- [Contenido](content.md)
    
## <a name="see-also"></a>Vea también



[Operación CreateAttachment](createattachment-operation.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)

