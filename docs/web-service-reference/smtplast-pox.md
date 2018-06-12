---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: El elemento SMTPLast especifica si el servidor de Protocolo Simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.
ms.openlocfilehash: 5359f20b33855f4ef48566058bc46bd618e3b2ff
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837505"
---
# <a name="smtplast-pox"></a><span data-ttu-id="f45b7-103">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-103">SMTPLast (POX)</span></span>

<span data-ttu-id="f45b7-104">El elemento **SMTPLast** especifica si el servidor de Protocolo Simple de transferencia de correo (SMTP) requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.</span><span class="sxs-lookup"><span data-stu-id="f45b7-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="f45b7-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="f45b7-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="f45b7-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="f45b7-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="f45b7-109">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f45b7-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f45b7-110">Attributes and elements</span></span>

<span data-ttu-id="f45b7-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f45b7-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f45b7-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f45b7-112">Attributes</span></span>

<span data-ttu-id="f45b7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f45b7-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f45b7-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f45b7-114">Child elements</span></span>

<span data-ttu-id="f45b7-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f45b7-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f45b7-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f45b7-116">Parent elements</span></span>

|<span data-ttu-id="f45b7-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f45b7-117">**Element**</span></span>|<span data-ttu-id="f45b7-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f45b7-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f45b7-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="f45b7-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="f45b7-120">Contiene las especificaciones para conectar a un cliente en el equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="f45b7-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f45b7-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f45b7-121">Text value</span></span>

<span data-ttu-id="f45b7-122">El valor de texto especifica si el servidor SMTP requiere que el correo electrónico se descargue antes de enviar correo electrónico mediante el servidor SMTP.</span><span class="sxs-lookup"><span data-stu-id="f45b7-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="f45b7-123">Los valores posibles son **encendido** y **apagado**.</span><span class="sxs-lookup"><span data-stu-id="f45b7-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="f45b7-124">El valor predeterminado es **desactivado**.</span><span class="sxs-lookup"><span data-stu-id="f45b7-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f45b7-125">Ver también</span><span class="sxs-lookup"><span data-stu-id="f45b7-125">See also</span></span>

- [<span data-ttu-id="f45b7-126">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f45b7-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

