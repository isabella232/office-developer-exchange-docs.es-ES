---
title: IncludeUnsearchableItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9a9bd2dc-f5b9-4b82-a6a0-f643d2951080
description: El elemento IncludeUnsearchableItems especifica si se incluyen los elementos que no se puede buscar.
ms.openlocfilehash: 4c6b9b3752330bf914c9901d2e8f69e93546fec6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835907"
---
# <a name="includeunsearchableitems"></a><span data-ttu-id="e8282-103">IncludeUnsearchableItems</span><span class="sxs-lookup"><span data-stu-id="e8282-103">IncludeUnsearchableItems</span></span>

<span data-ttu-id="e8282-104">El elemento **IncludeUnsearchableItems** especifica si se incluyen los elementos que no se puede buscar.</span><span class="sxs-lookup"><span data-stu-id="e8282-104">The **IncludeUnsearchableItems** element specifies whether to include items that cannot be searched.</span></span> 
  
```XML
<IncludeUnsearchableItems>true | false</IncludeUnsearchableItems>
```

 <span data-ttu-id="e8282-105">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e8282-105">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e8282-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e8282-106">Attributes and elements</span></span>

<span data-ttu-id="e8282-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e8282-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e8282-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e8282-108">Attributes</span></span>

<span data-ttu-id="e8282-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8282-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e8282-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e8282-110">Child elements</span></span>

<span data-ttu-id="e8282-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="e8282-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e8282-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e8282-112">Parent elements</span></span>

|<span data-ttu-id="e8282-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e8282-113">**Element**</span></span>|<span data-ttu-id="e8282-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e8282-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e8282-115">FindMailboxStatisticsByKeywords</span><span class="sxs-lookup"><span data-stu-id="e8282-115">FindMailboxStatisticsByKeywords</span></span>](findmailboxstatisticsbykeywords.md) <br/> |<span data-ttu-id="e8282-116">Especifica una solicitud para buscar las estadísticas de buzón de correo por palabra clave.</span><span class="sxs-lookup"><span data-stu-id="e8282-116">Specifies a request to search for mailbox statistics by keyword.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e8282-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e8282-117">Text value</span></span>

<span data-ttu-id="e8282-118">Un valor de texto de **true** para el elemento **IncludeUnsearchableItems** indica que no se incluyen para los elementos que no se pueden buscar las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="e8282-118">A text value of **true** for the **IncludeUnsearchableItems** element indicates that statistics are not included for items that are not searchable.</span></span> <span data-ttu-id="e8282-119">Un valor de **false** indica que las estadísticas se incluyen para los elementos que no se pueden buscar.</span><span class="sxs-lookup"><span data-stu-id="e8282-119">A value of **false** indicates that statistics are included for items that are not searchable.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e8282-120">Notas</span><span class="sxs-lookup"><span data-stu-id="e8282-120">Remarks</span></span>

<span data-ttu-id="e8282-121">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e8282-121">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e8282-122">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e8282-122">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e8282-123">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e8282-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e8282-124">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8282-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e8282-125">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e8282-125">Schema Name</span></span>  <br/> |<span data-ttu-id="e8282-126">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="e8282-126">Message schema</span></span>  <br/> |
|<span data-ttu-id="e8282-127">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e8282-127">Validation File</span></span>  <br/> |<span data-ttu-id="e8282-128">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e8282-128">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e8282-129">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e8282-129">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e8282-130">Ver también</span><span class="sxs-lookup"><span data-stu-id="e8282-130">See also</span></span>



- [<span data-ttu-id="e8282-131">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="e8282-131">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

