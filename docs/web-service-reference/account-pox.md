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
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764553"
---
# <a name="account-pox"></a><span data-ttu-id="54634-103">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-103">Account (POX)</span></span>

<span data-ttu-id="54634-104">El elemento de **cuenta** especifica la configuración de cuenta para el usuario o contiene las respuestas de error.</span><span class="sxs-lookup"><span data-stu-id="54634-104">The **Account** element specifies account settings for the user or contains error responses.</span></span> 
  
- [<span data-ttu-id="54634-105">Detección automática (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-105">AutoDiscover (POX)</span></span>](autodiscover-pox.md)
  
- [<span data-ttu-id="54634-106">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-106">Response (POX)</span></span>](response-pox.md)
  
- [<span data-ttu-id="54634-107">Cuenta (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-107">Account (POX)</span></span>](account-pox.md)
  
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

## <a name="attributes-and-elements"></a><span data-ttu-id="54634-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="54634-108">Attributes and elements</span></span>

<span data-ttu-id="54634-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="54634-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54634-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="54634-110">Attributes</span></span>

<span data-ttu-id="54634-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="54634-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="54634-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="54634-112">Child elements</span></span>

|<span data-ttu-id="54634-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="54634-113">**Element**</span></span>|<span data-ttu-id="54634-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54634-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54634-115">AccountType (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-115">AccountType (POX)</span></span>](accounttype-pox.md) <br/> |<span data-ttu-id="54634-116">Representa el tipo de cuenta.</span><span class="sxs-lookup"><span data-stu-id="54634-116">Represents the account type.</span></span>  <br/> |
|[<span data-ttu-id="54634-117">Acción (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-117">Action (POX)</span></span>](action-pox.md) <br/> |<span data-ttu-id="54634-118">Proporciona información que se utiliza para determinar si se requiere otra solicitud de detección automática para devolver la información de configuración de usuario.</span><span class="sxs-lookup"><span data-stu-id="54634-118">Provides information that is used to determine whether another Autodiscover request is required to return the user configuration information.</span></span>  <br/> |
|[<span data-ttu-id="54634-119">MicrosoftOnline (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-119">MicrosoftOnline (POX)</span></span>](microsoftonline-pox.md) <br/> |<span data-ttu-id="54634-120">Contiene un valor que indica si el buzón del usuario está hospedado en Exchange Online o Exchange Online como parte de Office 365.</span><span class="sxs-lookup"><span data-stu-id="54634-120">Contains a value that indicates whether the user's mailbox is hosted in Exchange Online or Exchange Online as part of Office 365.</span></span>  <br/> |
|[<span data-ttu-id="54634-121">RedirectUrl (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-121">RedirectUrl (POX)</span></span>](redirecturl-pox.md) <br/> |<span data-ttu-id="54634-122">Contiene la dirección URL del equipo que ejecuta Exchange Server que tiene el rol de servidor de acceso de cliente instalado que se debe usar para obtener la configuración de detección automática.</span><span class="sxs-lookup"><span data-stu-id="54634-122">Contains the URL of the computer that is running Exchange Server that has the Client Access server role installed that should be used to obtain Autodiscover settings.</span></span>  <br/> |
|[<span data-ttu-id="54634-123">RedirectAddr (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-123">RedirectAddr (POX)</span></span>](redirectaddr-pox.md) <br/> |<span data-ttu-id="54634-124">Especifica la dirección de correo electrónico que se debe usar para una solicitud de detección automática subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="54634-124">Specifies the email address that should be used for a subsequent Autodiscover request.</span></span>  <br/> |
|[<span data-ttu-id="54634-125">Imagen (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-125">Image (POX)</span></span>](image-pox.md) <br/> |<span data-ttu-id="54634-126">Contiene la ruta de acceso de una imagen que se usa para personalizar la marca de la experiencia de configuración.</span><span class="sxs-lookup"><span data-stu-id="54634-126">Contains the path of an image that is used to brand the configuration experience.</span></span>  <br/> |
|[<span data-ttu-id="54634-127">ServiceHome (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-127">ServiceHome (POX)</span></span>](servicehome-pox.md) <br/> |<span data-ttu-id="54634-128">Contiene la dirección URL de la página principal del proveedor de servicios Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="54634-128">Contains the URL of the home page of the Internet service provider (ISP).</span></span>  <br/> |
|[<span data-ttu-id="54634-129">Protocolo (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-129">Protocol (POX)</span></span>](protocol-pox.md) <br/> |<span data-ttu-id="54634-130">Contiene las especificaciones para conectar a un cliente con el servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="54634-130">Contains the specifications for connecting a client to the Client Access server.</span></span>  <br/> |
|[<span data-ttu-id="54634-131">PublicFolderInformation (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-131">PublicFolderInformation (POX)</span></span>](publicfolderinformation-pox.md) <br/> |<span data-ttu-id="54634-132">Contiene información que los clientes pueden usar para enviar una solicitud de detección automática para detectar información de carpetas públicas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="54634-132">Contains information that clients can use to send an Autodiscover request to discover public folder information for the user.</span></span>  <br/> |
|[<span data-ttu-id="54634-133">Error (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-133">Error (POX)</span></span>](error-pox.md) <br/> |<span data-ttu-id="54634-134">Contiene una respuesta de error de detección automática.</span><span class="sxs-lookup"><span data-stu-id="54634-134">Contains an Autodiscover error response.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="54634-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="54634-135">Parent elements</span></span>

|<span data-ttu-id="54634-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="54634-136">**Element**</span></span>|<span data-ttu-id="54634-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="54634-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="54634-138">Respuesta (POX)</span><span class="sxs-lookup"><span data-stu-id="54634-138">Response (POX)</span></span>](response-pox.md) <br/> |<span data-ttu-id="54634-139">Contiene la respuesta del servicio Detección automática.</span><span class="sxs-lookup"><span data-stu-id="54634-139">Contains the response from the Autodiscover service.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54634-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="54634-140">See also</span></span>

- [<span data-ttu-id="54634-141">Elementos de Autodiscover XML POX para Exchange</span><span class="sxs-lookup"><span data-stu-id="54634-141">POX Autodiscover XML elements for Exchange</span></span>](pox-autodiscover-xml-elements-for-exchange.md)

