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
description: El elemento RedirectTarget (SOAP) contiene el destino de la dirección URL de redirección o de correo electrónico.
ms.openlocfilehash: 092d575560379d43b12dd98a3efa155b59c31450
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462202"
---
# <a name="redirecttarget-soap"></a><span data-ttu-id="b4b94-103">RedirectTarget (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b4b94-103">RedirectTarget (SOAP)</span></span>

<span data-ttu-id="b4b94-104">El elemento [RedirectTarget (SOAP)](redirecttarget-soap.md) contiene el destino de la dirección URL de redirección o de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="b4b94-104">The [RedirectTarget (SOAP)](redirecttarget-soap.md) element contains the target of the redirection URL or e-mail address.</span></span> 
  
```XML
<RedirectTarget/>
```

 <span data-ttu-id="b4b94-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b4b94-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b4b94-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b4b94-106">Attributes and elements</span></span>

<span data-ttu-id="b4b94-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b4b94-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b4b94-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b4b94-108">Attributes</span></span>

<span data-ttu-id="b4b94-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b4b94-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b4b94-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b4b94-110">Child elements</span></span>

<span data-ttu-id="b4b94-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="b4b94-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b4b94-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b4b94-112">Parent elements</span></span>

|<span data-ttu-id="b4b94-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="b4b94-113">**Element**</span></span>|<span data-ttu-id="b4b94-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b4b94-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b4b94-115">UserResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b4b94-115">UserResponse (SOAP)</span></span>](userresponse-soap.md) <br/> |<span data-ttu-id="b4b94-116">Representa una respuesta a una solicitud de GetUserSettings para un usuario individual.</span><span class="sxs-lookup"><span data-stu-id="b4b94-116">Represents a response to a GetUserSettings request for an individual user.</span></span>  <br/> |
|[<span data-ttu-id="b4b94-117">DomainResponse (SOAP)</span><span class="sxs-lookup"><span data-stu-id="b4b94-117">DomainResponse (SOAP)</span></span>](domainresponse-soap.md) <br/> |<span data-ttu-id="b4b94-118">Contiene la configuración solicitada para el dominio especificado.</span><span class="sxs-lookup"><span data-stu-id="b4b94-118">Contains the requested settings for the specified domain.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="b4b94-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="b4b94-119">Text value</span></span>

<span data-ttu-id="b4b94-120">El valor de texto contiene el destino de la dirección URL de redirección o de correo electrónico que se debe usar para una solicitud GetUserSettings o GetDomainSettings subsiguiente.</span><span class="sxs-lookup"><span data-stu-id="b4b94-120">The text value contains the target of the redirection URL or e-mail address that should be used for a subsequent GetUserSettings or GetDomainSettings request.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b4b94-121">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b4b94-121">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b4b94-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="b4b94-122">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="b4b94-123">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b4b94-123">Schema Name</span></span>  <br/> |<span data-ttu-id="b4b94-124">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="b4b94-124">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="b4b94-125">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b4b94-125">Validation File</span></span>  <br/> |<span data-ttu-id="b4b94-126">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="b4b94-126">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b4b94-127">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b4b94-127">Can be Empty</span></span>  <br/> |<span data-ttu-id="b4b94-128">Verdadero</span><span class="sxs-lookup"><span data-stu-id="b4b94-128">True</span></span>  <br/> |
   

