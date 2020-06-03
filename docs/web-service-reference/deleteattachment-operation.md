---
title: Operación DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: La operación DeleteAttachment se usa para eliminar archivos y datos adjuntos de un elemento existente en el almacén de Exchange.
ms.openlocfilehash: 1d34ce4c5ba1d955989a35dafb8ab3c5d229d505
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457336"
---
# <a name="deleteattachment-operation"></a>Operación DeleteAttachment

La operación DeleteAttachment se usa para eliminar archivos y datos adjuntos de un elemento existente en el almacén de Exchange.
  
## <a name="remarks"></a>Comentarios

Esta operación permite eliminar uno o más datos adjuntos por identificador.
  
## <a name="deleteattachment-request-example"></a>Ejemplo de solicitud DeleteAttachment

### <a name="description"></a>Description

El siguiente ejemplo de una solicitud DeleteAttachment muestra cómo eliminar un elemento adjunto.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="https://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El identificador de datos adjuntos se ha abreviado para preservar la legibilidad.
  
### <a name="request-elements"></a>Elementos de solicitud

Los siguientes elementos se usan en la solicitud:
  
- [DeleteAttachment](deleteattachment.md)
    
- [Identificadores](attachmentids.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a>Ejemplo de respuesta DeleteAttachment

### <a name="description"></a>Description

En el ejemplo siguiente se muestra una respuesta correcta a una solicitud DeleteAttachment.
  
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
    <DeleteAttachmentResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:DeleteAttachmentResponseMessage xsi:type="m:DeleteAttachmentResponseMessageType" ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootItemId RootItemId="AAAtAEFkbWluaXN..." RootItemChangeKey="CQAAABYAA..."/>
        </m:DeleteAttachmentResponseMessage>
      </m:ResponseMessages>
    </DeleteAttachmentResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

La operación CreateAttachment devuelve un elemento de tipo AttachmentIdType que incluye un **RootItemId** y **RootItemChangeKey**. Estos atributos no se permiten para los identificadores dentro de una solicitud DeleteAttachment. DeleteAttachment usa elementos de tipo RequestAttachmentIdType, que no incluyen estos atributos.
  
La respuesta DeleteAttachment incluye el identificador del elemento primario. Cuando se quitan datos adjuntos de un elemento, se modifica la clave de cambio del elemento. La nueva clave de cambio de elemento se puede obtener de la respuesta DeleteAttachment.
  
> [!NOTE]
> El identificador [RootItemId](rootitemid.md) y changekey se han abreviado para preservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos Response correcto

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteAttachmentResponse](deleteattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootItemId](rootitemid.md)
    
## <a name="see-also"></a>Vea también

- [Operación CreateAttachment](createattachment-operation.md) 
- [Operación GetAttachment](getattachment-operation.md)

