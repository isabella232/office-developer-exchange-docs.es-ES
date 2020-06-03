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
description: El elemento FractionalPageFolderView describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud FindFolder.
ms.openlocfilehash: a8627c6277b49655d3933679128b844118633cda
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463072"
---
# <a name="fractionalpagefolderview"></a><span data-ttu-id="43238-103">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="43238-103">FractionalPageFolderView</span></span>

<span data-ttu-id="43238-104">El elemento **FractionalPageFolderView** describe dónde se inicia la vista paginada y el número máximo de carpetas que se devuelven en una solicitud [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="43238-104">The **FractionalPageFolderView** element describes where the paged view starts and the maximum number of folders returned in a [FindFolder](findfolder.md) request.</span></span> 
  
[<span data-ttu-id="43238-105">FindFolder</span><span class="sxs-lookup"><span data-stu-id="43238-105">FindFolder</span></span>](findfolder.md)
  
[<span data-ttu-id="43238-106">FractionalPageFolderView</span><span class="sxs-lookup"><span data-stu-id="43238-106">FractionalPageFolderView</span></span>](fractionalpagefolderview.md)
  
```xml
<FractionalPageFolderView MaxEntriesReturned="" Numerator="" Denominator=""/>
```

 <span data-ttu-id="43238-107">**FractionalPageViewType**</span><span class="sxs-lookup"><span data-stu-id="43238-107">**FractionalPageViewType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="43238-108">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="43238-108">Attributes and elements</span></span>

<span data-ttu-id="43238-109">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="43238-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="43238-110">Atributos</span><span class="sxs-lookup"><span data-stu-id="43238-110">Attributes</span></span>

|<span data-ttu-id="43238-111">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="43238-111">**Attribute**</span></span>|<span data-ttu-id="43238-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43238-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="43238-113">**MaxEntriesReturned**</span><span class="sxs-lookup"><span data-stu-id="43238-113">**MaxEntriesReturned**</span></span> <br/> |<span data-ttu-id="43238-114">Identifica el número máximo de resultados que se devolverá en la respuesta [FindFolder](findfolder.md) .</span><span class="sxs-lookup"><span data-stu-id="43238-114">Identifies the maximum number of results to return in the [FindFolder](findfolder.md) response.</span></span> <span data-ttu-id="43238-115">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="43238-115">This attribute is optional.</span></span>  <br/> |
|<span data-ttu-id="43238-116">**Numera**</span><span class="sxs-lookup"><span data-stu-id="43238-116">**Numerator**</span></span> <br/> |<span data-ttu-id="43238-117">Representa el numerador del desplazamiento fraccionario desde el inicio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-117">Represents the numerator of the fractional offset from the start of the result set.</span></span> <span data-ttu-id="43238-118">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43238-118">This attribute is required.</span></span> <span data-ttu-id="43238-119">El numerador debe ser igual o menor que el denominador.</span><span class="sxs-lookup"><span data-stu-id="43238-119">The numerator must be equal to or less than the denominator.</span></span> <span data-ttu-id="43238-120">Este atributo debe representar un valor integral que sea igual o mayor que cero.</span><span class="sxs-lookup"><span data-stu-id="43238-120">This attribute must represent an integral value that is equal to or greater than zero.</span></span> <span data-ttu-id="43238-121">Para obtener más información, vea las notas más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="43238-121">For more information, see Remarks later in this topic.</span></span>  <br/> |
|<span data-ttu-id="43238-122">**Denominador**</span><span class="sxs-lookup"><span data-stu-id="43238-122">**Denominator**</span></span> <br/> |<span data-ttu-id="43238-123">Representa el denominador del desplazamiento fraccionario desde el principio del número total de carpetas del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-123">Represents the denominator of the fractional offset from the start of the total number of folders in the result set.</span></span> <span data-ttu-id="43238-124">Este atributo es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="43238-124">This attribute is required.</span></span> <span data-ttu-id="43238-125">Este atributo debe representar un valor integral que sea mayor que uno.</span><span class="sxs-lookup"><span data-stu-id="43238-125">This attribute must represent an integral value that is greater than one.</span></span> <span data-ttu-id="43238-126">Para obtener más información, vea las notas más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="43238-126">For more information, see Remarks later in this topic.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="43238-127">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="43238-127">Child elements</span></span>

<span data-ttu-id="43238-128">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="43238-128">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="43238-129">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="43238-129">Parent elements</span></span>

|<span data-ttu-id="43238-130">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="43238-130">**Element**</span></span>|<span data-ttu-id="43238-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="43238-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="43238-132">FindFolder</span><span class="sxs-lookup"><span data-stu-id="43238-132">FindFolder</span></span>](findfolder.md) <br/> |<span data-ttu-id="43238-133">Define una solicitud para identificar las carpetas en un buzón.</span><span class="sxs-lookup"><span data-stu-id="43238-133">Defines a request to identify folders in a mailbox.</span></span>  <br/> <span data-ttu-id="43238-134">La siguiente es la expresión XPath a este elemento:</span><span class="sxs-lookup"><span data-stu-id="43238-134">The following is the XPath expression to this element:</span></span>  <br/>  `/FindFolder` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43238-135">Comentarios</span><span class="sxs-lookup"><span data-stu-id="43238-135">Remarks</span></span>

<span data-ttu-id="43238-136">El desplazamiento de vista paginada desde el principio del conjunto de carpetas encontradas se describe mediante una fracción.</span><span class="sxs-lookup"><span data-stu-id="43238-136">The paged view offset from the start of the set of found folders is described by a fraction.</span></span> <span data-ttu-id="43238-137">La fracción, definida por los atributos **numerador** y **denominador** , describe dónde comienza la página de información.</span><span class="sxs-lookup"><span data-stu-id="43238-137">The fraction, which is defined by the **Numerator** and **Denominator** attributes, describes where the page of information starts.</span></span> <span data-ttu-id="43238-138">Por ejemplo, si el **numerador** es igual a cuatro y el **denominador** es cinco, la página de la información devuelta comienza en una entrada que se encuentra cuatro-quintos de la forma en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-138">For example, if **Numerator** equals four and **Denominator** equals five, the page of returned information starts at an entry located four-fifths of the way in to the result set.</span></span> 
  
<span data-ttu-id="43238-139">Si la fracción da como resultado cero, indica el inicio del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-139">If the fraction evaluates to zero, that indicates the start of the results set.</span></span> <span data-ttu-id="43238-140">Si la fracción da como resultado una, que indica el final del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-140">If the fraction evaluates to one, that indicates the end of the result set.</span></span>
  
> [!NOTE]
> <span data-ttu-id="43238-141">La fracción representa el punto de inicio de la página, no el número de resultados que se devolverán en el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="43238-141">The fraction represents the start point of page, not how many results in the result set will be returned.</span></span> 
  
<span data-ttu-id="43238-142">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta MicrosoftExchange Server 2007 que tiene instalado el rol de servidor acceso de clientes.</span><span class="sxs-lookup"><span data-stu-id="43238-142">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="43238-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="43238-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="43238-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="43238-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="43238-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="43238-145">Schema Name</span></span>  <br/> |<span data-ttu-id="43238-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="43238-146">Messages schema</span></span>  <br/> |
|<span data-ttu-id="43238-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="43238-147">Validation File</span></span>  <br/> |<span data-ttu-id="43238-148">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="43238-148">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="43238-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="43238-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="43238-150">Falso</span><span class="sxs-lookup"><span data-stu-id="43238-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="43238-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="43238-151">See also</span></span>



[<span data-ttu-id="43238-152">Operación FindFolder</span><span class="sxs-lookup"><span data-stu-id="43238-152">FindFolder operation</span></span>](findfolder-operation.md)


[<span data-ttu-id="43238-153">Buscar carpetas</span><span class="sxs-lookup"><span data-stu-id="43238-153">Finding Folders</span></span>](https://msdn.microsoft.com/library/9124d868-017a-43f0-b915-5c0082cacec9%28Office.15%29.aspx)

