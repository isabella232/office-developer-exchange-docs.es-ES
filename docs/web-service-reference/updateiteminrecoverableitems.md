---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: El elemento UpdateItemInRecoverableItems especifica una solicitud para actualizar un elemento de elementos recuperables.
ms.openlocfilehash: 768de4bb8abe4780ab520405bae3149b8f17637c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19840837"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="c1ed7-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="c1ed7-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="c1ed7-104">El elemento **UpdateItemInRecoverableItems** especifica una solicitud para actualizar un elemento de elementos recuperables.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="c1ed7-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="c1ed7-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c1ed7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c1ed7-106">Attributes and elements</span></span>

<span data-ttu-id="c1ed7-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c1ed7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c1ed7-108">Attributes</span></span>

<span data-ttu-id="c1ed7-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c1ed7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c1ed7-110">Child elements</span></span>

<span data-ttu-id="c1ed7-111">[ItemId](itemid.md) | [actualizaciones (elemento)](updates-item.md) | [datos adjuntos](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="c1ed7-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="c1ed7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c1ed7-112">Parent elements</span></span>

<span data-ttu-id="c1ed7-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c1ed7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c1ed7-114">Remarks</span></span>

<span data-ttu-id="c1ed7-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="c1ed7-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c1ed7-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c1ed7-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c1ed7-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c1ed7-118">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c1ed7-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c1ed7-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c1ed7-119">Schema name</span></span>  <br/> |<span data-ttu-id="c1ed7-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c1ed7-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c1ed7-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c1ed7-121">Validation file</span></span>  <br/> |<span data-ttu-id="c1ed7-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c1ed7-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c1ed7-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c1ed7-123">Can be empty</span></span>  <br/> |<span data-ttu-id="c1ed7-124">falso</span><span class="sxs-lookup"><span data-stu-id="c1ed7-124">false</span></span>  <br/> |
   

