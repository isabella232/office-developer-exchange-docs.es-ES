---
title: Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que la mensajería unificada leerá los mensajes al usuario por teléfono.
ms.openlocfilehash: cf8e80e021d6467ba3a724cc0d04e165e00e8397
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544720"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)

La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que la mensajería unificada leerá los mensajes al usuario por teléfono.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>Ejemplo de solicitud SetTelephoneAccessFolderEmail

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud SetTelephoneAccessFolderEmail se muestra cómo formar una solicitud para establecer la carpeta desde la que la mensajería unificada leerá de nuevo al usuario por teléfono.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Ejemplo de respuesta SetTelephoneAccessFolderEmail correcto

### <a name="description"></a>Description

En el siguiente ejemplo de una respuesta SetTelephoneAccessFolderEmail se muestra una respuesta a la solicitud SetTelephoneAccessFolderEmail.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Consulte también



[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (servicio web de mensajería unificada)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (servicio web de mensajería unificada)](base64folderid-um-web-service.md)

