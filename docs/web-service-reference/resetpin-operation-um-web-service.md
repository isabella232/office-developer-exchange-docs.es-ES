---
title: Operación ResetPIN (servicio web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: La operación ResetPIN cambia el PIN (contraseña TUI) a un nuevo valor aleatorio.
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19837146"
---
# <a name="resetpin-operation-um-web-service"></a><span data-ttu-id="4fef3-103">Operación ResetPIN (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="4fef3-103">ResetPIN operation (UM web service)</span></span>

<span data-ttu-id="4fef3-104">La operación ResetPIN cambia el PIN (contraseña TUI) a un nuevo valor aleatorio.</span><span class="sxs-lookup"><span data-stu-id="4fef3-104">The ResetPIN operation changes the PIN (TUI password) to a new random value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fef3-105">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4fef3-105">Remarks</span></span>

<span data-ttu-id="4fef3-106">La operación ResetPIN crea un nuevo NIP en función de las directivas de PIN.</span><span class="sxs-lookup"><span data-stu-id="4fef3-106">The ResetPIN operation creates a new PIN based on the PIN policies.</span></span> <span data-ttu-id="4fef3-107">Si la operación se realiza correctamente, se envía un mensaje de correo electrónico que contiene el nuevo NIP para el buzón de correo del usuario.</span><span class="sxs-lookup"><span data-stu-id="4fef3-107">If the operation is successful, an e-mail message that contains the new PIN is sent to the mailbox of the user.</span></span> <span data-ttu-id="4fef3-108">Si se produce un error en la operación, producirá una excepción que contiene información sobre el error.</span><span class="sxs-lookup"><span data-stu-id="4fef3-108">If the operation fails, it will throw an exception that contains information about the failure.</span></span>
  
## <a name="resetpin-request-example"></a><span data-ttu-id="4fef3-109">Ejemplo de solicitud de ResetPIN</span><span class="sxs-lookup"><span data-stu-id="4fef3-109">ResetPIN request example</span></span>

### <a name="description"></a><span data-ttu-id="4fef3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fef3-110">Description</span></span>

<span data-ttu-id="4fef3-111">El siguiente ejemplo de una solicitud de ResetPIN muestra cómo formar una solicitud para restablecer el NIP de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="4fef3-111">The following example of a ResetPIN request shows how to form a request to reset the PIN for a mailbox.</span></span>
  
### <a name="code"></a><span data-ttu-id="4fef3-112">Código</span><span class="sxs-lookup"><span data-stu-id="4fef3-112">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a><span data-ttu-id="4fef3-113">Ejemplo de respuesta correcta de ResetPIN</span><span class="sxs-lookup"><span data-stu-id="4fef3-113">Successful ResetPIN response example</span></span>

### <a name="description"></a><span data-ttu-id="4fef3-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4fef3-114">Description</span></span>

<span data-ttu-id="4fef3-115">El siguiente ejemplo de una respuesta ResetPIN muestra una respuesta a la solicitud de ResetPIN.</span><span class="sxs-lookup"><span data-stu-id="4fef3-115">The following example of a ResetPIN response shows a response to the ResetPIN request.</span></span>
  
### <a name="code"></a><span data-ttu-id="4fef3-116">Código</span><span class="sxs-lookup"><span data-stu-id="4fef3-116">Code</span></span>

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a><span data-ttu-id="4fef3-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fef3-117">See also</span></span>



[<span data-ttu-id="4fef3-118">ResetPIN (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="4fef3-118">ResetPIN (UM web service)</span></span>](resetpin-um-web-service.md)
  
[<span data-ttu-id="4fef3-119">ResetPINResponse (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="4fef3-119">ResetPINResponse (UM web service)</span></span>](resetpinresponse-um-web-service.md)

