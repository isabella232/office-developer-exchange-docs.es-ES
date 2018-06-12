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
description: El elemento de cuenta especifica la configuración de cuenta para el usuario o contiene las respuestas de error.
ms.openlocfilehash: 88911aad41816f7cefbffef151e066fe5d4da192
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764553"
---
# <a name="account-pox"></a><span data-ttu-id="44b45-103">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-103">Account (POX)</span></span>

<span data-ttu-id="44b45-104">El elemento de **cuenta** especifica la configuración de cuenta para el usuario o contiene las respuestas de error.</span><span class="sxs-lookup"><span data-stu-id="44b45-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="44b45-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="44b45-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="44b45-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-107">Account (POX)</span></span>](account-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="44b45-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44b45-108">Attributes and elements</span></span>

<span data-ttu-id="44b45-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44b45-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44b45-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="44b45-110">Attributes</span></span>

<span data-ttu-id="44b45-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44b45-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44b45-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44b45-112">Child elements</span></span>

|<span data-ttu-id="44b45-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="44b45-113">**Element**</span></span>|<span data-ttu-id="44b45-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44b45-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44b45-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="44b45-116">Representa el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="44b45-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="44b45-117">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="44b45-118">Proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="44b45-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="44b45-119">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="44b45-120">Contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="44b45-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="44b45-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="44b45-122">Contiene la dirección URL del equipo que ejecuta Exchange Server que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="44b45-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="44b45-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="44b45-124">Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="44b45-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="44b45-125">Imagen (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="44b45-126">Contiene la ruta de acceso de una imagen que se usa para personalizar la marca de la experiencia de configuración.</span><span class="sxs-lookup"><span data-stu-id="44b45-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="44b45-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="44b45-128">Contiene la dirección URL de la página principal del proveedor de servicios Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="44b45-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="44b45-129">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="44b45-130">Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="44b45-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="44b45-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="44b45-132">Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="44b45-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="44b45-133">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="44b45-134">Contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="44b45-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44b45-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44b45-135">Parent elements</span></span>

|<span data-ttu-id="44b45-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="44b45-136">**Element**</span></span>|<span data-ttu-id="44b45-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44b45-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44b45-138">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="44b45-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="44b45-139">Contiene la respuesta del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="44b45-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="44b45-140">Ver también</span><span class="sxs-lookup"><span data-stu-id="44b45-140">See also</span></span>

- [<span data-ttu-id="44b45-141">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="44b45-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

