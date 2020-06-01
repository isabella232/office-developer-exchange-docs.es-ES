---
title: EndWallClock
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bc04e44e-e6d1-4355-a2b1-feb6663dc647
description: El elemento EndWallClock especifica la hora de finalización de una reunión en la zona horaria de la ubicación en la que tiene lugar la reunión.
ms.openlocfilehash: 48b762d0bfe367b966b6f1790230f6a2118c3fd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462974"
---
# <a name="endwallclock"></a><span data-ttu-id="e69b7-103">EndWallClock</span><span class="sxs-lookup"><span data-stu-id="e69b7-103">EndWallClock</span></span>

<span data-ttu-id="e69b7-104">El elemento **EndWallClock** especifica la hora de finalización de una reunión en la zona horaria de la ubicación en la que tiene lugar la reunión.</span><span class="sxs-lookup"><span data-stu-id="e69b7-104">The **EndWallClock** element specifies the end time of a meeting in the time zone of the location in which the meeting takes place.</span></span> 
  
```XML
<EndWallClock></EndWallClock>
```

 <span data-ttu-id="e69b7-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="e69b7-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e69b7-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="e69b7-106">Attributes and elements</span></span>

<span data-ttu-id="e69b7-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="e69b7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e69b7-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="e69b7-108">Attributes</span></span>

<span data-ttu-id="e69b7-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e69b7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e69b7-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="e69b7-110">Child elements</span></span>

<span data-ttu-id="e69b7-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="e69b7-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="e69b7-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="e69b7-112">Parent elements</span></span>

|<span data-ttu-id="e69b7-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="e69b7-113">**Element**</span></span>|<span data-ttu-id="e69b7-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="e69b7-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e69b7-115">Rol</span><span class="sxs-lookup"><span data-stu-id="e69b7-115">Persona</span></span>](persona.md) <br/> |<span data-ttu-id="e69b7-116">Especifica un conjunto de datos de rol devueltos por una solicitud **GetPersona** .</span><span class="sxs-lookup"><span data-stu-id="e69b7-116">Specifies a set of persona data returned by a **GetPersona** request.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="e69b7-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="e69b7-117">Text value</span></span>

<span data-ttu-id="e69b7-118">El valor de texto del elemento **EndWallClock** es un valor de cadena que especifica el identificador de la zona horaria.</span><span class="sxs-lookup"><span data-stu-id="e69b7-118">The text value of the **EndWallClock** element is a string value that specifies the time zone identifier.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e69b7-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e69b7-119">Remarks</span></span>

<span data-ttu-id="e69b7-120">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="e69b7-120">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="e69b7-121">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="e69b7-121">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e69b7-122">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="e69b7-122">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e69b7-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e69b7-123">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e69b7-124">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="e69b7-124">Schema Name</span></span>  <br/> |<span data-ttu-id="e69b7-125">Esquema de tipo</span><span class="sxs-lookup"><span data-stu-id="e69b7-125">Type schema</span></span>  <br/> |
|<span data-ttu-id="e69b7-126">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="e69b7-126">Validation File</span></span>  <br/> |<span data-ttu-id="e69b7-127">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="e69b7-127">types.xsd</span></span>  <br/> |
|<span data-ttu-id="e69b7-128">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="e69b7-128">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="e69b7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="e69b7-129">See also</span></span>



- [<span data-ttu-id="e69b7-130">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="e69b7-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

