---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: El elemento PublicFolderInformation contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.
ms.openlocfilehash: bb4432a664024c3d1ccb17826948cfe7a1b58cdf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836927"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="6d1bd-103">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="6d1bd-104">El elemento **PublicFolderInformation** contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="6d1bd-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="6d1bd-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="6d1bd-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="6d1bd-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="6d1bd-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d1bd-109">Attributes and elements</span></span>

<span data-ttu-id="6d1bd-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d1bd-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d1bd-111">Attributes</span></span>

<span data-ttu-id="6d1bd-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d1bd-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d1bd-113">Child elements</span></span>

|<span data-ttu-id="6d1bd-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d1bd-114">**Element**</span></span>|<span data-ttu-id="6d1bd-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d1bd-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d1bd-116">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="6d1bd-117">Contiene la dirección SMTP asignada a la tienda de mensaje de carpeta pública configurada para el usuario.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="6d1bd-118">Esta dirección SMTP puede utilizarse en el elemento [EMailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="6d1bd-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d1bd-119">Parent elements</span></span>

|<span data-ttu-id="6d1bd-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="6d1bd-120">**Element**</span></span>|<span data-ttu-id="6d1bd-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6d1bd-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6d1bd-122">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="6d1bd-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="6d1bd-123">Especifica la configuración de cuenta para el usuario.</span><span class="sxs-lookup"><span data-stu-id="6d1bd-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d1bd-124">Notas</span><span class="sxs-lookup"><span data-stu-id="6d1bd-124">Remarks</span></span>

<span data-ttu-id="6d1bd-125">El elemento **PublicFolderInformation** es un elemento secundario opcional del elemento de **cuenta** .</span><span class="sxs-lookup"><span data-stu-id="6d1bd-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6d1bd-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="6d1bd-126">See also</span></span>



[<span data-ttu-id="6d1bd-127">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="6d1bd-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

