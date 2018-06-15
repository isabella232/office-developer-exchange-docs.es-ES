---
title: IsExternalMailbox
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5cc83174-e684-42c8-b72a-f82d3de3bb2f
description: El elemento IsExternalMailbox indica si el buzón de correo es externo a la organización.
ms.openlocfilehash: cf9f71e9b955cffd1bebefd5f23acba66ba1b894
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19836010"
---
# <a name="isexternalmailbox"></a><span data-ttu-id="05193-103">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="05193-103">IsExternalMailbox</span></span>

<span data-ttu-id="05193-104">El elemento **IsExternalMailbox** indica si el buzón de correo es externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="05193-104">The **IsExternalMailbox** element indicates whether the mailbox is external to the organization.</span></span> 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 <span data-ttu-id="05193-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="05193-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05193-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="05193-106">Attributes and elements</span></span>

<span data-ttu-id="05193-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="05193-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05193-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="05193-108">Attributes</span></span>

<span data-ttu-id="05193-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05193-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05193-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="05193-110">Child elements</span></span>

<span data-ttu-id="05193-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="05193-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="05193-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="05193-112">Parent elements</span></span>

[<span data-ttu-id="05193-113">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="05193-113">SearchableMailbox</span></span>](searchablemailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="05193-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="05193-114">Text value</span></span>

<span data-ttu-id="05193-115">Un valor de texto de **true** para el elemento **IsExternalMailbox** indica que el buzón está en una organización externa.</span><span class="sxs-lookup"><span data-stu-id="05193-115">A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization.</span></span> <span data-ttu-id="05193-116">Un valor de **false** indica que el buzón está en la organización.</span><span class="sxs-lookup"><span data-stu-id="05193-116">A value of **false** indicates that the mailbox is in the organization.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="05193-117">Notas</span><span class="sxs-lookup"><span data-stu-id="05193-117">Remarks</span></span>

<span data-ttu-id="05193-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="05193-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="05193-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="05193-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05193-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="05193-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05193-121">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="05193-121">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05193-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="05193-122">Schema name</span></span>  <br/> |<span data-ttu-id="05193-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="05193-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="05193-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="05193-124">Validation file</span></span>  <br/> |<span data-ttu-id="05193-125">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05193-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05193-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="05193-126">Can be empty</span></span>  <br/> |<span data-ttu-id="05193-127">False</span><span class="sxs-lookup"><span data-stu-id="05193-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05193-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="05193-128">See also</span></span>



- [<span data-ttu-id="05193-129">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="05193-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

