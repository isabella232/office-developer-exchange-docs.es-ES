---
title: EndWallClock
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc04e44e-e6d1-4355-a2b1-feb6663dc647
description: El elemento EndWallClock especifica la hora de finalización de una reunión en la zona horaria de la ubicación en la que lleva a cabo la reunión.
ms.openlocfilehash: 10e4a2bde50354b2f2752751c01a6a70aa084d05
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764414"
---
# <a name="endwallclock"></a><span data-ttu-id="9abfe-103">EndWallClock</span><span class="sxs-lookup"><span data-stu-id="9abfe-103">EndWallClock</span></span>

<span data-ttu-id="9abfe-104">El elemento **EndWallClock** especifica la hora de finalización de una reunión en la zona horaria de la ubicación en la que lleva a cabo la reunión.</span><span class="sxs-lookup"><span data-stu-id="9abfe-104">The **EndWallClock** element specifies the end time of a meeting in the time zone of the location in which the meeting takes place.</span></span> 
  
```XML
<EndWallClock></EndWallClock>
```

 <span data-ttu-id="9abfe-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="9abfe-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9abfe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9abfe-106">Attributes and elements</span></span>

<span data-ttu-id="9abfe-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9abfe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9abfe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9abfe-108">Attributes</span></span>

<span data-ttu-id="9abfe-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9abfe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9abfe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9abfe-110">Child elements</span></span>

<span data-ttu-id="9abfe-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9abfe-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="9abfe-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9abfe-112">Parent elements</span></span>

|<span data-ttu-id="9abfe-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9abfe-113">**Element**</span></span>|<span data-ttu-id="9abfe-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9abfe-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9abfe-115">Rol</span><span class="sxs-lookup"><span data-stu-id="9abfe-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="9abfe-116">Especifica un conjunto de datos de rol devueltos por una solicitud de **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="9abfe-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9abfe-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="9abfe-117">Text value</span></span>

<span data-ttu-id="9abfe-118">El valor de texto del elemento **EndWallClock** es un valor de tipo string que especifica el identificador de zona horaria.</span><span class="sxs-lookup"><span data-stu-id="9abfe-118">The text value of the **EndWallClock** element is a string value that specifies the time zone identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9abfe-119">Notas</span><span class="sxs-lookup"><span data-stu-id="9abfe-119">Remarks</span></span>

<span data-ttu-id="9abfe-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="9abfe-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="9abfe-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="9abfe-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9abfe-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9abfe-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9abfe-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9abfe-123">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9abfe-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9abfe-124">Schema Name</span></span>  <br/> |<span data-ttu-id="9abfe-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="9abfe-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="9abfe-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9abfe-126">Validation File</span></span>  <br/> |<span data-ttu-id="9abfe-127">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9abfe-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="9abfe-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9abfe-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="9abfe-129">Ver también</span><span class="sxs-lookup"><span data-stu-id="9abfe-129">See also</span></span>



- [<span data-ttu-id="9abfe-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9abfe-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

