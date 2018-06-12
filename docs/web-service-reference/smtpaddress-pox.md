---
title: SmtpAddress (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 984ccd97-c337-47b6-ba42-3405a8b55a71
description: El elemento SmtpAddress contiene la dirección SMTP asignada a la tienda de mensaje de carpeta pública configurada para el usuario.
ms.openlocfilehash: 43ebb328e31cdec11412e80b743d4d4393b7960a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837507"
---
# <a name="smtpaddress-pox"></a><span data-ttu-id="f1e2d-103">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-103">SmtpAddress (POX)</span></span>

<span data-ttu-id="f1e2d-104">El elemento **SmtpAddress** contiene la dirección SMTP asignada a la tienda de mensaje de carpeta pública configurada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-104">The **SmtpAddress** element contains the SMTP address assigned to the public folder message store configured for the user.</span></span> 
  
- [<span data-ttu-id="f1e2d-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="f1e2d-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="f1e2d-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-107">Account (POX)</span></span>](account-pox.md)
  
- [<span data-ttu-id="f1e2d-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
- [<span data-ttu-id="f1e2d-109">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-109">SmtpAddress (POX)</span></span>](smtpaddress-pox.md)
  
```XML
<SmtpAddress/>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="f1e2d-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="f1e2d-110">Attributes and elements</span></span>

<span data-ttu-id="f1e2d-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1e2d-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="f1e2d-112">Attributes</span></span>

<span data-ttu-id="f1e2d-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1e2d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="f1e2d-114">Child elements</span></span>

<span data-ttu-id="f1e2d-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f1e2d-116">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="f1e2d-116">Parent elements</span></span>

|<span data-ttu-id="f1e2d-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1e2d-117">**Element**</span></span>|<span data-ttu-id="f1e2d-118">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f1e2d-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1e2d-119">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="f1e2d-119">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="f1e2d-120">Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-120">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f1e2d-121">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="f1e2d-121">Text value</span></span>

<span data-ttu-id="f1e2d-122">El valor de texto representa la dirección SMTP asignada a la tienda de carpeta pública configurada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-122">The text value represents the SMTP address assigned to the public folder store configured for the user.</span></span> <span data-ttu-id="f1e2d-123">Esta dirección SMTP puede utilizarse en el elemento [EMailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="f1e2d-123">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f1e2d-124">Notas</span><span class="sxs-lookup"><span data-stu-id="f1e2d-124">Remarks</span></span>

<span data-ttu-id="f1e2d-125">El elemento **SmtpAddress** es un elemento secundario necesario del elemento **PublicFolderInformation** .</span><span class="sxs-lookup"><span data-stu-id="f1e2d-125">The **SmtpAddress** element is a required child element of the **PublicFolderInformation** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1e2d-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="f1e2d-126">See also</span></span>

- [<span data-ttu-id="f1e2d-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="f1e2d-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

