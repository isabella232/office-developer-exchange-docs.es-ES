---
title: Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)
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
description: La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que la mensajería unificada va a leer los mensajes al usuario por teléfono.
ms.openlocfilehash: a2bb630f812ca811b4cbe68db1308dc18e5d3ba0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467336"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a>Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)

La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que la mensajería unificada va a leer los mensajes al usuario por teléfono.
  
## <a name="settelephoneaccessfolderemail-request-example"></a>Ejemplo de solicitud SetTelephoneAccessFolderEmail

### <a name="description"></a>Description

En el siguiente ejemplo de una solicitud de SetTelephoneAccessFolderEmail se muestra cómo realizar una solicitud para establecer la carpeta desde la que se leerá la mensajería unificada al usuario por teléfono.
  
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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a>Ejemplo de respuesta SetTelephoneAccessFolderEmail correcta

### <a name="description"></a>Description

El siguiente ejemplo de una respuesta de SetTelephoneAccessFolderEmail muestra una respuesta a la solicitud SetTelephoneAccessFolderEmail.
  
### <a name="code"></a>Código

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Vea también



[SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)](settelephoneaccessfolderemail-um-web-service.md)
  
[SetTelephoneAccessFolderEmailResponse (servicio Web de mensajería unificada)](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[base64FolderId (servicio Web de mensajería unificada)](base64folderid-um-web-service.md)

