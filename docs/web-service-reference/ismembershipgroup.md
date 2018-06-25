---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: El elemento IsMembershipGroup especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón de correo.
ms.openlocfilehash: 03ab0dc75d2c798b7f2afeef85aa45f0349be70a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836050"
---
# <a name="ismembershipgroup"></a><span data-ttu-id="e157f-103">IsMembershipGroup</span><span class="sxs-lookup"><span data-stu-id="e157f-103">IsMembershipGroup</span></span>

<span data-ttu-id="e157f-104">El elemento **IsMembershipGroup** especifica un valor booleano que indica si la entidad es un grupo de distribución o un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e157f-104">The **IsMembershipGroup** element specifies a Boolean value that indicates whether the entity is a distribution group or a mailbox.</span></span> 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
```

 <span data-ttu-id="e157f-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e157f-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e157f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e157f-106">Attributes and elements</span></span>

<span data-ttu-id="e157f-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e157f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e157f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e157f-108">Attributes</span></span>

<span data-ttu-id="e157f-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e157f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e157f-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e157f-110">Child elements</span></span>

<span data-ttu-id="e157f-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e157f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e157f-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e157f-112">Parent elements</span></span>

|<span data-ttu-id="e157f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e157f-113">**Element**</span></span>|<span data-ttu-id="e157f-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e157f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e157f-115">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="e157f-115">SearchableMailbox</span></span>](searchablemailbox.md) <br/> |<span data-ttu-id="e157f-116">Especifica un buzón de correo devuelto desde una solicitud de **GetSearchableMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="e157f-116">Specifies a mailbox returned from a **GetSearchableMailboxes** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e157f-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e157f-117">Text value</span></span>

<span data-ttu-id="e157f-118">Un valor de texto de **true** para el elemento **IsMembershipGroup** indica que la entidad es un grupo de distribución o un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e157f-118">A text value of **true** for the **IsMembershipGroup** element indicates that the entity is a distribution group or a mailbox.</span></span> <span data-ttu-id="e157f-119">Un valor de false indica que la entidad no es un grupo de distribución o un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="e157f-119">A value of false indicates that the entity is not a distribution group or a mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e157f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e157f-120">Remarks</span></span>

<span data-ttu-id="e157f-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e157f-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e157f-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e157f-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e157f-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e157f-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e157f-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e157f-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e157f-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e157f-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e157f-126">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e157f-126">Type schema</span></span>  <br/> |
|<span data-ttu-id="e157f-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e157f-127">Validation File</span></span>  <br/> |<span data-ttu-id="e157f-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e157f-128">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e157f-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e157f-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e157f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="e157f-130">See also</span></span>



- [<span data-ttu-id="e157f-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e157f-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

