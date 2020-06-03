---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: El elemento SmtpAddress contiene la dirección SMTP asignada al almacén de mensajes de carpeta pública configurado para el usuario.
ms.openlocfilehash: 48703a11fb056967c6c76073c2e928d5f6efa264
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468645"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="7cc5b-103">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="7cc5b-104">El elemento **SmtpAddress** contiene la dirección SMTP asignada al almacén de mensajes de carpeta pública configurado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="7cc5b-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="7cc5b-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="7cc5b-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="7cc5b-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="7cc5b-109">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="7cc5b-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7cc5b-110">Attributes and elements</span></span>

<span data-ttu-id="7cc5b-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7cc5b-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="7cc5b-112">Attributes</span></span>

<span data-ttu-id="7cc5b-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7cc5b-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7cc5b-114">Child elements</span></span>

<span data-ttu-id="7cc5b-115">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="7cc5b-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7cc5b-116">Parent elements</span></span>

|<span data-ttu-id="7cc5b-117">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="7cc5b-117">**Element**</span></span>|<span data-ttu-id="7cc5b-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7cc5b-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7cc5b-119">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="7cc5b-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="7cc5b-120">Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7cc5b-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7cc5b-121">Text value</span></span>

<span data-ttu-id="7cc5b-122">El valor de texto representa la dirección SMTP asignada al almacén de carpetas públicas configurado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="7cc5b-123">Esta dirección SMTP puede usarse en el elemento [EmailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de las carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="7cc5b-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7cc5b-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="7cc5b-124">Remarks</span></span>

<span data-ttu-id="7cc5b-125">El elemento **SmtpAddress** es un elemento secundario necesario del elemento **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="7cc5b-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7cc5b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7cc5b-126">See also</span></span>

- [<span data-ttu-id="7cc5b-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="7cc5b-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

