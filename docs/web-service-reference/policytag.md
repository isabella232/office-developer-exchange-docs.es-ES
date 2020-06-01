---
title: PolicyTag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: fa4b1447-dc7b-47ad-a677-78fcee443dc6
description: El elemento PolicyTag especifica el identificador de retención de un elemento o una carpeta.
ms.openlocfilehash: ddc4d890d1e514586ba5ea7f6a8b541b2e4786c7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460900"
---
# <a name="policytag"></a><span data-ttu-id="73a29-103">PolicyTag</span><span class="sxs-lookup"><span data-stu-id="73a29-103">PolicyTag</span></span>

<span data-ttu-id="73a29-104">El elemento **PolicyTag** especifica el identificador de retención de un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="73a29-104">The **PolicyTag** element specifies the retention identifier on an item or folder.</span></span> 
  
```xml
<PolicyTag IsExplicit="true | false"></PolicyTag>
```

 <span data-ttu-id="73a29-105">**RetentionTagType**</span><span class="sxs-lookup"><span data-stu-id="73a29-105">**RetentionTagType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73a29-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="73a29-106">Attributes and elements</span></span>

<span data-ttu-id="73a29-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="73a29-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73a29-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="73a29-108">Attributes</span></span>

|<span data-ttu-id="73a29-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="73a29-109">**Attribute**</span></span>|<span data-ttu-id="73a29-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73a29-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73a29-111">IsExplicit</span><span class="sxs-lookup"><span data-stu-id="73a29-111">IsExplicit</span></span>  <br/> |<span data-ttu-id="73a29-112">Indica si una etiqueta de Directiva se estableció explícitamente en un elemento o una carpeta.</span><span class="sxs-lookup"><span data-stu-id="73a29-112">Indicates whether a policy tag was explicitly set on an item or folder.</span></span>  <br/> <span data-ttu-id="73a29-113">Un valor de texto de **true** para el atributo **IsExplicit** indica que la etiqueta de Directiva se estableció explícitamente en el elemento o carpeta.</span><span class="sxs-lookup"><span data-stu-id="73a29-113">A text value of **true** for the **IsExplicit** attribute indicates that the policy tag was explicitly set on the item or folder.</span></span> <span data-ttu-id="73a29-114">Un valor de texto **falso** indica que la etiqueta de Directiva se ha configurado implícitamente en el elemento o la carpeta basándose en la etiqueta de directiva de carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="73a29-114">A text value of **false** indicates that the policy tag was implicitly set on the item or folder based on the parent folder policy tag.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73a29-115">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73a29-115">Child elements</span></span>

<span data-ttu-id="73a29-116">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="73a29-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73a29-117">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="73a29-117">Parent elements</span></span>

<span data-ttu-id="73a29-118">[SearchPreviewItem](searchpreviewitem.md)  |  [Elemento](item.md)  |  [Contacto](contact.md)  |  [Mensaje de error](message-ex15websvcsotherref.md)  |  [DistributionList](distributionlist.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Tarea](task.md)</span><span class="sxs-lookup"><span data-stu-id="73a29-118">[SearchPreviewItem](searchpreviewitem.md) | [Item](item.md) | [Contact](contact.md) | [Message](message-ex15websvcsotherref.md) | [DistributionList](distributionlist.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Task](task.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="73a29-119">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="73a29-119">Text value</span></span>

<span data-ttu-id="73a29-120">El valor de texto del elemento **PolicyTag** es el identificador de la etiqueta de directiva.</span><span class="sxs-lookup"><span data-stu-id="73a29-120">The text value of the **PolicyTag** element is the policy tag identifier.</span></span> <span data-ttu-id="73a29-121">El identificador de etiqueta de directiva es un GUID.</span><span class="sxs-lookup"><span data-stu-id="73a29-121">The policy tag identifier is a GUID.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="73a29-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73a29-122">Remarks</span></span>

<span data-ttu-id="73a29-123">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="73a29-123">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="73a29-124">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="73a29-124">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73a29-125">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="73a29-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73a29-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="73a29-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73a29-127">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="73a29-127">Schema name</span></span>  <br/> |<span data-ttu-id="73a29-128">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="73a29-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="73a29-129">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="73a29-129">Validation file</span></span>  <br/> |<span data-ttu-id="73a29-130">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="73a29-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73a29-131">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73a29-131">Can be empty</span></span>  <br/> ||
   

