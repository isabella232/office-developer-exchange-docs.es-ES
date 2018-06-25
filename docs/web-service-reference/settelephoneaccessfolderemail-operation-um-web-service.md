---
title: Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetTelephoneAccessFolderEmail
api_type:
- schema
ms.assetid: 2c92d914-bdee-4337-b3ea-0655fdb658e9
description: La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que mensajería unificada leerá atrás mensajes al usuario a través del teléfono.
ms.openlocfilehash: 9497e58f66b8efcf7e358aa529223942298a3bed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837459"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>Operación SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)

La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que mensajería unificada leerá atrás mensajes al usuario a través del teléfono.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>Ejemplo de solicitud de SetTelephoneAccessFolderEmail

### <a name="description"></a>Descripción

El siguiente ejemplo de una solicitud de SetTelephoneAccessFolderEmail muestra cómo formar una solicitud para establecer la carpeta desde la que va a mensajería unificada leer al usuario a través del teléfono.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetTelephoneAccessFolderEmail xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <base64FolderID>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</base64FolderID>
    </SetTelephoneAccessFolderEmail>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Ejemplo de respuesta correcta de SetTelephoneAccessFolderEmail

### <a name="description"></a>Descripción

El siguiente ejemplo de una respuesta SetTelephoneAccessFolderEmail muestra una respuesta a la solicitud de SetTelephoneAccessFolderEmail.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetTelephoneAccessFolderEmail (servicio web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (servicio web de mensajería unificada)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (servicio web de mensajería unificada)](base64folderid-um-web-service.md)

