---
title: IsUMEnabled (servicio Web de mensajería unificada)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: 33810bbd-837f-4a71-9ed9-cb4b8c52186d
description: El elemento IsUMEnabled indica si un buzón está habilitado para mensajería unificada.
ms.openlocfilehash: ea5bde677c62664acad8afd5c8142e96d82b7a74
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458232"
---
# <a name="isumenabled-um-web-service"></a><span data-ttu-id="6d3df-103">IsUMEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="6d3df-103">IsUMEnabled (UM web service)</span></span>

<span data-ttu-id="6d3df-104">El elemento **IsUMEnabled** indica si un buzón está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="6d3df-104">The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging.</span></span> 
  
```xml
<IsUMEnabled/>
```

 <span data-ttu-id="6d3df-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="6d3df-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6d3df-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6d3df-106">Attributes and elements</span></span>

<span data-ttu-id="6d3df-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6d3df-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6d3df-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6d3df-108">Attributes</span></span>

<span data-ttu-id="6d3df-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d3df-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6d3df-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6d3df-110">Child elements</span></span>

<span data-ttu-id="6d3df-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d3df-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6d3df-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6d3df-112">Parent elements</span></span>

<span data-ttu-id="6d3df-113">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6d3df-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="6d3df-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="6d3df-114">Text value</span></span>

<span data-ttu-id="6d3df-115">Si se incluye este elemento, es necesario un valor de texto que represente un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="6d3df-115">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="6d3df-116">Un valor de **true** indica que el buzón de correo está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="6d3df-116">A value of **true** indicates that the mailbox is enabled for Unified Messaging.</span></span> <span data-ttu-id="6d3df-117">Un valor de **false** significa que el buzón de correo no está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="6d3df-117">A value of **false** means that the mailbox is not enabled for Unified Messaging.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6d3df-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6d3df-118">Remarks</span></span>

<span data-ttu-id="6d3df-119">Para determinar si un buzón está habilitado para mensajería unificada, use la [operación IsUMEnabled (servicio Web de mensajería unificada)](isumenabled-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="6d3df-119">To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6d3df-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6d3df-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6d3df-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="6d3df-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6d3df-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6d3df-122">Schema Name</span></span>  <br/> |<span data-ttu-id="6d3df-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="6d3df-123">Messages</span></span>  <br/> |
|<span data-ttu-id="6d3df-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6d3df-124">Validation File</span></span>  <br/> |<span data-ttu-id="6d3df-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6d3df-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6d3df-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6d3df-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="6d3df-127">Falso</span><span class="sxs-lookup"><span data-stu-id="6d3df-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d3df-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d3df-128">See also</span></span>



[<span data-ttu-id="6d3df-129">Operación IsUMEnabled (servicio Web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="6d3df-129">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)


[<span data-ttu-id="6d3df-130">Elementos XML de servicio Web de mensajería unificada para Exchange</span><span class="sxs-lookup"><span data-stu-id="6d3df-130">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

