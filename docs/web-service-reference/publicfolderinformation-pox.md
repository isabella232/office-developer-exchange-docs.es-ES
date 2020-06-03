---
title: PublicFolderInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a221aa9e-b4ac-4ec5-aa42-7e2a69e8eaa6
description: El elemento PublicFolderInformation contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.
ms.openlocfilehash: e044a1feddfaeb4eb93c289c617dde9adc66f332
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457721"
---
# <a name="publicfolderinformation-pox"></a><span data-ttu-id="64c09-103">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-103">PublicFolderInformation (POX)</span></span>

<span data-ttu-id="64c09-104">El elemento **PublicFolderInformation** contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.</span><span class="sxs-lookup"><span data-stu-id="64c09-104">The **PublicFolderInformation** element contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span> 
  
[<span data-ttu-id="64c09-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
[<span data-ttu-id="64c09-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-106">Response (POX)</span></span>](response-pox.md)
  
[<span data-ttu-id="64c09-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-107">Account (POX)</span></span>](account-pox.md)
  
[<span data-ttu-id="64c09-108">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-108">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md)
  
```XML
<PublicFolderInformation>
   <SmtpAddress/>
</PublicFolderInformation>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="64c09-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="64c09-109">Attributes and elements</span></span>

<span data-ttu-id="64c09-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="64c09-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64c09-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="64c09-111">Attributes</span></span>

<span data-ttu-id="64c09-112">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="64c09-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="64c09-113">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="64c09-113">Child elements</span></span>

|<span data-ttu-id="64c09-114">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64c09-114">**Element**</span></span>|<span data-ttu-id="64c09-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64c09-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64c09-116">SmtpAddress (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-116">SmtpAddress (POX)</span></span>](smtpaddress-pox.md) <br/> |<span data-ttu-id="64c09-117">Contiene la dirección SMTP asignada al almacén de mensajes de carpeta pública configurado para el usuario.</span><span class="sxs-lookup"><span data-stu-id="64c09-117">Contains the SMTP address assigned to the public folder message store configured for the user.</span></span> <span data-ttu-id="64c09-118">Esta dirección SMTP puede usarse en el elemento [EmailAddress (POX)](emailaddress-pox.md) de una solicitud de detección automática para detectar la configuración de las carpetas públicas.</span><span class="sxs-lookup"><span data-stu-id="64c09-118">This SMTP address can be used in the [EMailAddress (POX)](emailaddress-pox.md) element of an Autodiscover request to discover public folder settings.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="64c09-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="64c09-119">Parent elements</span></span>

|<span data-ttu-id="64c09-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="64c09-120">**Element**</span></span>|<span data-ttu-id="64c09-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="64c09-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="64c09-122">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="64c09-122">Account (POX)</span></span>](account-pox.md) <br/> |<span data-ttu-id="64c09-123">Especifica la configuración de la cuenta del usuario.</span><span class="sxs-lookup"><span data-stu-id="64c09-123">Specifies account settings for the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="64c09-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="64c09-124">Remarks</span></span>

<span data-ttu-id="64c09-125">El elemento **PublicFolderInformation** es un elemento secundario opcional del elemento **account** .</span><span class="sxs-lookup"><span data-stu-id="64c09-125">The **PublicFolderInformation** element is an optional child element of the **Account** element.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64c09-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="64c09-126">See also</span></span>



[<span data-ttu-id="64c09-127">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="64c09-127">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

