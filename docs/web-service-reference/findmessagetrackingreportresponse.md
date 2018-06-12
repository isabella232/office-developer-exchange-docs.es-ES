---
title: FindMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FindMessageTrackingReportResponse
api_type:
- schema
ms.assetid: ed4265dc-0e79-4b34-8bf4-88a94875629d
description: El elemento FindMessageTrackingReportResponse contiene el estado y el resultado de una única solicitud de operación FindMessageTrackingReport.
ms.openlocfilehash: fa381f500eac9a46b11aea8c813f1ffc625a3bc3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764646"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="4fbb9-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="4fbb9-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="4fbb9-104">El elemento **FindMessageTrackingReportResponse** contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbb9-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
```xml
<FindMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <Diagnostics/>
   <MessageTrackingSearchResults/>
   <Errors/>
   <Properties/>
</FindMessageTrackingReportResponse>
```

 <span data-ttu-id="4fbb9-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4fbb9-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4fbb9-106">Attributes and elements</span></span>

<span data-ttu-id="4fbb9-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4fbb9-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4fbb9-108">Attributes</span></span>

|<span data-ttu-id="4fbb9-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-109">**Attribute**</span></span>|<span data-ttu-id="4fbb9-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fbb9-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="4fbb9-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="4fbb9-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="4fbb9-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="4fbb9-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="4fbb9-114">-  Success</span></span>  <br/><span data-ttu-id="4fbb9-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="4fbb9-115">-  Warning</span></span>  <br/><span data-ttu-id="4fbb9-116">-Error</span><span class="sxs-lookup"><span data-stu-id="4fbb9-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="4fbb9-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4fbb9-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="4fbb9-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-118">**Value**</span></span>|<span data-ttu-id="4fbb9-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4fbb9-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-120">**Success**</span></span> <br/> |<span data-ttu-id="4fbb9-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="4fbb9-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-122">**Warning**</span></span> <br/> | <span data-ttu-id="4fbb9-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-123">Describes a request that was not processed.</span></span> <span data-ttu-id="4fbb9-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="4fbb9-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="4fbb9-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="4fbb9-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="4fbb9-127">-Los servicios de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="4fbb9-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="4fbb9-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="4fbb9-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="4fbb9-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="4fbb9-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-132">**Error**</span></span> <br/> | <span data-ttu-id="4fbb9-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="4fbb9-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="4fbb9-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="4fbb9-135">-No válida Atributos o elementos</span><span class="sxs-lookup"><span data-stu-id="4fbb9-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="4fbb9-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="4fbb9-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="4fbb9-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="4fbb9-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="4fbb9-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="4fbb9-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="4fbb9-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="4fbb9-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="4fbb9-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="4fbb9-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="4fbb9-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="4fbb9-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4fbb9-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4fbb9-142">Child elements</span></span>

|<span data-ttu-id="4fbb9-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-143">**Element**</span></span>|<span data-ttu-id="4fbb9-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fbb9-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4fbb9-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="4fbb9-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4fbb9-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4fbb9-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4fbb9-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4fbb9-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4fbb9-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="4fbb9-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4fbb9-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4fbb9-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-154">Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="4fbb9-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="4fbb9-155">Contiene información que se usará para producir varios informes de estadísticos para la característica de seguimiento en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="4fbb9-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="4fbb9-157">Contiene y matriz de los mensajes que coinciden con los requisitos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="4fbb9-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="4fbb9-159">Contiene el ámbito de la búsqueda que se llevó a cabo para obtener los resultados de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-160">Errors</span><span class="sxs-lookup"><span data-stu-id="4fbb9-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="4fbb9-161">Contiene un contenedor de propiedades para almacenar los errores que se devuelven a través del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="4fbb9-162">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="4fbb9-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="4fbb9-163">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4fbb9-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4fbb9-164">Parent elements</span></span>

<span data-ttu-id="4fbb9-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="4fbb9-166">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="4fbb9-166">Text value</span></span>

<span data-ttu-id="4fbb9-167">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4fbb9-168">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fbb9-168">Remarks</span></span>

<span data-ttu-id="4fbb9-169">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4fbb9-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4fbb9-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4fbb9-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4fbb9-171">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4fbb9-171">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4fbb9-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4fbb9-172">Schema Name</span></span>  <br/> |<span data-ttu-id="4fbb9-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4fbb9-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="4fbb9-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4fbb9-174">Validation File</span></span>  <br/> |<span data-ttu-id="4fbb9-175">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="4fbb9-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4fbb9-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4fbb9-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="4fbb9-177">False</span><span class="sxs-lookup"><span data-stu-id="4fbb9-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4fbb9-178">Ver también</span><span class="sxs-lookup"><span data-stu-id="4fbb9-178">See also</span></span>

- [<span data-ttu-id="4fbb9-179">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="4fbb9-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="4fbb9-180">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="4fbb9-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

