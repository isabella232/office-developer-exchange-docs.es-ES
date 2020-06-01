---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'El elemento FindPeople especifica un conjunto de datos que se usa en una solicitud de FindPeople. Los datos incluyen cero o más de los siguientes elementos: una forma persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), un identificador de carpeta principal y una cadena de consulta (opcional).'
ms.openlocfilehash: 4777601b7146ec857b5c79fa9d4ced59a7247889
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462904"
---
# <a name="findpeople"></a><span data-ttu-id="2f3bc-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="2f3bc-104">FindPeople</span></span>

<span data-ttu-id="2f3bc-105">El elemento **FindPeople** especifica un conjunto de datos que se usa en una solicitud de FindPeople.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="2f3bc-106">Los datos incluyen cero o más de los siguientes elementos: una forma persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), un identificador de carpeta principal y una cadena de consulta (opcional).</span><span class="sxs-lookup"><span data-stu-id="2f3bc-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
```XML
<FindPeople>
   <PersonaShape/>
   <IndexedPageItemView/>
   <Restriction/>
   <AggregationRestriction/>
   <SortOrder/>
   <ParentFolderId/>
   <QueryString/>
</FindPeople>
```

 <span data-ttu-id="2f3bc-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="2f3bc-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2f3bc-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2f3bc-108">Attributes and elements</span></span>

<span data-ttu-id="2f3bc-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2f3bc-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="2f3bc-110">Attributes</span></span>

<span data-ttu-id="2f3bc-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2f3bc-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2f3bc-112">Child elements</span></span>

<span data-ttu-id="2f3bc-113">[PersonaShape](personashape.md)  |  [IndexedPageItemView](indexedpageitemview.md)  |  [Restricción](restriction.md)  |  [AggregationRestriction](aggregationrestriction.md)  |  [SortOrder](sortorder.md)  |  [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [QueryString (QueryStringType)](querystring-querystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="2f3bc-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2f3bc-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2f3bc-114">Parent elements</span></span>

<span data-ttu-id="2f3bc-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f3bc-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f3bc-116">Remarks</span></span>

<span data-ttu-id="2f3bc-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2f3bc-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2f3bc-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f3bc-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2f3bc-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f3bc-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f3bc-120">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2f3bc-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2f3bc-121">Schema name</span></span>  <br/> |<span data-ttu-id="2f3bc-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2f3bc-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="2f3bc-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2f3bc-123">Validation file</span></span>  <br/> |<span data-ttu-id="2f3bc-124">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2f3bc-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2f3bc-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2f3bc-125">Can be empty</span></span>  <br/> |<span data-ttu-id="2f3bc-126">false</span><span class="sxs-lookup"><span data-stu-id="2f3bc-126">false</span></span>  <br/> |
   

