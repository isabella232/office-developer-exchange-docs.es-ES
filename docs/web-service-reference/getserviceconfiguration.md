---
title: GetServiceConfiguration
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetServiceConfiguration
api_type:
- schema
ms.assetid: acbb29e4-d853-4302-8e32-7018775d54e4
description: El elemento GetServiceConfiguration define una solicitud GetServiceConfiguration.
ms.openlocfilehash: 7ff7124ff062f21a02fc69b86b7cc7367ba3fcb6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835666"
---
# <a name="getserviceconfiguration"></a><span data-ttu-id="807d4-103">GetServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="807d4-103">GetServiceConfiguration</span></span>

<span data-ttu-id="807d4-104">El elemento **GetServiceConfiguration** define una solicitud GetServiceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="807d4-104">The **GetServiceConfiguration** element defines a GetServiceConfiguration request.</span></span> 
  
```XML
<GetServiceConfiguration>
   <ActingAs/>
   <RequestedConfiguration/>
</GetServiceConfiguration>
```

 <span data-ttu-id="807d4-105">**GetServiceConfigurationType**</span><span class="sxs-lookup"><span data-stu-id="807d4-105">**GetServiceConfigurationType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="807d4-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="807d4-106">Attributes and elements</span></span>

<span data-ttu-id="807d4-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="807d4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="807d4-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="807d4-108">Attributes</span></span>

<span data-ttu-id="807d4-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="807d4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="807d4-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="807d4-110">Child elements</span></span>

|<span data-ttu-id="807d4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="807d4-111">**Element**</span></span>|<span data-ttu-id="807d4-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="807d4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="807d4-113">ActingAs</span><span class="sxs-lookup"><span data-stu-id="807d4-113">ActingAs</span></span>](actingas.md) <br/> |<span data-ttu-id="807d4-114">Identifique quién envía como el autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="807d4-114">Identifies who the caller is sending as.</span></span> <span data-ttu-id="807d4-115">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="807d4-115">This element is optional.</span></span> <span data-ttu-id="807d4-116">Si este elemento no está presente, el usuario autenticado se supone que el remitente.</span><span class="sxs-lookup"><span data-stu-id="807d4-116">If this element is not present, the authenticated user is assumed to be the sender.</span></span> <span data-ttu-id="807d4-117">El elemento **ActingAs** debe incluirse para solicitar sugerencias de remitente.</span><span class="sxs-lookup"><span data-stu-id="807d4-117">The **ActingAs** element must be included for requesting sender hints.</span></span> <span data-ttu-id="807d4-118">Puede devolver un error de ErrorInvalidArgument en una respuesta si el elemento **ActingAs** falta, no incluye un tipo de distribución, no incluye una dirección de correo electrónico, contiene una dirección de correo electrónico no válida, no se resuelve a un usuario de dominio de Active Directory Services (AD DS), o se resuelve a varios usuarios en AD DS.</span><span class="sxs-lookup"><span data-stu-id="807d4-118">An ErrorInvalidArgument error can be returned in a response if the **ActingAs** element is missing, does not include a routing type, does not include an e-mail address, contains an invalid e-mail address, does not resolve to a user in Active Directory Domain Services (AD DS), or resolves to multiple users in AD DS.</span></span>  <br/> |
|[<span data-ttu-id="807d4-119">RequestedConfiguration</span><span class="sxs-lookup"><span data-stu-id="807d4-119">RequestedConfiguration</span></span>](requestedconfiguration.md) <br/> |<span data-ttu-id="807d4-120">Contiene las configuraciones del servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="807d4-120">Contains the requested service configurations.</span></span> <span data-ttu-id="807d4-121">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="807d4-121">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="807d4-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="807d4-122">Parent elements</span></span>

<span data-ttu-id="807d4-123">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="807d4-123">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="807d4-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="807d4-124">Text value</span></span>

<span data-ttu-id="807d4-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="807d4-125">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="807d4-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="807d4-126">Remarks</span></span>

<span data-ttu-id="807d4-127">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="807d4-127">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="807d4-128">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="807d4-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="807d4-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="807d4-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="807d4-130">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="807d4-130">Schema Name</span></span>  <br/> |<span data-ttu-id="807d4-131">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="807d4-131">Messages schema</span></span>  <br/> |
|<span data-ttu-id="807d4-132">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="807d4-132">Validation File</span></span>  <br/> |<span data-ttu-id="807d4-133">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="807d4-133">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="807d4-134">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="807d4-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="807d4-135">False</span><span class="sxs-lookup"><span data-stu-id="807d4-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="807d4-136">Ver también</span><span class="sxs-lookup"><span data-stu-id="807d4-136">See also</span></span>



- [<span data-ttu-id="807d4-137">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="807d4-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

