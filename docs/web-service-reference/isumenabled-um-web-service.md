---
title: IsUMEnabled (servicio web de mensajería unificada)
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
description: El elemento IsUMEnabled indica si un buzón de correo está habilitado para mensajería unificada.
ms.openlocfilehash: 5f4d59c5497158e5afbc8bb5db4900bd129df50b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19836113"
---
# <a name="isumenabled-um-web-service"></a><span data-ttu-id="31e4b-103">IsUMEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="31e4b-103">IsUMEnabled (UM web service)</span></span>

<span data-ttu-id="31e4b-104">El elemento **IsUMEnabled** indica si un buzón de correo está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="31e4b-104">The **IsUMEnabled** element indicates whether a mailbox is enabled for Unified Messaging.</span></span> 
  
```xml
<IsUMEnabled/>
```

 <span data-ttu-id="31e4b-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="31e4b-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31e4b-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="31e4b-106">Attributes and elements</span></span>

<span data-ttu-id="31e4b-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="31e4b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31e4b-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="31e4b-108">Attributes</span></span>

<span data-ttu-id="31e4b-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31e4b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31e4b-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="31e4b-110">Child elements</span></span>

<span data-ttu-id="31e4b-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31e4b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="31e4b-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="31e4b-112">Parent elements</span></span>

<span data-ttu-id="31e4b-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="31e4b-113">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="31e4b-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="31e4b-114">Text value</span></span>

<span data-ttu-id="31e4b-115">Si este elemento se incluye, se requiere un valor de texto que representa un valor de tipo Boolean.</span><span class="sxs-lookup"><span data-stu-id="31e4b-115">A text value that represents a Boolean value is required if this element is included.</span></span> <span data-ttu-id="31e4b-116">Un valor de **true** indica que el buzón está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="31e4b-116">A value of **true** indicates that the mailbox is enabled for Unified Messaging.</span></span> <span data-ttu-id="31e4b-117">Un valor de **false** significa que el buzón de correo no está habilitado para mensajería unificada.</span><span class="sxs-lookup"><span data-stu-id="31e4b-117">A value of **false** means that the mailbox is not enabled for Unified Messaging.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31e4b-118">Notas</span><span class="sxs-lookup"><span data-stu-id="31e4b-118">Remarks</span></span>

<span data-ttu-id="31e4b-119">Para determinar si un buzón de correo está habilitado para mensajería unificada, use la [operación de IsUMEnabled (servicio web de mensajería unificada)](isumenabled-operation-um-web-service.md).</span><span class="sxs-lookup"><span data-stu-id="31e4b-119">To determine whether a mailbox is enabled for Unified Messaging, use the [IsUMEnabled operation (UM web service)](isumenabled-operation-um-web-service.md).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31e4b-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="31e4b-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31e4b-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="31e4b-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="31e4b-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="31e4b-122">Schema Name</span></span>  <br/> |<span data-ttu-id="31e4b-123">Mensajes</span><span class="sxs-lookup"><span data-stu-id="31e4b-123">Messages</span></span>  <br/> |
|<span data-ttu-id="31e4b-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="31e4b-124">Validation File</span></span>  <br/> |<span data-ttu-id="31e4b-125">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="31e4b-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="31e4b-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="31e4b-126">Can be Empty</span></span>  <br/> |<span data-ttu-id="31e4b-127">False</span><span class="sxs-lookup"><span data-stu-id="31e4b-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31e4b-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="31e4b-128">See also</span></span>



[<span data-ttu-id="31e4b-129">Operación IsUMEnabled (servicio web de mensajería unificada)</span><span class="sxs-lookup"><span data-stu-id="31e4b-129">IsUMEnabled operation (UM web service)</span></span>](isumenabled-operation-um-web-service.md)


[<span data-ttu-id="31e4b-130">Elementos XML de servicio de web de Unified Messaging para Exchange</span><span class="sxs-lookup"><span data-stu-id="31e4b-130">Unified Messaging web service XML elements for Exchange</span></span>](unified-messaging-web-service-xml-elements-for-exchange.md)

