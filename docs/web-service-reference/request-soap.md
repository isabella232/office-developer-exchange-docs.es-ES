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
ms.lasthandoff: 05/31/2020
ms.locfileid: "44448992"
---
# <a name="request-soap"></a><span data-ttu-id="0e49a-103">Solicitud (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-103">Request (SOAP)</span></span>

<span data-ttu-id="0e49a-104">El elemento **request** contiene las opciones de configuración solicitadas y los usuarios de destino.</span><span class="sxs-lookup"><span data-stu-id="0e49a-104">The **Request** element contains the requested configuration settings and the target users.</span></span> 
  
```XML
<Request>
   <Users/>
   <RequestedSettings/>
   <RequestedVersion/>
</Request>
```

 <span data-ttu-id="0e49a-105">**GetUserSettingsRequest**</span><span class="sxs-lookup"><span data-stu-id="0e49a-105">**GetUserSettingsRequest**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0e49a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="0e49a-106">Attributes and elements</span></span>

<span data-ttu-id="0e49a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="0e49a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0e49a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="0e49a-108">Attributes</span></span>

<span data-ttu-id="0e49a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e49a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0e49a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="0e49a-110">Child elements</span></span>

|<span data-ttu-id="0e49a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0e49a-111">**Element**</span></span>|<span data-ttu-id="0e49a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e49a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e49a-113">Usuarios (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-113">Users (SOAP)</span></span>](users-soap.md) <br/> |<span data-ttu-id="0e49a-114">Representa una colección de direcciones de correo electrónico de los usuarios para los que se debe recuperar la configuración.</span><span class="sxs-lookup"><span data-stu-id="0e49a-114">Represents a collection of e-mail addresses of the users for whom settings should be retrieved.</span></span>  <br/> |
|[<span data-ttu-id="0e49a-115">RequestedSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-115">RequestedSettings (SOAP)</span></span>](requestedsettings-soap.md) <br/> |<span data-ttu-id="0e49a-116">Contiene los nombres de las opciones de configuración solicitadas.</span><span class="sxs-lookup"><span data-stu-id="0e49a-116">Contains the names of the requested configuration settings.</span></span>  <br/> |
|[<span data-ttu-id="0e49a-117">RequestedVersion (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-117">RequestedVersion (SOAP)</span></span>](requestedversion-soap.md) <br/> |<span data-ttu-id="0e49a-118">Especifica la versión de servidor específica que el proveedor desea usar.</span><span class="sxs-lookup"><span data-stu-id="0e49a-118">Specifies the specific server version that the provider would like to use.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="0e49a-119">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="0e49a-119">Parent elements</span></span>

|<span data-ttu-id="0e49a-120">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="0e49a-120">**Element**</span></span>|<span data-ttu-id="0e49a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0e49a-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0e49a-122">GetUserSettingsRequestMessage (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-122">GetUserSettingsRequestMessage (SOAP)</span></span>](getusersettingsrequestmessage-soap.md) <br/> |<span data-ttu-id="0e49a-123">Representa una solicitud de [operación de GetUserSettings (SOAP)](getusersettings-operation-soap.md) .</span><span class="sxs-lookup"><span data-stu-id="0e49a-123">Represents a [GetUserSettings operation (SOAP)](getusersettings-operation-soap.md) request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0e49a-124">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="0e49a-124">Text value</span></span>

<span data-ttu-id="0e49a-125">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="0e49a-125">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0e49a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="0e49a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0e49a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e49a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/2010/Autodiscover  <br/> |
|<span data-ttu-id="0e49a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="0e49a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="0e49a-129">Esquema de detección automática</span><span class="sxs-lookup"><span data-stu-id="0e49a-129">Autodiscover schema</span></span>  <br/> |
|<span data-ttu-id="0e49a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="0e49a-130">Validation File</span></span>  <br/> |<span data-ttu-id="0e49a-131">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="0e49a-131">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="0e49a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="0e49a-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="0e49a-133">Verdadero</span><span class="sxs-lookup"><span data-stu-id="0e49a-133">True</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0e49a-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="0e49a-134">See also</span></span>



[<span data-ttu-id="0e49a-135">Operación GetUserSettings (SOAP)</span><span class="sxs-lookup"><span data-stu-id="0e49a-135">GetUserSettings operation (SOAP)</span></span>](getusersettings-operation-soap.md)

