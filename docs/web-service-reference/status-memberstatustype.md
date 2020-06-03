---
title: Estado (MemberStatusType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Status
api_type:
- schema
ms.assetid: 4f8a860b-0a48-4a0d-9a7a-69a0304aa747
description: El elemento status proporciona información sobre el estado de un miembro de la lista de distribución en el servidor.
ms.openlocfilehash: bfa0c349d6af51c1b2238c9749d2656541d31906
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465467"
---
# <a name="status-memberstatustype"></a><span data-ttu-id="626ab-103">Estado (MemberStatusType)</span><span class="sxs-lookup"><span data-stu-id="626ab-103">Status (MemberStatusType)</span></span>

<span data-ttu-id="626ab-104">El elemento **status** proporciona información sobre el estado de un miembro de la lista de distribución en el servidor.</span><span class="sxs-lookup"><span data-stu-id="626ab-104">The **Status** element provides information about the status of a distribution list member on the server.</span></span> 
  
```
<Status>Unrecognized or Normal or Demoted</Status>
```

 <span data-ttu-id="626ab-105">**MemberStatusType**</span><span class="sxs-lookup"><span data-stu-id="626ab-105">**MemberStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="626ab-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="626ab-106">Attributes and elements</span></span>

<span data-ttu-id="626ab-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="626ab-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="626ab-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="626ab-108">Attributes</span></span>

<span data-ttu-id="626ab-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="626ab-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="626ab-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="626ab-110">Child elements</span></span>

<span data-ttu-id="626ab-111">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="626ab-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="626ab-112">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="626ab-112">Parent elements</span></span>

|<span data-ttu-id="626ab-113">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="626ab-113">**Element**</span></span>|<span data-ttu-id="626ab-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="626ab-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="626ab-115">Miembro</span><span class="sxs-lookup"><span data-stu-id="626ab-115">Member</span></span>](member-ex15websvcsotherref.md) <br/> |<span data-ttu-id="626ab-116">Representa un miembro de una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="626ab-116">Represents a member of a distribution list.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="626ab-117">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="626ab-117">Text value</span></span>

<span data-ttu-id="626ab-118">En la siguiente tabla se enumeran los valores posibles para el elemento **status** .</span><span class="sxs-lookup"><span data-stu-id="626ab-118">The following table lists the possible values for the **Status** element.</span></span> 
  
<span data-ttu-id="626ab-119">**Valores del elemento status**</span><span class="sxs-lookup"><span data-stu-id="626ab-119">**Status element values**</span></span>

|<span data-ttu-id="626ab-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="626ab-120">**Value**</span></span>|<span data-ttu-id="626ab-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="626ab-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="626ab-122">No reconocido</span><span class="sxs-lookup"><span data-stu-id="626ab-122">Unrecognized</span></span>  <br/> |<span data-ttu-id="626ab-123">La información del miembro no es válida o no se reconoce.</span><span class="sxs-lookup"><span data-stu-id="626ab-123">Member information is invalid or unrecognized.</span></span>  <br/> |
|<span data-ttu-id="626ab-124">Normal</span><span class="sxs-lookup"><span data-stu-id="626ab-124">Normal</span></span>  <br/> |<span data-ttu-id="626ab-125">La información de los miembros de una lista de distribución está sincronizada con el objeto al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="626ab-125">Member information in a distribution list is in sync with the referenced object.</span></span>  <br/> |
|<span data-ttu-id="626ab-126">Disminuido</span><span class="sxs-lookup"><span data-stu-id="626ab-126">Demoted</span></span>  <br/> |<span data-ttu-id="626ab-127">El objeto al que se hace referencia no está disponible.</span><span class="sxs-lookup"><span data-stu-id="626ab-127">Referenced object is not available.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="626ab-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="626ab-128">Remarks</span></span>

<span data-ttu-id="626ab-129">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="626ab-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="626ab-130">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="626ab-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="626ab-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="626ab-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="626ab-132">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="626ab-132">Schema Name</span></span>  <br/> |<span data-ttu-id="626ab-133">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="626ab-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="626ab-134">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="626ab-134">Validation File</span></span>  <br/> |<span data-ttu-id="626ab-135">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="626ab-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="626ab-136">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="626ab-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="626ab-137">Falso</span><span class="sxs-lookup"><span data-stu-id="626ab-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="626ab-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="626ab-138">See also</span></span>



- [<span data-ttu-id="626ab-139">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="626ab-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

