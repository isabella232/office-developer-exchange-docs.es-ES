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
description: El elemento ExpandDLResponseMessage contiene el estado y el resultado de una única solicitud de operación ExpandDL.
ms.openlocfilehash: e186c4e14cbb9c922a4d262c85c130b9c33ff939
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460641"
---
# <a name="expanddlresponsemessage"></a><span data-ttu-id="239d8-103">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="239d8-103">ExpandDLResponseMessage</span></span>

<span data-ttu-id="239d8-104">El elemento **ExpandDLResponseMessage** contiene el estado y el resultado de una única solicitud de [operación ExpandDL](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="239d8-104">The **ExpandDLResponseMessage** element contains the status and result of a single [ExpandDL operation](expanddl-operation.md) request.</span></span> 
  
- [<span data-ttu-id="239d8-105">ExpandDLResponse</span><span class="sxs-lookup"><span data-stu-id="239d8-105">ExpandDLResponse</span></span>](expanddlresponse.md)  
- [<span data-ttu-id="239d8-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="239d8-106">ResponseMessages</span></span>](responsemessages.md) 
- [<span data-ttu-id="239d8-107">ExpandDLResponseMessage</span><span class="sxs-lookup"><span data-stu-id="239d8-107">ExpandDLResponseMessage</span></span>](expanddlresponsemessage.md)
  
```xml
<ExpandDLResponseMessage ResponseClass="" IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <DLExpansion/>
</ExpandDLResponseMessage>
```

<span data-ttu-id="239d8-108">**ExpandDLResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="239d8-108">**ExpandDLResponseMessageType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="239d8-109">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="239d8-109">Attributes and elements</span></span>

<span data-ttu-id="239d8-110">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="239d8-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="239d8-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="239d8-111">Attributes</span></span>

|<span data-ttu-id="239d8-112">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="239d8-112">**Attribute**</span></span>|<span data-ttu-id="239d8-113">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239d8-113">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="239d8-114">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="239d8-114">**ResponseClass**</span></span> <br/> | <span data-ttu-id="239d8-115">Describe el estado de una respuesta de [operación de ExpandDL](expanddl-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="239d8-115">Describes the status of an [ExpandDL operation](expanddl-operation.md) response.</span></span><br/><br/><span data-ttu-id="239d8-116">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="239d8-116">The following values are valid for this attribute:</span></span> <br/> <br/><span data-ttu-id="239d8-117">-Correcto</span><span class="sxs-lookup"><span data-stu-id="239d8-117">-  Success</span></span>  <br/><span data-ttu-id="239d8-118">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="239d8-118">-  Warning</span></span>  <br/><span data-ttu-id="239d8-119">-Error</span><span class="sxs-lookup"><span data-stu-id="239d8-119">-  Error</span></span>  <br/> |
|<span data-ttu-id="239d8-120">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="239d8-120">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="239d8-121">Representa el siguiente índice que se debe usar para la siguiente solicitud cuando se usa una vista de paginación indizada.</span><span class="sxs-lookup"><span data-stu-id="239d8-121">Represents the next index that should be used for the next request when an indexed paging view is used.</span></span>  <br/> |
|<span data-ttu-id="239d8-122">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="239d8-122">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="239d8-123">Representa el nuevo valor del numerador que se va a usar para la siguiente solicitud cuando se usan vistas de página de fracción.</span><span class="sxs-lookup"><span data-stu-id="239d8-123">Represents the new numerator value to use for the next request when fraction page views are used.</span></span>  <br/> |
|<span data-ttu-id="239d8-124">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="239d8-124">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="239d8-125">Representa el siguiente denominador que se va a usar para la siguiente solicitud cuando se realiza una paginación fraccionada.</span><span class="sxs-lookup"><span data-stu-id="239d8-125">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="239d8-126">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="239d8-126">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="239d8-127">Indica que no se necesita paginación adicional.</span><span class="sxs-lookup"><span data-stu-id="239d8-127">Indicates that additional paging is not needed.</span></span> <span data-ttu-id="239d8-128">Este atributo será true si los resultados actuales contienen el último elemento de la consulta.</span><span class="sxs-lookup"><span data-stu-id="239d8-128">This attribute will be true if the current results contain the last item in the query.</span></span>  <br/> |
|<span data-ttu-id="239d8-129">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="239d8-129">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="239d8-130">Representa el número total de elementos que supera la restricción.</span><span class="sxs-lookup"><span data-stu-id="239d8-130">Represents the total number of items that pass the restriction.</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="239d8-131">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="239d8-131">ResponseClass attribute values</span></span>

|<span data-ttu-id="239d8-132">**Valor**</span><span class="sxs-lookup"><span data-stu-id="239d8-132">**Value**</span></span>|<span data-ttu-id="239d8-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239d8-133">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="239d8-134">**Success**</span><span class="sxs-lookup"><span data-stu-id="239d8-134">**Success**</span></span> <br/> |<span data-ttu-id="239d8-135">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="239d8-135">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="239d8-136">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="239d8-136">**Warning**</span></span> <br/> | <span data-ttu-id="239d8-137">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="239d8-137">Describes a request that was not processed.</span></span> <span data-ttu-id="239d8-138">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="239d8-138">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="239d8-139">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="239d8-139">The following are examples of sources of warnings:</span></span><br/>  <br/><span data-ttu-id="239d8-140">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="239d8-140">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="239d8-141">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="239d8-141">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="239d8-142">-Se mueven los buzones.</span><span class="sxs-lookup"><span data-stu-id="239d8-142">-  Mailboxes are moved.</span></span>  <br/><span data-ttu-id="239d8-143">-La base de datos de buzones (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="239d8-143">-  The mailbox database (MDB) is offline.</span></span>  <br/><span data-ttu-id="239d8-144">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="239d8-144">-  A password is expired.</span></span>  <br/><span data-ttu-id="239d8-145">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="239d8-145">-  A quota was exceeded.</span></span>  <br/> |
|<span data-ttu-id="239d8-146">**Error**</span><span class="sxs-lookup"><span data-stu-id="239d8-146">**Error**</span></span> <br/> | <span data-ttu-id="239d8-147">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="239d8-147">Describes a request that cannot be fulfilled.</span></span><br/><br/> <span data-ttu-id="239d8-148">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="239d8-148">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="239d8-149">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="239d8-149">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="239d8-150">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="239d8-150">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="239d8-151">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="239d8-151">-  An unknown tag</span></span>  <br/><span data-ttu-id="239d8-152">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="239d8-152">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="239d8-153">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="239d8-153">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="239d8-154">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="239d8-154">-  A server-side failure in response to a valid client-side call</span></span> <br/> <br/>  <span data-ttu-id="239d8-155">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="239d8-155">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="239d8-156">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="239d8-156">Child elements</span></span>

|<span data-ttu-id="239d8-157">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="239d8-157">**Element**</span></span>|<span data-ttu-id="239d8-158">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239d8-158">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="239d8-159">MessageText</span><span class="sxs-lookup"><span data-stu-id="239d8-159">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="239d8-160">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="239d8-160">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="239d8-161">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="239d8-161">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="239d8-162">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="239d8-162">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="239d8-163">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="239d8-163">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="239d8-164">Actualmente no se usa y está reservado para su uso en el futuro.</span><span class="sxs-lookup"><span data-stu-id="239d8-164">Currently unused and is reserved for future use.</span></span> <span data-ttu-id="239d8-165">Contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="239d8-165">It contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="239d8-166">MessageXml</span><span class="sxs-lookup"><span data-stu-id="239d8-166">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="239d8-167">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="239d8-167">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="239d8-168">DLExpansion</span><span class="sxs-lookup"><span data-stu-id="239d8-168">DLExpansion</span></span>](dlexpansion.md) <br/> |<span data-ttu-id="239d8-169">Contiene una matriz de buzones que se encuentran en una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="239d8-169">Contains an array of mailboxes that are contained in a distribution list.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="239d8-170">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="239d8-170">Parent elements</span></span>

|<span data-ttu-id="239d8-171">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="239d8-171">**Element**</span></span>|<span data-ttu-id="239d8-172">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="239d8-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="239d8-173">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="239d8-173">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="239d8-174">Contiene los mensajes de respuesta de una solicitud de servicios web Exchange.</span><span class="sxs-lookup"><span data-stu-id="239d8-174">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="239d8-175">Comentarios</span><span class="sxs-lookup"><span data-stu-id="239d8-175">Remarks</span></span>

<span data-ttu-id="239d8-176">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que ejecuta Exchange Server con el rol de servidor acceso de clientes instalado.</span><span class="sxs-lookup"><span data-stu-id="239d8-176">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="239d8-177">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="239d8-177">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="239d8-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="239d8-178">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="239d8-179">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="239d8-179">Schema Name</span></span>  <br/> |<span data-ttu-id="239d8-180">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="239d8-180">Types schema</span></span>  <br/> |
|<span data-ttu-id="239d8-181">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="239d8-181">Validation File</span></span>  <br/> |<span data-ttu-id="239d8-182">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="239d8-182">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="239d8-183">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="239d8-183">Can be Empty</span></span>  <br/> |<span data-ttu-id="239d8-184">Falso</span><span class="sxs-lookup"><span data-stu-id="239d8-184">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="239d8-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="239d8-185">See also</span></span>

- [<span data-ttu-id="239d8-186">Operación ExpandDL</span><span class="sxs-lookup"><span data-stu-id="239d8-186">ExpandDL operation</span></span>](expanddl-operation.md)
- [<span data-ttu-id="239d8-187">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="239d8-187">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)
- [<span data-ttu-id="239d8-188">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="239d8-188">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

