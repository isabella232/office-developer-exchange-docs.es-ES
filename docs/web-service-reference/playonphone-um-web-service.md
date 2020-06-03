---
title: Reproducir (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 206a2ad1-a01d-4e71-99a1-90c2530423da
description: El elemento reproducir define una solicitud para reproducir un elemento en un teléfono.
ms.openlocfilehash: 9acbf9edbf4a889506558b24f5736a44d5015d3f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44434081"
---
# <a name="playonphone-um-web-service"></a><span data-ttu-id="07f43-103">Reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="07f43-103">PlayOnPhone (UM web service)</span></span>

<span data-ttu-id="07f43-104">El elemento **reproducir** define una solicitud para reproducir un elemento en un teléfono.</span><span class="sxs-lookup"><span data-stu-id="07f43-104">The **PlayOnPhone** element defines a request to play an item on a telephone.</span></span> 
  
[<span data-ttu-id="07f43-105">Reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="07f43-105">PlayOnPhone (UM web service)</span></span>](playonphone-um-web-service.md)
  
```xml
<PlayOnPhone>
  <entryId>   </entryId>
  <DialString>   </DialString>
</PlayOnPhone>
```

 <span data-ttu-id="07f43-106">**complexType**</span><span class="sxs-lookup"><span data-stu-id="07f43-106">**complexType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="07f43-107">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="07f43-107">Attributes and elements</span></span>

<span data-ttu-id="07f43-108">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="07f43-108">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="07f43-109">Atributos</span><span class="sxs-lookup"><span data-stu-id="07f43-109">Attributes</span></span>

<span data-ttu-id="07f43-110">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="07f43-110">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="07f43-111">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="07f43-111">Child elements</span></span>

|<span data-ttu-id="07f43-112">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="07f43-112">**Element**</span></span>|<span data-ttu-id="07f43-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="07f43-113">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="07f43-114">entryId (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="07f43-114">entryId (UM web service)</span></span>](entryid-um-web-service.md) <br/> |<span data-ttu-id="07f43-115">Contiene el valor que representa el identificador del elemento que se va a reproducir en el teléfono en una solicitud de [operación de reproducir (servicio Web de mensajería unificada)](playonphone-operation-um-web-service.md) .</span><span class="sxs-lookup"><span data-stu-id="07f43-115">Contains the value that represents the identifier of the item to play on the telephone in a [PlayOnPhone operation (UM web service)](playonphone-operation-um-web-service.md) request.</span></span>  <br/> |
|[<span data-ttu-id="07f43-116">dialString (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="07f43-116">dialString (UM web service)</span></span>](dialstring-um-web-service.md) <br/> |<span data-ttu-id="07f43-117">Contiene el valor del número de teléfono que se marca.</span><span class="sxs-lookup"><span data-stu-id="07f43-117">Contains the value for the telephone number to dial.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="07f43-118">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="07f43-118">Parent elements</span></span>

<span data-ttu-id="07f43-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="07f43-119">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="07f43-120">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="07f43-120">Text value</span></span>

<span data-ttu-id="07f43-121">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="07f43-121">None.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="07f43-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="07f43-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="07f43-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="07f43-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="07f43-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="07f43-124">Schema Name</span></span>  <br/> |<span data-ttu-id="07f43-125">Mensajes</span><span class="sxs-lookup"><span data-stu-id="07f43-125">Messages</span></span>  <br/> |
|<span data-ttu-id="07f43-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="07f43-126">Validation File</span></span>  <br/> |<span data-ttu-id="07f43-127">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="07f43-127">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="07f43-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="07f43-128">Can be Empty</span></span>  <br/> |<span data-ttu-id="07f43-129">Falso</span><span class="sxs-lookup"><span data-stu-id="07f43-129">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="07f43-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="07f43-130">See also</span></span>



[<span data-ttu-id="07f43-131">Operación reproducir (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="07f43-131">PlayOnPhone operation (UM web service)</span></span>](playonphone-operation-um-web-service.md)

