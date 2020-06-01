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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467336"
---
# <a name="settelephoneaccessfolderemail-operation-um-web-service"></a><span data-ttu-id="00e13-103">Operación SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="00e13-103">SetTelephoneAccessFolderEmail operation (UM web service)</span></span>

<span data-ttu-id="00e13-104">La operación SetTelephoneAccessFolderEmail establece la carpeta desde la que la mensajería unificada va a leer los mensajes al usuario por teléfono.</span><span class="sxs-lookup"><span data-stu-id="00e13-104">The SetTelephoneAccessFolderEmail operation sets the folder from which Unified Messaging will read back messages to the user over the telephone.</span></span>
  
## <a name="settelephoneaccessfolderemail-request-example"></a><span data-ttu-id="00e13-105">Ejemplo de solicitud SetTelephoneAccessFolderEmail</span><span class="sxs-lookup"><span data-stu-id="00e13-105">SetTelephoneAccessFolderEmail request example</span></span>

### <a name="description"></a><span data-ttu-id="00e13-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="00e13-106">Description</span></span>

<span data-ttu-id="00e13-107">En el siguiente ejemplo de una solicitud de SetTelephoneAccessFolderEmail se muestra cómo realizar una solicitud para establecer la carpeta desde la que se leerá la mensajería unificada al usuario por teléfono.</span><span class="sxs-lookup"><span data-stu-id="00e13-107">The following example of a SetTelephoneAccessFolderEmail request shows how to form a request to set the folder from which Unified Messaging will read back to the user over the telephone.</span></span>
  
### <a name="code"></a><span data-ttu-id="00e13-108">Código</span><span class="sxs-lookup"><span data-stu-id="00e13-108">Code</span></span>

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

## <a name="successful-settelephoneaccessfolderemail-response-example"></a><span data-ttu-id="00e13-109">Ejemplo de respuesta SetTelephoneAccessFolderEmail correcta</span><span class="sxs-lookup"><span data-stu-id="00e13-109">Successful SetTelephoneAccessFolderEmail response example</span></span>

### <a name="description"></a><span data-ttu-id="00e13-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="00e13-110">Description</span></span>

<span data-ttu-id="00e13-111">El siguiente ejemplo de una respuesta de SetTelephoneAccessFolderEmail muestra una respuesta a la solicitud SetTelephoneAccessFolderEmail.</span><span class="sxs-lookup"><span data-stu-id="00e13-111">The following example of a SetTelephoneAccessFolderEmail response shows a response to the SetTelephoneAccessFolderEmail request.</span></span>
  
### <a name="code"></a><span data-ttu-id="00e13-112">Código</span><span class="sxs-lookup"><span data-stu-id="00e13-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetTelephoneAccessFolderEmailResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="00e13-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="00e13-113">See also</span></span>



[<span data-ttu-id="00e13-114">SetTelephoneAccessFolderEmail (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="00e13-114">SetTelephoneAccessFolderEmail (UM web service)</span></span>](settelephoneaccessfolderemail-um-web-service.md)
  
[<span data-ttu-id="00e13-115">SetTelephoneAccessFolderEmailResponse (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="00e13-115">SetTelephoneAccessFolderEmailResponse (UM web service)</span></span>](settelephoneaccessfolderemailresponse-um-web-service.md)
  
[<span data-ttu-id="00e13-116">base64FolderId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="00e13-116">base64FolderId (UM web service)</span></span>](base64folderid-um-web-service.md)

