---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: El elemento IncludeUnsearchableItems especifica si se deben incluir los elementos que no se pueden buscar.
ms.openlocfilehash: 19fe450f5b1647be2df75138dbe67dd9e1c05c21
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465705"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="2798e-103">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="2798e-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="2798e-104">El elemento **IncludeUnsearchableItems** especifica si se deben incluir los elementos que no se pueden buscar.</span><span class="sxs-lookup"><span data-stu-id="2798e-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="2798e-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2798e-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="2798e-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="2798e-106">Attributes and elements</span></span>

<span data-ttu-id="2798e-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="2798e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2798e-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="2798e-108">Attributes</span></span>

<span data-ttu-id="2798e-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2798e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="2798e-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="2798e-110">Child elements</span></span>

<span data-ttu-id="2798e-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="2798e-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="2798e-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="2798e-112">Parent elements</span></span>

|<span data-ttu-id="2798e-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="2798e-113">**Element**</span></span>|<span data-ttu-id="2798e-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2798e-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2798e-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="2798e-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="2798e-116">Especifica una solicitud para buscar estadísticas de buzón por palabra clave.</span><span class="sxs-lookup"><span data-stu-id="2798e-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="2798e-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="2798e-117">Text value</span></span>

<span data-ttu-id="2798e-118">Un valor de texto de **true** para el elemento **IncludeUnsearchableItems** indica que no se incluyen estadísticas para los elementos que no se pueden buscar.</span><span class="sxs-lookup"><span data-stu-id="2798e-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="2798e-119">Un valor de **false** indica que se incluyen estadísticas para los elementos que no se pueden buscar.</span><span class="sxs-lookup"><span data-stu-id="2798e-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2798e-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2798e-120">Remarks</span></span>

<span data-ttu-id="2798e-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="2798e-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="2798e-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="2798e-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2798e-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="2798e-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2798e-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="2798e-124">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="2798e-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="2798e-125">Schema Name</span></span>  <br/> |<span data-ttu-id="2798e-126">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="2798e-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="2798e-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="2798e-127">Validation File</span></span>  <br/> |<span data-ttu-id="2798e-128">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="2798e-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="2798e-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="2798e-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="2798e-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2798e-130">See also</span></span>



- [<span data-ttu-id="2798e-131">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="2798e-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

