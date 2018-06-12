---
title: DLExpansion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DLExpansion
api_type:
- schema
ms.assetid: 9e50278d-fe6a-45e2-a72b-0fb06809e128
description: El elemento DLExpansion contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.
ms.openlocfilehash: 06081b4aba761a7137f921b3bc1c8d6b2afab88c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764257"
---
# <a name="dlexpansion"></a><span data-ttu-id="52e18-103">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="52e18-103">DLExpansion</span></span>

<span data-ttu-id="52e18-104">El elemento **DLExpansion** contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="52e18-104">The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list.</span></span> 
  
- [<span data-ttu-id="52e18-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="52e18-105">ExpandDLResponse</span></span>](expanddlresponse.md) 
- [<span data-ttu-id="52e18-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="52e18-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="52e18-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52e18-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
- [<span data-ttu-id="52e18-108">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="52e18-108">DLExpansion</span></span>](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 <span data-ttu-id="52e18-109">**ArrayOfDLExpansionType**</span><span class="sxs-lookup"><span data-stu-id="52e18-109">**ArrayOfDLExpansionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="52e18-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="52e18-110">Attributes and elements</span></span>

<span data-ttu-id="52e18-111">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="52e18-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="52e18-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="52e18-112">Attributes</span></span>

|<span data-ttu-id="52e18-113">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="52e18-113">**Attribute**</span></span>|<span data-ttu-id="52e18-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52e18-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52e18-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="52e18-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="52e18-116">Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista de página indizados.</span><span class="sxs-lookup"><span data-stu-id="52e18-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="52e18-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="52e18-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="52e18-118">Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se utilizan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="52e18-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="52e18-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="52e18-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="52e18-120">Representa el denominador siguiente para usar para la solicitud siguiente cuando se utilizan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="52e18-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="52e18-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="52e18-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="52e18-122">Indica si los resultados actuales contienen el último elemento de la consulta de modo que no es necesaria la paginación adicional.</span><span class="sxs-lookup"><span data-stu-id="52e18-122">Indicates whether the current results contain the last item in the query so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="52e18-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="52e18-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="52e18-124">Representa el número total de elementos en la vista.</span><span class="sxs-lookup"><span data-stu-id="52e18-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52e18-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="52e18-125">Child elements</span></span>

|<span data-ttu-id="52e18-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="52e18-126">**Element**</span></span>|<span data-ttu-id="52e18-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52e18-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e18-128">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="52e18-128">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="52e18-129">Identifica un objeto de servicio de directorio de Active Directory habilitados para correo.</span><span class="sxs-lookup"><span data-stu-id="52e18-129">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="52e18-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="52e18-130">Parent elements</span></span>

|<span data-ttu-id="52e18-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="52e18-131">**Element**</span></span>|<span data-ttu-id="52e18-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="52e18-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52e18-133">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="52e18-133">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md) <br/> |<span data-ttu-id="52e18-134">Contiene el estado y el resultado de una única solicitud ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="52e18-134">Contains the status and result of a single ExpandDL request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52e18-135">Notas</span><span class="sxs-lookup"><span data-stu-id="52e18-135">Remarks</span></span>

<span data-ttu-id="52e18-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="52e18-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52e18-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="52e18-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52e18-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="52e18-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="52e18-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="52e18-139">Schema Name</span></span>  <br/> |<span data-ttu-id="52e18-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="52e18-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="52e18-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="52e18-141">Validation File</span></span>  <br/> |<span data-ttu-id="52e18-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="52e18-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="52e18-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="52e18-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="52e18-144">False</span><span class="sxs-lookup"><span data-stu-id="52e18-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="52e18-145">Ver también</span><span class="sxs-lookup"><span data-stu-id="52e18-145">See also</span></span>

- [<span data-ttu-id="52e18-146">Operación de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="52e18-146">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="52e18-147">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="52e18-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md) 
- [<span data-ttu-id="52e18-148">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="52e18-148">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

