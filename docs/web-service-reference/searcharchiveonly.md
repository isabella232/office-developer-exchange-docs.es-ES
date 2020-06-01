---
title: SearchArchiveOnly
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cce5344c-b622-44d4-bc14-a0de346c9335
description: El elemento SearchArchiveOnly indica si sólo se busca en el buzón de archivo los elementos que no se pueden indizar.
ms.openlocfilehash: 9014044ed06c697cc43dd62103d7a1a907bda5a8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460501"
---
# <a name="searcharchiveonly"></a><span data-ttu-id="20214-103">SearchArchiveOnly</span><span class="sxs-lookup"><span data-stu-id="20214-103">SearchArchiveOnly</span></span>

<span data-ttu-id="20214-104">El elemento **SearchArchiveOnly** indica si sólo se busca en el buzón de archivo los elementos que no se pueden indizar.</span><span class="sxs-lookup"><span data-stu-id="20214-104">The **SearchArchiveOnly** element indicates whether only the archive mailbox is searched for non-indexable items.</span></span> 
  
```xml
<SearchArchiveOnly>true | false</SearchArchiveOnly>
```

 <span data-ttu-id="20214-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="20214-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="20214-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="20214-106">Attributes and elements</span></span>

<span data-ttu-id="20214-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="20214-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="20214-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="20214-108">Attributes</span></span>

<span data-ttu-id="20214-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20214-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="20214-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="20214-110">Child elements</span></span>

<span data-ttu-id="20214-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="20214-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="20214-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="20214-112">Parent elements</span></span>

<span data-ttu-id="20214-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span><span class="sxs-lookup"><span data-stu-id="20214-113">[GetNonIndexableItemStatistics](getnonindexableitemstatistics.md) │ [GetNonIndexableItemDetails](getnonindexableitemdetails.md)</span></span>
  
## <a name="text-value"></a><span data-ttu-id="20214-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="20214-114">Text value</span></span>

<span data-ttu-id="20214-115">Un valor de texto de **true** para el elemento **SearchArchiveOnly** indica que la búsqueda de elementos no indexables solo se realiza en el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="20214-115">A text value of **true** for the **SearchArchiveOnly** element indicates that non-indexable item search is only performed on the archive mailbox.</span></span> <span data-ttu-id="20214-116">Un valor de texto **falso** indica que la búsqueda se realiza en el buzón principal y en el buzón de archivo.</span><span class="sxs-lookup"><span data-stu-id="20214-116">A text value of **false** indicates that the search is performed against the primary mailbox and archive mailbox.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20214-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="20214-117">Remarks</span></span>

<span data-ttu-id="20214-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="20214-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="20214-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="20214-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="20214-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="20214-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="20214-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="20214-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="20214-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="20214-122">Schema name</span></span>  <br/> |<span data-ttu-id="20214-123">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="20214-123">Messages schema</span></span>  <br/> |
|<span data-ttu-id="20214-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="20214-124">Validation file</span></span>  <br/> |<span data-ttu-id="20214-125">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="20214-125">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="20214-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="20214-126">Can be empty</span></span>  <br/> ||
   

