---
title: RedirectTarget (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f8162724-cf9a-4543-a1ad-5846c8b10bfa
description: El elemento RedirectTarget (SOAP) contiene el destino de la dirección de correo electrónico o de dirección URL de redirección.
ms.openlocfilehash: 3a8a0c39c6889730c9d17778c6a26f84fcbcd4a7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837019"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="194ca-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="194ca-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="194ca-104">El elemento [RedirectTarget (SOAP)](redirecttarget-soap.md) contiene el destino de la dirección de correo electrónico o de dirección URL de redirección.</span><span class="sxs-lookup"><span data-stu-id="194ca-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="194ca-105">**string**</span><span class="sxs-lookup"><span data-stu-id="194ca-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="194ca-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="194ca-106">Attributes and elements</span></span>

<span data-ttu-id="194ca-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="194ca-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="194ca-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="194ca-108">Attributes</span></span>

<span data-ttu-id="194ca-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="194ca-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="194ca-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="194ca-110">Child elements</span></span>

<span data-ttu-id="194ca-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="194ca-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="194ca-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="194ca-112">Parent elements</span></span>

|<span data-ttu-id="194ca-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="194ca-113">**Element**</span></span>|<span data-ttu-id="194ca-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="194ca-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="194ca-115">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="194ca-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="194ca-116">Representa una respuesta a una solicitud de GetUserSettings para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="194ca-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="194ca-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="194ca-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="194ca-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="194ca-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="194ca-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="194ca-119">Text value</span></span>

<span data-ttu-id="194ca-120">El valor de texto contiene el destino de la dirección de dirección URL o el correo electrónico de redirección que se debe usar para una GetUserSettings posteriores o solicitar GetDomainSettings.</span><span class="sxs-lookup"><span data-stu-id="194ca-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="194ca-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="194ca-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="194ca-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="194ca-122">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="194ca-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="194ca-123">Schema Name</span></span>  <br/> |<span data-ttu-id="194ca-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="194ca-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="194ca-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="194ca-125">Validation File</span></span>  <br/> |<span data-ttu-id="194ca-126">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="194ca-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="194ca-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="194ca-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="194ca-128">True</span><span class="sxs-lookup"><span data-stu-id="194ca-128">True</span></span>  <br/> |
   

