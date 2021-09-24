---
title: Operación CreateAttachment
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
ms.assetid: e066db95-6963-4507-a8d0-8efad287f550
description: La operación CreateAttachment crea un elemento o datos adjuntos de archivo y lo adjunta al elemento especificado.
ms.openlocfilehash: 0c75e8c73bf4352e2703a6ca6ac06e261e8f37c9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511884"
---
# <a name="createattachment-operation"></a>Operación CreateAttachment

La operación CreateAttachment crea un elemento o datos adjuntos de archivo y lo adjunta al elemento especificado.
  
## <a name="file-createattachment-request-example"></a>Ejemplo de solicitud CreateAttachment de archivo

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud CreateAttachment se muestra cómo crear datos adjuntos de archivo.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
<soap:Body>
  <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                    xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
    <ParentItemId Id="AAAtAE..." ChangeKey="CQAAABYA..."/>
    <Attachments>
      <t:FileAttachment>
        <t:Name>SomeFile</t:Name>
        <t:Content>AQIDBAU=</t:Content>
      </t:FileAttachment>
    </Attachments>
  </CreateAttachment>
</soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comentario

Se debe proporcionar un nombre para los datos adjuntos.
  
> [!NOTE]
> El identificador del elemento primario y la clave de cambio se han acortado para conservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [Adjuntos](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Contenido](content.md)
    
## <a name="successful-file-createattachment-response-example"></a>Ejemplo de respuesta CreateAttachment de archivo correcto

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateAttachment.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:FileAttachment>
              <t:AttachmentId Id="AAAtAE=" RootItemId="AAAtAEFk=" RootItemChangeKey="CQAAAB"/>
            </t:FileAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comentario

La respuesta contiene el identificador del archivo adjunto. También contiene el identificador y la clave de cambio del elemento raíz. Los identificadores de elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Adjuntos](attachments-ex15websvcsotherref.md)
    
- [FileAttachment](fileattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="item-createattachment-request-example"></a>Ejemplo de solicitud CreateAttachment item

### <a name="description"></a>Descripción

En el siguiente ejemplo de una solicitud CreateAttachment se muestra cómo crear datos adjuntos de elementos.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <CreateAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <ParentItemId Id="AAAtAE=" ChangeKey="CQAAABYA"/>
      <Attachments>
        <t:ItemAttachment>
          <t:Name>An item attachment</t:Name>
          <t:Message>
            <t:Subject>A message to attach</t:Subject>
          </t:Message>
        </t:ItemAttachment>
      </Attachments>
    </CreateAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comentario

Se debe proporcionar un nombre para los datos adjuntos.
  
 **Nota** El identificador del elemento primario y la clave de cambio se han acortado para conservar la legibilidad. 
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [CreateAttachment](createattachment.md)
    
- [ParentItemId](parentitemid.md)
    
- [Adjuntos](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [Name (AttachmentType)](name-attachmenttype.md)
    
- [Mensaje](message-ex15websvcsotherref.md)
    
- [Asunto](subject.md)
    
## <a name="successful-item-createattachment-response-example"></a>Ejemplo de respuesta CreateAttachment de elemento correcto

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta correcta a la solicitud CreateAttachment.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Attachments>
            <t:ItemAttachment>
              <t:AttachmentId Id="AAAtAEFk=" RootItemId="AAAtAEFkb=" RootItemChangeKey="CQAAABYA"/>
            </t:ItemAttachment>
          </m:Attachments>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comment"></a>Comentario

La respuesta contiene el identificador de los nuevos datos adjuntos. También contiene el identificador y la clave de cambio del elemento raíz. El elemento raíz es el elemento que contiene los datos adjuntos. Los identificadores de elemento y la clave de cambio se han acortado para conservar la legibilidad.
  
### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Adjuntos](attachments-ex15websvcsotherref.md)
    
- [ItemAttachment](itemattachment.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="createattachment-error-response-example"></a>Ejemplo de respuesta de error CreateAttachment

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta de error a la solicitud CreateAttachment. El error se debe a que no se especificó el nombre de los datos adjuntos.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="653" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"/>
  </soap:Header>
  <soap:Body>
    <CreateAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:CreateAttachmentResponseMessage ResponseClass="Error">
          <m:MessageText>Required property is missing.</m:MessageText>
          <m:ResponseCode>ErrorRequiredPropertyMissing</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
          <m:MessageXml>
            <t:ExceptionFieldURI FieldURI="attachment:Name"/>
          </m:MessageXml>
          <m:Attachments/>
        </m:CreateAttachmentResponseMessage>
      </m:ResponseMessages>
    </CreateAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="error-response-elements"></a>Elementos de respuesta de error

En la respuesta de error se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [CreateAttachmentResponse](createattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [CreateAttachmentResponseMessage](createattachmentresponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
- [MessageXml](messagexml.md)
    
- [ExceptionFieldURI](exceptionfielduri.md)
    
- [Adjuntos](attachments-ex15websvcsotherref.md)
    
## <a name="remarks"></a>Comentarios

Si se adjuntan varios datos adjuntos a un elemento en un solo recorrido de ida y vuelta, RootItemChangeKey en el último mensaje de respuesta es el que representa la nueva clave de cambio del elemento que tiene los datos adjuntos.
  
## <a name="see-also"></a>Ver también



[Operación DeleteAttachment](deleteattachment-operation.md)
  
[Operación GetAttachment](getattachment-operation.md)

