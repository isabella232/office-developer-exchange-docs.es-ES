---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: El elemento PolicyTag especifica el identificador de retención en una carpeta o elemento.
ms.openlocfilehash: d6cd5aab1145f6006912541c8f8c1d0a91d1e17e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19836835"
---
# <a name="policytag"></a><span data-ttu-id="67acb-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="67acb-103">PolicyTag</span></span>

<span data-ttu-id="67acb-104">El elemento **PolicyTag** especifica el identificador de retención en una carpeta o elemento.</span><span class="sxs-lookup"><span data-stu-id="67acb-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="67acb-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="67acb-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="67acb-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="67acb-106">Attributes and elements</span></span>

<span data-ttu-id="67acb-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="67acb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="67acb-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="67acb-108">Attributes</span></span>

|<span data-ttu-id="67acb-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="67acb-109">**Attribute**</span></span>|<span data-ttu-id="67acb-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="67acb-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="67acb-111">IsExplicit</span><span class="sxs-lookup"><span data-stu-id="67acb-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="67acb-112">Indica si una etiqueta de directiva se estableció explícitamente en un elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="67acb-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="67acb-113">Un valor de texto de **true** para el atributo **IsExplicit** indica que la etiqueta de directiva se establezca explícitamente en el elemento o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="67acb-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="67acb-114">Un valor de texto de **false** indica que la etiqueta de directiva implícitamente se estableció en el elemento o la carpeta en función de la etiqueta de directiva de carpeta primaria.</span><span class="sxs-lookup"><span data-stu-id="67acb-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="67acb-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="67acb-115">Child elements</span></span>

<span data-ttu-id="67acb-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="67acb-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="67acb-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="67acb-117">Parent elements</span></span>

<span data-ttu-id="67acb-118">[SearchPreviewItem](searchpreviewitem.md) | [elemento](item.md) | [contacto](contact.md) | [mensaje](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="67acb-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="67acb-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="67acb-119">Text value</span></span>

<span data-ttu-id="67acb-120">El valor de texto del elemento **PolicyTag** es el identificador de etiqueta de directiva.</span><span class="sxs-lookup"><span data-stu-id="67acb-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="67acb-121">El identificador de etiqueta de directiva es un GUID.</span><span class="sxs-lookup"><span data-stu-id="67acb-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="67acb-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="67acb-122">Remarks</span></span>

<span data-ttu-id="67acb-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="67acb-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="67acb-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="67acb-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="67acb-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="67acb-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="67acb-126">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="67acb-126">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="67acb-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="67acb-127">Schema name</span></span>  <br/> |<span data-ttu-id="67acb-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="67acb-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="67acb-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="67acb-129">Validation file</span></span>  <br/> |<span data-ttu-id="67acb-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="67acb-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="67acb-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="67acb-131">Can be empty</span></span>  <br/> ||
   

