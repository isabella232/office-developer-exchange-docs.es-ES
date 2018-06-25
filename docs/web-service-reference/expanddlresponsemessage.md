---
title: ExpandDLResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ExpandDLResponseMessage
api_type:
- schema
ms.assetid: 1140601b-98cf-4cb4-a019-321c7f63d5be
description: El elemento ExpandDLResponseMessage contiene el estado y el resultado de una única solicitud de operación de ExpandDL.
ms.openlocfilehash: 62a81574f9c513b905a92876b3d757c635b4f07b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764496"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="73cd7-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73cd7-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="73cd7-104">El elemento **ExpandDLResponseMessage** contiene el estado y el resultado de una única solicitud de [la operación de ExpandDL](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="73cd7-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="73cd7-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="73cd7-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="73cd7-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="73cd7-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="73cd7-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="73cd7-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="73cd7-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="73cd7-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="73cd7-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="73cd7-109">Attributes and elements</span></span>

<span data-ttu-id="73cd7-110">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="73cd7-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73cd7-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="73cd7-111">Attributes</span></span>

|<span data-ttu-id="73cd7-112">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="73cd7-112">**Attribute**</span></span>|<span data-ttu-id="73cd7-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73cd7-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73cd7-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="73cd7-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="73cd7-115">Describe el estado de una respuesta de [la operación de ExpandDL](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="73cd7-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="73cd7-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="73cd7-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="73cd7-117">-Éxito</span><span class="sxs-lookup"><span data-stu-id="73cd7-117">-  Success</span></span>  <br/><span data-ttu-id="73cd7-118">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="73cd7-118">-  Warning</span></span>  <br/><span data-ttu-id="73cd7-119">-Error</span><span class="sxs-lookup"><span data-stu-id="73cd7-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="73cd7-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="73cd7-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="73cd7-121">Representa el siguiente índice que se debe usar para la solicitud siguiente cuando se usa una vista indizada de paginación.</span><span class="sxs-lookup"><span data-stu-id="73cd7-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="73cd7-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="73cd7-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="73cd7-123">Representa el nuevo valor: número que se usará para la solicitud siguiente cuando se usan las vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="73cd7-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="73cd7-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="73cd7-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="73cd7-125">Representa el denominador siguiente para usar para la solicitud siguiente al realizar la paginación fraccionaria.</span><span class="sxs-lookup"><span data-stu-id="73cd7-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="73cd7-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="73cd7-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="73cd7-127">Indica que no es necesario paginación adicional.</span><span class="sxs-lookup"><span data-stu-id="73cd7-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="73cd7-128">Este atributo será true si los resultados actuales contienen el último elemento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="73cd7-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="73cd7-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="73cd7-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="73cd7-130">Representa el número total de elementos que pase la restricción.</span><span class="sxs-lookup"><span data-stu-id="73cd7-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="73cd7-131">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="73cd7-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="73cd7-132">**Valor**</span><span class="sxs-lookup"><span data-stu-id="73cd7-132">**Value**</span></span>|<span data-ttu-id="73cd7-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73cd7-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73cd7-134">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="73cd7-134">**Success**</span></span> <br/> |<span data-ttu-id="73cd7-135">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="73cd7-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="73cd7-136">**Warning**</span><span class="sxs-lookup"><span data-stu-id="73cd7-136">**Warning**</span></span> <br/> | <span data-ttu-id="73cd7-137">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="73cd7-137">Describes a request that was not processed.</span></span> <span data-ttu-id="73cd7-138">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="73cd7-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="73cd7-139">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="73cd7-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="73cd7-140">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="73cd7-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="73cd7-141">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="73cd7-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="73cd7-142">-Se mueven los buzones de correo.</span><span class="sxs-lookup"><span data-stu-id="73cd7-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="73cd7-143">-La base de datos de buzón (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="73cd7-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="73cd7-144">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="73cd7-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="73cd7-145">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="73cd7-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="73cd7-146">**Error**</span><span class="sxs-lookup"><span data-stu-id="73cd7-146">**Error**</span></span> <br/> | <span data-ttu-id="73cd7-147">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="73cd7-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="73cd7-148">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="73cd7-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="73cd7-149">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="73cd7-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="73cd7-150">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="73cd7-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="73cd7-151">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="73cd7-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="73cd7-152">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="73cd7-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="73cd7-153">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="73cd7-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="73cd7-154">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="73cd7-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="73cd7-155">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="73cd7-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73cd7-156">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="73cd7-156">Child elements</span></span>

|<span data-ttu-id="73cd7-157">**Element**</span><span class="sxs-lookup"><span data-stu-id="73cd7-157">**Element**</span></span>|<span data-ttu-id="73cd7-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73cd7-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73cd7-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="73cd7-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="73cd7-160">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73cd7-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="73cd7-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="73cd7-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="73cd7-162">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73cd7-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="73cd7-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="73cd7-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="73cd7-164">Actualmente no se utiliza y está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="73cd7-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="73cd7-165">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="73cd7-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="73cd7-166">MessageXml</span><span class="sxs-lookup"><span data-stu-id="73cd7-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="73cd7-167">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="73cd7-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="73cd7-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="73cd7-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="73cd7-169">Contiene una matriz de los buzones de correo que están contenidos en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="73cd7-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="73cd7-170">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="73cd7-170">Parent elements</span></span>

|<span data-ttu-id="73cd7-171">**Element**</span><span class="sxs-lookup"><span data-stu-id="73cd7-171">**Element**</span></span>|<span data-ttu-id="73cd7-172">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="73cd7-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73cd7-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="73cd7-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="73cd7-174">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="73cd7-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73cd7-175">Comentarios</span><span class="sxs-lookup"><span data-stu-id="73cd7-175">Remarks</span></span>

<span data-ttu-id="73cd7-176">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con la función de servidor de acceso de cliente instalada.</span><span class="sxs-lookup"><span data-stu-id="73cd7-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="73cd7-177">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="73cd7-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73cd7-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="73cd7-178">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73cd7-179">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="73cd7-179">Schema Name</span></span>  <br/> |<span data-ttu-id="73cd7-180">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="73cd7-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="73cd7-181">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="73cd7-181">Validation File</span></span>  <br/> |<span data-ttu-id="73cd7-182">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73cd7-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73cd7-183">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="73cd7-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="73cd7-184">False</span><span class="sxs-lookup"><span data-stu-id="73cd7-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73cd7-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="73cd7-185">See also</span></span>

- [<span data-ttu-id="73cd7-186">Operación de ExpandDL</span><span class="sxs-lookup"><span data-stu-id="73cd7-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="73cd7-187">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="73cd7-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="73cd7-188">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="73cd7-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

