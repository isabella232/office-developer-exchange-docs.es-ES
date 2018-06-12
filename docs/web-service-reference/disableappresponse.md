---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: El elemento DisableAppResponse especifica la respuesta a una solicitud de DisableApp.
ms.openlocfilehash: 740801fa4b60e217f0b9148bcfcc5b206e96bf31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764181"
---
# <a name="disableappresponse"></a><span data-ttu-id="428f8-103">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="428f8-103">DisableAppResponse</span></span>

<span data-ttu-id="428f8-104">El elemento **DisableAppResponse** especifica la respuesta a una solicitud de **DisableApp** .</span><span class="sxs-lookup"><span data-stu-id="428f8-104">The **DisableAppResponse** element specifies the response to a **DisableApp** request.</span></span> 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 <span data-ttu-id="428f8-105">**DisableAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="428f8-105">**DisableAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="428f8-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="428f8-106">Attributes and elements</span></span>

<span data-ttu-id="428f8-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="428f8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="428f8-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="428f8-108">Attributes</span></span>

<span data-ttu-id="428f8-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="428f8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="428f8-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="428f8-110">Child elements</span></span>

|<span data-ttu-id="428f8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="428f8-111">**Element**</span></span>|<span data-ttu-id="428f8-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="428f8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="428f8-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="428f8-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="428f8-114">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="428f8-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="428f8-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="428f8-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="428f8-116">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="428f8-116">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="428f8-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="428f8-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="428f8-118">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="428f8-118">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="428f8-119">MessageXml</span><span class="sxs-lookup"><span data-stu-id="428f8-119">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="428f8-120">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="428f8-120">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="428f8-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="428f8-121">Parent elements</span></span>

<span data-ttu-id="428f8-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="428f8-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="428f8-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="428f8-123">Remarks</span></span>

<span data-ttu-id="428f8-124">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="428f8-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="428f8-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="428f8-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="428f8-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="428f8-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="428f8-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="428f8-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="428f8-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="428f8-128">Schema Name</span></span>  <br/> |<span data-ttu-id="428f8-129">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="428f8-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="428f8-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="428f8-130">Validation File</span></span>  <br/> |<span data-ttu-id="428f8-131">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="428f8-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="428f8-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="428f8-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="428f8-133">Ver también</span><span class="sxs-lookup"><span data-stu-id="428f8-133">See also</span></span>

- [<span data-ttu-id="428f8-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="428f8-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

