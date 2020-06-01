---
title: Operación DeleteUserConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteUserConfiguration
api_type:
- schema
ms.assetid: 93e44690-be2d-4fdb-96a8-4ded3c193aed
description: La operación DeleteUserConfiguration elimina un objeto de configuración de usuario en una carpeta.
ms.openlocfilehash: 064e1ace2c2f51783431ce42670b2a4fd8146b54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44451470"
---
# <a name="deleteuserconfiguration-operation"></a><span data-ttu-id="39511-103">Operación DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="39511-103">DeleteUserConfiguration operation</span></span>

<span data-ttu-id="39511-104">La operación **DeleteUserConfiguration** elimina un objeto de configuración de usuario en una carpeta.</span><span class="sxs-lookup"><span data-stu-id="39511-104">The **DeleteUserConfiguration** operation deletes a user configuration object on a folder.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="39511-105">La operación **DeleteUserConfiguration** desencadenará un evento Move para el sistema de notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="39511-105">The **DeleteUserConfiguration** operation will trigger a move event for the event notification system.</span></span> <span data-ttu-id="39511-106">El objeto de configuración de usuario se moverá al contenedor.</span><span class="sxs-lookup"><span data-stu-id="39511-106">The user configuration object will be moved to the dumpster.</span></span> 
  
## <a name="deleteuserconfiguration-request-example"></a><span data-ttu-id="39511-107">Ejemplo de solicitud DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="39511-107">DeleteUserConfiguration request example</span></span>

### <a name="description"></a><span data-ttu-id="39511-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="39511-108">Description</span></span>

<span data-ttu-id="39511-109">El siguiente ejemplo de una solicitud **DeleteUserConfiguration** muestra cómo crear una solicitud para eliminar un objeto de configuración de usuario de la carpeta Borradores.</span><span class="sxs-lookup"><span data-stu-id="39511-109">The following example of a **DeleteUserConfiguration** request shows how to form a request to delete a user configuration object on the Drafts folder.</span></span> 
  
### <a name="code"></a><span data-ttu-id="39511-110">Código</span><span class="sxs-lookup"><span data-stu-id="39511-110">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2010" />
  </soap:Header>
  <soap:Body>
    <m:DeleteUserConfiguration>
      <m:UserConfigurationName Name="TestConfig">
        <t:DistinguishedFolderId Id="drafts"/>
      </m:UserConfigurationName>
    </m:DeleteUserConfiguration>
  </soap:Body>
</soap:Envelope>
```

## <a name="deleteuserconfiguration-response-example"></a><span data-ttu-id="39511-111">Ejemplo de respuesta DeleteUserConfiguration</span><span class="sxs-lookup"><span data-stu-id="39511-111">DeleteUserConfiguration response example</span></span>

### <a name="description"></a><span data-ttu-id="39511-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="39511-112">Description</span></span>

<span data-ttu-id="39511-113">En el ejemplo siguiente se muestra una respuesta correcta a la solicitud **DeleteUserConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="39511-113">The following example shows a successful response to the **DeleteUserConfiguration** request.</span></span> 
  
### <a name="code"></a><span data-ttu-id="39511-114">Código</span><span class="sxs-lookup"><span data-stu-id="39511-114">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="14" 
                         MinorVersion="0" 
                         MajorBuildNumber="639" 
                         MinorBuildNumber="20" 
                         Version="Exchange2010" 
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"/>
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:DeleteUserConfigurationResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:DeleteUserConfigurationResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:DeleteUserConfigurationResponseMessage>
      </m:ResponseMessages>
    </m:DeleteUserConfigurationResponse>
  </s:Body>
</s:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="39511-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="39511-115">See also</span></span>

- [<span data-ttu-id="39511-116">Operaciones de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="39511-116">EWS operations in Exchange</span></span>](ews-operations-in-exchange.md) 
- [<span data-ttu-id="39511-117">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="39511-117">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

