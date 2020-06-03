---
title: UpdateItemInRecoverableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c49816b1-dbb5-4716-86c7-30790e86f30e
description: El elemento UpdateItemInRecoverableItems especifica una solicitud para actualizar un elemento en elementos recuperables.
ms.openlocfilehash: f3dae55097c613b84a80795185baad559e312b90
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459787"
---
# <a name="updateiteminrecoverableitems"></a><span data-ttu-id="6b2ef-103">UpdateItemInRecoverableItems</span><span class="sxs-lookup"><span data-stu-id="6b2ef-103">UpdateItemInRecoverableItems</span></span>

<span data-ttu-id="6b2ef-104">El elemento **UpdateItemInRecoverableItems** especifica una solicitud para actualizar un elemento en elementos recuperables.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-104">The **UpdateItemInRecoverableItems** element specifies a request to update an item in recoverable items.</span></span> 
  
```XML
<UpdateItemInRecoverableItems>
   <ItemId/>
   <Updates/>
   <Attachments/>
   <MakeItemImmutable/>
</UpdateItemInRecoverableItems>
```

 <span data-ttu-id="6b2ef-105">**UpdateItemInRecoverableItemsType**</span><span class="sxs-lookup"><span data-stu-id="6b2ef-105">**UpdateItemInRecoverableItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="6b2ef-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="6b2ef-106">Attributes and elements</span></span>

<span data-ttu-id="6b2ef-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6b2ef-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="6b2ef-108">Attributes</span></span>

<span data-ttu-id="6b2ef-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="6b2ef-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="6b2ef-110">Child elements</span></span>

<span data-ttu-id="6b2ef-111">[Itemid](itemid.md)  |  [Actualizaciones (elemento)](updates-item.md)  |  [Datos adjuntos](attachments-ex15websvcsotherref.md)  |  [MakeItemImmutable](makeitemimmutable.md)</span><span class="sxs-lookup"><span data-stu-id="6b2ef-111">[ItemId](itemid.md) | [Updates (Item)](updates-item.md) | [Attachments](attachments-ex15websvcsotherref.md) | [MakeItemImmutable](makeitemimmutable.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="6b2ef-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="6b2ef-112">Parent elements</span></span>

<span data-ttu-id="6b2ef-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6b2ef-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6b2ef-114">Remarks</span></span>

<span data-ttu-id="6b2ef-115">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="6b2ef-116">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="6b2ef-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6b2ef-117">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="6b2ef-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6b2ef-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b2ef-118">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="6b2ef-119">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="6b2ef-119">Schema name</span></span>  <br/> |<span data-ttu-id="6b2ef-120">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="6b2ef-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="6b2ef-121">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="6b2ef-121">Validation file</span></span>  <br/> |<span data-ttu-id="6b2ef-122">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="6b2ef-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="6b2ef-123">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="6b2ef-123">Can be empty</span></span>  <br/> |<span data-ttu-id="6b2ef-124">false</span><span class="sxs-lookup"><span data-stu-id="6b2ef-124">false</span></span>  <br/> |
   

