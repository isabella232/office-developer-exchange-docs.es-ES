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
description: El elemento SMTPLast especifica si el servidor de Protocolo simple de transferencia de correo (SMTP) requiere que se descargue el correo electrónico antes de enviar correo electrónico mediante el servidor SMTP.
ms.openlocfilehash: 7019da28ffa196a9abc8798aa75aff2756198da3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468435"
---
# <a name="smtplast-pox"></a><span data-ttu-id="8b1d3-103">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-103">SMTPLast (POX)</span></span>

<span data-ttu-id="8b1d3-104">El elemento **SMTPLast** especifica si el servidor de Protocolo simple de transferencia de correo (SMTP) requiere que se descargue el correo electrónico antes de enviar correo electrónico mediante el servidor SMTP.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-104">The **SMTPLast** element specifies whether the Simple Mail Transfer Protocol (SMTP) server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> 
  
- [<span data-ttu-id="8b1d3-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="8b1d3-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="8b1d3-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="8b1d3-108">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-108">Protocol (POX)</span></span>](protocol-pox.md)
  
- [<span data-ttu-id="8b1d3-109">SMTPLast (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-109">SMTPLast (POX)</span></span>](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="8b1d3-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8b1d3-110">Attributes and elements</span></span>

<span data-ttu-id="8b1d3-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8b1d3-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="8b1d3-112">Attributes</span></span>

<span data-ttu-id="8b1d3-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8b1d3-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8b1d3-114">Child elements</span></span>

<span data-ttu-id="8b1d3-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8b1d3-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8b1d3-116">Parent elements</span></span>

|<span data-ttu-id="8b1d3-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="8b1d3-117">**Element**</span></span>|<span data-ttu-id="8b1d3-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8b1d3-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8b1d3-119">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="8b1d3-119">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="8b1d3-120">Contiene las especificaciones para conectar un cliente al equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-120">Contains the specifications for connecting a client to the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8b1d3-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8b1d3-121">Text value</span></span>

<span data-ttu-id="8b1d3-122">El valor de texto especifica si el servidor SMTP requiere que se descargue el correo electrónico antes de enviar correo electrónico mediante el servidor SMTP.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-122">The text value specifies whether the SMTP server requires that e-mail be downloaded before it sends e-mail by using the SMTP server.</span></span> <span data-ttu-id="8b1d3-123">Los valores posibles son **activado** y **desactivado**.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-123">The possible values are **on** and **off**.</span></span> <span data-ttu-id="8b1d3-124">El valor predeterminado es **OFF**.</span><span class="sxs-lookup"><span data-stu-id="8b1d3-124">The default value is **off**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b1d3-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b1d3-125">See also</span></span>

- [<span data-ttu-id="8b1d3-126">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="8b1d3-126">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

