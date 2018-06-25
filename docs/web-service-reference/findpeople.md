---
title: FindPeople
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 12c70441-77b9-4619-8e66-1b7e3a63ba48
description: 'El elemento FindPeople especifica un conjunto de datos usados en una solicitud de FindPeople. Los datos incluyen cero o más de los siguientes elementos: una forma de persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), una carpeta principal identificador y una cadena de consulta (opcional).'
ms.openlocfilehash: 79c8a4324cd217232442b781c33223296d8015e5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764647"
---
# <a name="findpeople"></a><span data-ttu-id="ab0e3-104">FindPeople</span><span class="sxs-lookup"><span data-stu-id="ab0e3-104">FindPeople</span></span>

<span data-ttu-id="ab0e3-105">El elemento **FindPeople** especifica un conjunto de datos usados en una solicitud de FindPeople.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-105">The **FindPeople** element specifies a set of data used in a FindPeople request.</span></span> <span data-ttu-id="ab0e3-106">Los datos incluyen cero o más de los siguientes elementos: una forma de persona (opcional), una vista de elemento de página indizada, una restricción (opcional), una restricción de agregación (opcional), un criterio de ordenación (opcional), una carpeta principal identificador y una cadena de consulta (opcional).</span><span class="sxs-lookup"><span data-stu-id="ab0e3-106">The data includes zero or more of the following elements: a persona shape (optional), an indexed page item view, a restriction (optional), an aggregation restriction (optional), a sort order (optional), a parent folder Id, and a query string (optional).</span></span> 
  
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

 <span data-ttu-id="ab0e3-107">**FindPeopleType**</span><span class="sxs-lookup"><span data-stu-id="ab0e3-107">**FindPeopleType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab0e3-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ab0e3-108">Attributes and elements</span></span>

<span data-ttu-id="ab0e3-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab0e3-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="ab0e3-110">Attributes</span></span>

<span data-ttu-id="ab0e3-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab0e3-112">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ab0e3-112">Child elements</span></span>

<span data-ttu-id="ab0e3-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [restricción](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ID (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)  |  [ QueryString (QueryStringType)](querystring-querystringtype.md)</span><span class="sxs-lookup"><span data-stu-id="ab0e3-113">[PersonaShape](personashape.md) | [IndexedPageItemView](indexedpageitemview.md) | [Restriction](restriction.md) | [AggregationRestriction](aggregationrestriction.md) | [SortOrder](sortorder.md) | [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) | [QueryString (QueryStringType)](querystring-querystringtype.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="ab0e3-114">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ab0e3-114">Parent elements</span></span>

<span data-ttu-id="ab0e3-115">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-115">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ab0e3-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ab0e3-116">Remarks</span></span>

<span data-ttu-id="ab0e3-117">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="ab0e3-118">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ab0e3-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab0e3-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ab0e3-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab0e3-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ab0e3-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ab0e3-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ab0e3-121">Schema name</span></span>  <br/> |<span data-ttu-id="ab0e3-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ab0e3-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ab0e3-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ab0e3-123">Validation file</span></span>  <br/> |<span data-ttu-id="ab0e3-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ab0e3-124">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ab0e3-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ab0e3-125">Can be empty</span></span>  <br/> |<span data-ttu-id="ab0e3-126">falso</span><span class="sxs-lookup"><span data-stu-id="ab0e3-126">false</span></span>  <br/> |
   

