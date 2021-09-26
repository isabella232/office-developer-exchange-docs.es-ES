---
title: Operación DeleteAttachment
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeleteAttachment
api_type:
- schema
ms.assetid: 4d48e595-b98c-48e7-bbeb-cacf91d12a78
description: La operación DeleteAttachment se usa para eliminar datos adjuntos de archivos y elementos de un elemento existente en el Exchange almacén.
ms.openlocfilehash: bd08776e1f4e75204819ef5463e297e3770a34a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546689"
---
# <a name="deleteattachment-operation"></a>Operación DeleteAttachment

La operación DeleteAttachment se usa para eliminar datos adjuntos de archivos y elementos de un elemento existente en el Exchange almacén.
  
## <a name="remarks"></a>Comentarios

Esta operación permite eliminar uno o varios datos adjuntos por identificador.
  
## <a name="deleteattachment-request-example"></a>Ejemplo de solicitud DeleteAttachment

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud DeleteAttachment se muestra cómo eliminar los datos adjuntos de un elemento.
  
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

El identificador de datos adjuntos se ha acortado para conservar la legibilidad.
  
### <a name="request-elements"></a>Elementos Request

En la solicitud se usan los siguientes elementos:
  
- [DeleteAttachment](deleteattachment.md)
    
- [AttachmentIds](attachmentids.md)
    
- [AttachmentId](attachmentid.md)
    
## <a name="deleteattachment-response-example"></a>Ejemplo de respuesta DeleteAttachment

### <a name="description"></a>Description

En el siguiente ejemplo se muestra una respuesta correcta a una solicitud DeleteAttachment.
  
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

La operación CreateAttachment devuelve un elemento del tipo AttachmentIdType que incluye **rootitemid** y **rootitemchangekey**. Estos atributos no están permitidos para identificadores dentro de una solicitud DeleteAttachment. DeleteAttachment usa elementos del tipo RequestAttachmentIdType, que no incluye estos atributos.
  
La respuesta DeleteAttachment incluye el identificador del elemento primario. Cuando se quitan datos adjuntos de un elemento, se modifica la clave de cambio del elemento. La nueva clave de cambio de elemento se puede obtener de la respuesta DeleteAttachment.
  
> [!NOTE]
> El [identificador RootItemId](rootitemid.md) y ChangeKey se han acortado para conservar la legibilidad. 
  
### <a name="successful-response-elements"></a>Elementos de respuesta correctos

En la respuesta se usan los siguientes elementos:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [DeleteAttachmentResponse](deleteattachmentresponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [DeleteAttachmentResponseMessage](deleteattachmentresponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [RootItemId](rootitemid.md)
    
## <a name="see-also"></a>Consulte también

- [Operación CreateAttachment](createattachment-operation.md) 
- [Operación GetAttachment](getattachment-operation.md)

