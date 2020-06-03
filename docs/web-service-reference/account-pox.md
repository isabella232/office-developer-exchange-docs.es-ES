---
title: Cuenta (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 488fdbdc-e9d9-4301-91ab-e22eb42e549e
description: El elemento Account especifica la configuración de la cuenta para el usuario o contiene respuestas de error.
ms.openlocfilehash: ffd8ebe4b7bd9d4b3f6a9b42fc557ac6189a068d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462321"
---
# <a name="account-pox"></a><span data-ttu-id="cda37-103">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-103">Account (POX)</span></span>

<span data-ttu-id="cda37-104">El elemento **account** especifica la configuración de la cuenta para el usuario o contiene respuestas de error.</span><span class="sxs-lookup"><span data-stu-id="cda37-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="cda37-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
- [<span data-ttu-id="cda37-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-106">Response (POX)</span></span>](response-pox.md)
- [<span data-ttu-id="cda37-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-107">Account (POX)</span></span>](account-pox.md)
  
```XML
<Account>
   <AccountType/>
   <Action/>
   <MicrosoftOnline/>
   <RedirectURL/>
   <RedirectAddr/>
   <Image/>
   <ServiceHome/>
   <Protocol/>
   <PublicFolderInformation/>
</Account>
```

<br/>

```XML
<Account> 
    <Error/> 
</Account>
```

## <a name="attributes-and-elements"></a><span data-ttu-id="cda37-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cda37-108">Attributes and elements</span></span>

<span data-ttu-id="cda37-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cda37-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cda37-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="cda37-110">Attributes</span></span>

<span data-ttu-id="cda37-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cda37-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cda37-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cda37-112">Child elements</span></span>

|<span data-ttu-id="cda37-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cda37-113">**Element**</span></span>|<span data-ttu-id="cda37-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cda37-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda37-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="cda37-116">Representa el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="cda37-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="cda37-117">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="cda37-118">Proporciona información que se usa para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración del usuario.</span><span class="sxs-lookup"><span data-stu-id="cda37-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="cda37-119">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="cda37-120">Contiene un valor que indica si el buzón del usuario está hospedado en Exchange online o Exchange online como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="cda37-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="cda37-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="cda37-122">Contiene la dirección URL del equipo que ejecuta Exchange Server y que tiene instalado el rol de servidor acceso de clientes que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="cda37-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="cda37-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="cda37-124">Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática posterior.</span><span class="sxs-lookup"><span data-stu-id="cda37-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="cda37-125">Imagen (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="cda37-126">Contiene la ruta de acceso de una imagen que se usa para personalizar la experiencia de configuración.</span><span class="sxs-lookup"><span data-stu-id="cda37-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="cda37-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="cda37-128">Contiene la dirección URL de la Página principal del proveedor de servicios de Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="cda37-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="cda37-129">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="cda37-130">Contiene las especificaciones para conectar un cliente al servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="cda37-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="cda37-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="cda37-132">Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar la información de las carpetas públicas del usuario.</span><span class="sxs-lookup"><span data-stu-id="cda37-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="cda37-133">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="cda37-134">Contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="cda37-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cda37-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cda37-135">Parent elements</span></span>

|<span data-ttu-id="cda37-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="cda37-136">**Element**</span></span>|<span data-ttu-id="cda37-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="cda37-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cda37-138">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="cda37-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="cda37-139">Contiene la respuesta del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="cda37-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cda37-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cda37-140">See also</span></span>

- [<span data-ttu-id="cda37-141">Elementos XML de detección automática de POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="cda37-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

