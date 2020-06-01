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
description: El elemento DLExpansion contiene una matriz de buzones que se encuentran en una lista de distribución.
ms.openlocfilehash: 079ad1c0f114d201f5d1b91c3fd9bb45b943cc1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457000"
---
# <a name="dlexpansion"></a><span data-ttu-id="16382-103">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="16382-103">DLExpansion</span></span>

<span data-ttu-id="16382-104">El elemento **DLExpansion** contiene una matriz de buzones que se encuentran en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="16382-104">The **DLExpansion** element contains an array of mailboxes that are contained in a distribution list.</span></span> 
  
- [<span data-ttu-id="16382-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="16382-105">ExpandDLResponse</span></span>](expanddlresponse.md) 
- [<span data-ttu-id="16382-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="16382-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="16382-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="16382-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
- [<span data-ttu-id="16382-108">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="16382-108">DLExpansion</span></span>](dlexpansion.md)
  
```xml
<DLExpansion AbsoluteDenominator"" IncludesLastItemInRange="" IndexedPagingOffset="" NumeratorOffset="" TotalItemsInView="">
   <Mailbox/>
</DLExpansion>
```

 <span data-ttu-id="16382-109">**ArrayOfDLExpansionType**</span><span class="sxs-lookup"><span data-stu-id="16382-109">**ArrayOfDLExpansionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="16382-110">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="16382-110">Attributes and elements</span></span>

<span data-ttu-id="16382-111">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="16382-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="16382-112">Atributos</span><span class="sxs-lookup"><span data-stu-id="16382-112">Attributes</span></span>

|<span data-ttu-id="16382-113">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="16382-113">**Attribute**</span></span>|<span data-ttu-id="16382-114">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16382-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="16382-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="16382-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="16382-116">Representa el siguiente índice que se debe usar para la siguiente solicitud cuando se usa una vista de página indizada.</span><span class="sxs-lookup"><span data-stu-id="16382-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="16382-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="16382-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="16382-118">Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud cuando se usan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="16382-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="16382-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="16382-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="16382-120">Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se usan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="16382-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="16382-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="16382-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="16382-122">Indica si los resultados actuales contienen el último elemento de la consulta para que no sea necesario paginación adicional.</span><span class="sxs-lookup"><span data-stu-id="16382-122">Indicates whether the current results contain the last item in the query so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="16382-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="16382-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="16382-124">Representa el número total de elementos de la vista.</span><span class="sxs-lookup"><span data-stu-id="16382-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16382-125">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="16382-125">Child elements</span></span>

|<span data-ttu-id="16382-126">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16382-126">**Element**</span></span>|<span data-ttu-id="16382-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16382-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16382-128">Buzón</span><span class="sxs-lookup"><span data-stu-id="16382-128">Mailbox</span></span>](mailbox.md) <br/> |<span data-ttu-id="16382-129">Identifica un objeto de servicio de directorio de Active Directory habilitado para correo.</span><span class="sxs-lookup"><span data-stu-id="16382-129">Identifies a mail-enabled Active Directory directory service object.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="16382-130">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="16382-130">Parent elements</span></span>

|<span data-ttu-id="16382-131">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="16382-131">**Element**</span></span>|<span data-ttu-id="16382-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="16382-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="16382-133">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="16382-133">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md) <br/> |<span data-ttu-id="16382-134">Contiene el estado y el resultado de una sola solicitud ExpandDL.</span><span class="sxs-lookup"><span data-stu-id="16382-134">Contains the status and result of a single ExpandDL request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16382-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="16382-135">Remarks</span></span>

<span data-ttu-id="16382-136">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Microsoft Exchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="16382-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16382-137">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="16382-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16382-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="16382-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="16382-139">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="16382-139">Schema Name</span></span>  <br/> |<span data-ttu-id="16382-140">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="16382-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="16382-141">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="16382-141">Validation File</span></span>  <br/> |<span data-ttu-id="16382-142">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="16382-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="16382-143">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="16382-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="16382-144">Falso</span><span class="sxs-lookup"><span data-stu-id="16382-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="16382-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="16382-145">See also</span></span>

- [<span data-ttu-id="16382-146">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="16382-146">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="16382-147">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="16382-147">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md) 
- [<span data-ttu-id="16382-148">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="16382-148">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

