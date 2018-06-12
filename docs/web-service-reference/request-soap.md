---
title: Solicitud (SOAP)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 75696436-997e-49f1-a31b-eb9a8c3526f3
description: El elemento de solicitud contiene las opciones de configuración solicitado y los usuarios de destino.
ms.openlocfilehash: dfea33786066dd7803d0fd061cbb87bb06d11531
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19837125"
---
# <a name="request-soap"></a><span data-ttu-id="7bbf2-103">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-103">Request (SOAP)</span></span>

<span data-ttu-id="7bbf2-104">El elemento de **solicitud** contiene las opciones de configuración solicitado y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="7bbf2-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7bbf2-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="7bbf2-106">Attributes and elements</span></span>

<span data-ttu-id="7bbf2-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7bbf2-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="7bbf2-108">Attributes</span></span>

<span data-ttu-id="7bbf2-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="7bbf2-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="7bbf2-110">Child elements</span></span>

|<span data-ttu-id="7bbf2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-111">**Element**</span></span>|<span data-ttu-id="7bbf2-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bbf2-113">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="7bbf2-114">Representa una colección de direcciones de correo electrónico de los usuarios para el que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="7bbf2-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="7bbf2-116">Contiene los nombres de las opciones de configuración solicitado.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="7bbf2-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="7bbf2-118">Especifica la versión de servidor específico que le gustaría usar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7bbf2-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="7bbf2-119">Parent elements</span></span>

|<span data-ttu-id="7bbf2-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-120">**Element**</span></span>|<span data-ttu-id="7bbf2-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7bbf2-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7bbf2-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="7bbf2-123">Representa una solicitud de [operación GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbf2-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="7bbf2-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="7bbf2-124">Text value</span></span>

<span data-ttu-id="7bbf2-125">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="7bbf2-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7bbf2-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="7bbf2-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7bbf2-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7bbf2-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="7bbf2-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="7bbf2-128">Schema Name</span></span>  <br/> |<span data-ttu-id="7bbf2-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="7bbf2-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="7bbf2-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="7bbf2-130">Validation File</span></span>  <br/> |<span data-ttu-id="7bbf2-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7bbf2-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7bbf2-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="7bbf2-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="7bbf2-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="7bbf2-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7bbf2-134">Ver también</span><span class="sxs-lookup"><span data-stu-id="7bbf2-134">See also</span></span>



[<span data-ttu-id="7bbf2-135">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="7bbf2-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

