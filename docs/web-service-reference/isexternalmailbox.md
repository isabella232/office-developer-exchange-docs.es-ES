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
ms.openlocfilehash: 9be702b05e89857913023a8ec34b78ea4c309274
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455292"
---
# <a name="isexternalmailbox"></a><span data-ttu-id="cdb51-103">IsExternalMailbox</span><span class="sxs-lookup"><span data-stu-id="cdb51-103">IsExternalMailbox</span></span>

<span data-ttu-id="cdb51-104">El elemento **IsExternalMailbox** indica si el buzón de correo es externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="cdb51-104">The **IsExternalMailbox** element indicates whether the mailbox is external to the organization.</span></span> 
  
```XML
<IsExternalMailbox>true | false</IsExternalMailbox>
```

 <span data-ttu-id="cdb51-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="cdb51-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cdb51-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="cdb51-106">Attributes and elements</span></span>

<span data-ttu-id="cdb51-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="cdb51-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cdb51-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="cdb51-108">Attributes</span></span>

<span data-ttu-id="cdb51-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdb51-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cdb51-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cdb51-110">Child elements</span></span>

<span data-ttu-id="cdb51-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="cdb51-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cdb51-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="cdb51-112">Parent elements</span></span>

[<span data-ttu-id="cdb51-113">SearchableMailbox</span><span class="sxs-lookup"><span data-stu-id="cdb51-113">SearchableMailbox</span></span>](searchablemailbox.md)
  
## <a name="text-value"></a><span data-ttu-id="cdb51-114">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="cdb51-114">Text value</span></span>

<span data-ttu-id="cdb51-115">Un valor de texto de **true** para el elemento **IsExternalMailbox** indica que el buzón de correo está en una organización externa.</span><span class="sxs-lookup"><span data-stu-id="cdb51-115">A text value of **true** for the **IsExternalMailbox** element indicates that the mailbox is in an external organization.</span></span> <span data-ttu-id="cdb51-116">Un valor de **false** indica que el buzón de correo está en la organización.</span><span class="sxs-lookup"><span data-stu-id="cdb51-116">A value of **false** indicates that the mailbox is in the organization.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cdb51-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cdb51-117">Remarks</span></span>

<span data-ttu-id="cdb51-118">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="cdb51-118">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="cdb51-119">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="cdb51-119">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cdb51-120">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="cdb51-120">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cdb51-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdb51-121">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cdb51-122">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="cdb51-122">Schema name</span></span>  <br/> |<span data-ttu-id="cdb51-123">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="cdb51-123">Types schema</span></span>  <br/> |
|<span data-ttu-id="cdb51-124">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="cdb51-124">Validation file</span></span>  <br/> |<span data-ttu-id="cdb51-125">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="cdb51-125">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cdb51-126">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="cdb51-126">Can be empty</span></span>  <br/> |<span data-ttu-id="cdb51-127">Falso</span><span class="sxs-lookup"><span data-stu-id="cdb51-127">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cdb51-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cdb51-128">See also</span></span>



- [<span data-ttu-id="cdb51-129">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="cdb51-129">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

