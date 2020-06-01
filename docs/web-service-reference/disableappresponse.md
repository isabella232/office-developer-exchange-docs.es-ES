---
title: DisableAppResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 11ebe618-d759-4f16-be99-eaaa817ba782
description: El elemento DisableAppResponse especifica la respuesta a una solicitud DisableApp.
ms.openlocfilehash: cc28abf644247339e1226cd0e13824cc5f5669be
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455649"
---
# <a name="disableappresponse"></a><span data-ttu-id="44f0a-103">DisableAppResponse</span><span class="sxs-lookup"><span data-stu-id="44f0a-103">DisableAppResponse</span></span>

<span data-ttu-id="44f0a-104">El elemento **DisableAppResponse** especifica la respuesta a una solicitud **DisableApp** .</span><span class="sxs-lookup"><span data-stu-id="44f0a-104">The **DisableAppResponse** element specifies the response to a **DisableApp** request.</span></span> 
  
```XML
<DisableAppResponse>
    <MessageText></MessageText>
    <ResponseCode></ResponeCode>
    <DescriptiveLinkKey></DescriptiveLinkKey>
    <MessageXml></MessageXml>
</DisableAppResponse>
```

 <span data-ttu-id="44f0a-105">**DisableAppResponseType**</span><span class="sxs-lookup"><span data-stu-id="44f0a-105">**DisableAppResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="44f0a-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="44f0a-106">Attributes and elements</span></span>

<span data-ttu-id="44f0a-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="44f0a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="44f0a-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="44f0a-108">Attributes</span></span>

<span data-ttu-id="44f0a-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="44f0a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="44f0a-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="44f0a-110">Child elements</span></span>

|<span data-ttu-id="44f0a-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="44f0a-111">**Element**</span></span>|<span data-ttu-id="44f0a-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="44f0a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="44f0a-113">MessageText</span><span class="sxs-lookup"><span data-stu-id="44f0a-113">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="44f0a-114">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44f0a-114">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="44f0a-115">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="44f0a-115">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="44f0a-116">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44f0a-116">Provides status information about the request.</span></span>  <br/> |
|[<span data-ttu-id="44f0a-117">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="44f0a-117">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="44f0a-118">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="44f0a-118">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="44f0a-119">MessageXml</span><span class="sxs-lookup"><span data-stu-id="44f0a-119">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="44f0a-120">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="44f0a-120">Provides additional error response information.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="44f0a-121">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="44f0a-121">Parent elements</span></span>

<span data-ttu-id="44f0a-122">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="44f0a-122">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44f0a-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="44f0a-123">Remarks</span></span>

<span data-ttu-id="44f0a-124">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="44f0a-124">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="44f0a-125">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="44f0a-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="44f0a-126">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="44f0a-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="44f0a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="44f0a-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="44f0a-128">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="44f0a-128">Schema Name</span></span>  <br/> |<span data-ttu-id="44f0a-129">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="44f0a-129">Message schema</span></span>  <br/> |
|<span data-ttu-id="44f0a-130">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="44f0a-130">Validation File</span></span>  <br/> |<span data-ttu-id="44f0a-131">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="44f0a-131">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="44f0a-132">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="44f0a-132">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="44f0a-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="44f0a-133">See also</span></span>

- [<span data-ttu-id="44f0a-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="44f0a-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

