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
description: La operación GetAttachment se usa para recuperar datos adjuntos existentes en los elementos del almacén de Exchange.
ms.openlocfilehash: ac7eafd61c62b077a8d20e5fd8d004924bf06cf1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461292"
---
# <a name="getattachment-operation"></a>Operación GetAttachment

La operación GetAttachment se usa para recuperar datos adjuntos existentes en los elementos del almacén de Exchange.
  
## <a name="getattachment-request-example"></a>Ejemplo de solicitud GetAttachment

### <a name="description"></a>Descripción

El siguiente ejemplo de solicitud GetAttachment muestra cómo obtener datos adjuntos.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <GetAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentShape/>
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX..."/>
      </AttachmentIds>
    </GetAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El elemento [AttachmentShape](attachmentshape.md) permite especificar qué información de archivos adjuntos se debe devolver. Un elemento [AttachmentShape](attachmentshape.md) vacío es válido y representará los datos adjuntos sin contenido MIME para los datos adjuntos de elemento, con un tipo de cuerpo de texto y sin propiedades adicionales. 
  
La colección [identificadores](attachmentids.md) permite especificar uno o más identificadores de datos adjuntos que se van a devolver. Tenga en cuenta que son de tipo RequestAttachmentIdType, por lo que cualquier identificadores que reciba de **CreateAttachment** debe tener los atributos **RootItemId** y **RootItemChangeKey** antes de pasarlos a **GetAttachment**.
  
> [!NOTE]
> El identificador de los datos adjuntos y la clave de cambio se han abreviado para preservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [GetAttachment](getattachment.md)
    
- [AttachmentShape](attachmentshape.md)
    
- [Identificadores](attachmentids.md)
    
- [AttachmentId (GetAttachment y DeleteAttachment)](attachmentid-getattachment-and-deleteattachment.md)
    
## <a name="getattachment-response-example"></a>Ejemplo de respuesta GetAttachment

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud GetAttachment. En este ejemplo se devuelven datos adjuntos de archivo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="662" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <GetAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                           xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                           xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

Los mensajes de respuesta para GetAttachment siempre contendrán los datos adjuntos completos; es decir, siempre se incluirán todas las propiedades. Para los datos adjuntos, esas propiedades son [Name (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [contentid](contentid.md), [ContentLocation](contentlocation.md)y [Content](content.md). Para los datos adjuntos de elementos, esas propiedades son [nombre (AttachmentType)](name-attachmenttype.md), [ContentType](contenttype.md), [contentid](contentid.md), [ContentLocation](contentlocation.md) y todas las propiedades del elemento, como si la forma **AllProperties** se hubiera usado en una llamada GetItem. El elemento [AttachmentShape](attachmentshape.md) , si está presente, permitirá que una aplicación de consumidor solicite propiedades extendidas adicionales para los datos adjuntos de elementos. 
  
### <a name="successful-response-elements"></a>Elementos Response correcto

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
    
- [Content](content.md)
    
## <a name="see-also"></a>Vea también



[Operación CreateAttachment](createattachment-operation.md)
  
[Operación DeleteAttachment](deleteattachment-operation.md)

