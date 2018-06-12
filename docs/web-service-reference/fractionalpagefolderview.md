---
title: FractionalPageFolderView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FractionalPageFolderView
api_type:
- schema
ms.assetid: ef681f8a-136a-4c0e-ade6-ddcdbf2d85ad
description: El elemento FractionalPageFolderView describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud FindFolder.
ms.openlocfilehash: 3cb5f8333634a0c484ae3ce6a6256631cff57cc5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764705"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="5ee39-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="5ee39-103">FractionalPageFolderView</span></span>

<span data-ttu-id="5ee39-104">El elemento **FractionalPageFolderView** describe donde se inicia la vista de página y devuelve el número máximo de carpetas en una solicitud [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="5ee39-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="5ee39-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="5ee39-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="5ee39-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="5ee39-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="5ee39-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="5ee39-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5ee39-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5ee39-108">Attributes and elements</span></span>

<span data-ttu-id="5ee39-109">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5ee39-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5ee39-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="5ee39-110">Attributes</span></span>

|<span data-ttu-id="5ee39-111">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="5ee39-111">**Attribute**</span></span>|<span data-ttu-id="5ee39-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ee39-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ee39-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="5ee39-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="5ee39-114">Identifica el número máximo de resultados a devolver en la respuesta [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="5ee39-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="5ee39-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="5ee39-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="5ee39-116">**Numerador**</span><span class="sxs-lookup"><span data-stu-id="5ee39-116">**Numerator**</span></span> <br/> |<span data-ttu-id="5ee39-117">Representa el numerador de la fraccionario desplazamiento desde el comienzo del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="5ee39-118">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5ee39-118">This attribute is required.</span></span> <span data-ttu-id="5ee39-119">El numerador debe ser igual o menor que el denominador.</span><span class="sxs-lookup"><span data-stu-id="5ee39-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="5ee39-120">Este atributo debe representar un valor entero que es igual o mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="5ee39-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="5ee39-121">Para obtener más información, vea Comentarios más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="5ee39-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="5ee39-122">**Denominador**</span><span class="sxs-lookup"><span data-stu-id="5ee39-122">**Denominator**</span></span> <br/> |<span data-ttu-id="5ee39-123">Representa el denominador de la fraccionario desplazamiento desde el comienzo del número total de carpetas en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="5ee39-124">Este atributo es necesario.</span><span class="sxs-lookup"><span data-stu-id="5ee39-124">This attribute is required.</span></span> <span data-ttu-id="5ee39-125">Este atributo debe representar un valor entero que es mayor que uno.</span><span class="sxs-lookup"><span data-stu-id="5ee39-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="5ee39-126">Para obtener más información, vea Comentarios más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="5ee39-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5ee39-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5ee39-127">Child elements</span></span>

<span data-ttu-id="5ee39-128">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5ee39-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5ee39-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5ee39-129">Parent elements</span></span>

|<span data-ttu-id="5ee39-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="5ee39-130">**Element**</span></span>|<span data-ttu-id="5ee39-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5ee39-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ee39-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="5ee39-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="5ee39-133">Define una solicitud para identificar las carpetas de un buzón de correo.</span><span class="sxs-lookup"><span data-stu-id="5ee39-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="5ee39-134">La siguiente es la expresión de XPath para este elemento:</span><span class="sxs-lookup"><span data-stu-id="5ee39-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ee39-135">Notas</span><span class="sxs-lookup"><span data-stu-id="5ee39-135">Remarks</span></span>

<span data-ttu-id="5ee39-136">Se describe el desplazamiento de la vista de página desde el comienzo del conjunto de carpetas que se encuentran por una fracción.</span><span class="sxs-lookup"><span data-stu-id="5ee39-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="5ee39-137">La fracción, que se define mediante los atributos **numerador** y **denominador** , describe donde se inicia la página de información.</span><span class="sxs-lookup"><span data-stu-id="5ee39-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="5ee39-138">Por ejemplo, si **numerador** es igual a cuatro y **denominador** es igual a cinco, la página de información devuelta que comienza en una entrada que encuentra cuatro quintos de la forma en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="5ee39-139">Si el argumento de fracción se evalúa como cero, indica el inicio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="5ee39-140">Si el argumento de fracción se evalúa como uno, indica el final del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="5ee39-141">La fracción representa el punto inicial de la página, se devolverán resultados no cuántos en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="5ee39-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="5ee39-142">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="5ee39-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5ee39-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5ee39-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5ee39-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5ee39-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5ee39-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5ee39-145">Schema Name</span></span>  <br/> |<span data-ttu-id="5ee39-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5ee39-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5ee39-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5ee39-147">Validation File</span></span>  <br/> |<span data-ttu-id="5ee39-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="5ee39-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5ee39-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5ee39-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="5ee39-150">False</span><span class="sxs-lookup"><span data-stu-id="5ee39-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5ee39-151">Ver también</span><span class="sxs-lookup"><span data-stu-id="5ee39-151">See also</span></span>



[<span data-ttu-id="5ee39-152">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="5ee39-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="5ee39-153">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="5ee39-153">Finding Folders</span></span>](http://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

