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
description: La operación DeleteAttachment se usa para eliminar los datos adjuntos de archivo y elemento de un elemento existente en el almacén de Exchange.
ms.openlocfilehash: 4b94bfd8d6333c1f52be8ad7d0d111ab2a0552b3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764080"
---
# <a name="deleteattachment-operation"></a>Operación DeleteAttachment

La operación DeleteAttachment se usa para eliminar los datos adjuntos de archivo y elemento de un elemento existente en el almacén de Exchange.
  
## <a name="remarks"></a>Comentarios

Esta operación le permite eliminar uno o varios datos adjuntos por Id.
  
## <a name="deleteattachment-request-example"></a>Ejemplo de solicitud DeleteAttachment

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de DeleteAttachment muestra cómo eliminar un elemento de datos adjuntos.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:xsd="http://www.w3.org/2001/XMLSchema"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <DeleteAttachment xmlns="http://schemas.microsoft.com/exchange/services/2006/messages"
                      xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <AttachmentIds>
        <t:AttachmentId Id="AAAtAEFkbWluaX"/>
      </AttachmentIds>
    </DeleteAttachment>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comentarios

El identificador de datos adjuntos se ha acortado para conservar la legibilidad.
  
### <a name="request-elements"></a>Elementos de solicitud

En la solicitud se usan los siguientes elementos:
  
- [DeleteAttachment](deleteattachment.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a>Ejemplo de respuesta DeleteAttachment

### <a name="description"></a>Descripción

En el ejemplo siguiente se muestra una respuesta a una solicitud de DeleteAttachment correcta.
  
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
    <DeleteAttachmentResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                              xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

La operación CreateAttachment devuelve un elemento de tipo AttachmentIdType que incluya un **RootItemId** y **RootItemChangeKey**. Estos atributos no están permitidos para los identificadores dentro de una solicitud de DeleteAttachment. DeleteAttachment utiliza elementos de tipo RequestAttachmentIdType, que no incluye estos atributos.
  
La respuesta DeleteAttachment incluye el identificador del elemento primario. Cuando se quitan los datos adjuntos de un elemento, se modifica la clave del elemento cambio. La respuesta DeleteAttachment puede obtenerse la nueva clave de cambio de elemento.
  
> [!NOTE]
> El identificador de [RootItemId](rootitemid.md) y ChangeKey se han abreviado para conservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos de respuesta correcta

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

