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
description: El elemento request contiene las opciones de configuración solicitadas y los usuarios de destino.
ms.openlocfilehash: 4358713d19e763b75d2a43f147385026f43b1255
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44448992"
---
# <a name="request-soap"></a><span data-ttu-id="0cd9d-103">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-103">Request (SOAP)</span></span>

<span data-ttu-id="0cd9d-104">El elemento **request** contiene las opciones de configuración solicitadas y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="0cd9d-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="0cd9d-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0cd9d-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0cd9d-106">Attributes and elements</span></span>

<span data-ttu-id="0cd9d-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0cd9d-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0cd9d-108">Attributes</span></span>

<span data-ttu-id="0cd9d-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0cd9d-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0cd9d-110">Child elements</span></span>

|<span data-ttu-id="0cd9d-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0cd9d-111">**Element**</span></span>|<span data-ttu-id="0cd9d-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cd9d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cd9d-113">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="0cd9d-114">Representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="0cd9d-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="0cd9d-116">Contiene los nombres de las opciones de configuración solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="0cd9d-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="0cd9d-118">Especifica la versión de servidor específica que el proveedor desea usar.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0cd9d-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0cd9d-119">Parent elements</span></span>

|<span data-ttu-id="0cd9d-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0cd9d-120">**Element**</span></span>|<span data-ttu-id="0cd9d-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0cd9d-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0cd9d-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="0cd9d-123">Representa una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="0cd9d-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0cd9d-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0cd9d-124">Text value</span></span>

<span data-ttu-id="0cd9d-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0cd9d-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0cd9d-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0cd9d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0cd9d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0cd9d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0cd9d-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0cd9d-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0cd9d-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="0cd9d-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0cd9d-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0cd9d-130">Validation File</span></span>  <br/> |<span data-ttu-id="0cd9d-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0cd9d-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0cd9d-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0cd9d-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0cd9d-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0cd9d-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0cd9d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cd9d-134">See also</span></span>



[<span data-ttu-id="0cd9d-135">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0cd9d-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

