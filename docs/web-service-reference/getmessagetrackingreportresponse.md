---
title: GetMessageTrackingReportResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetMessageTrackingReportResponse
api_type:
- schema
ms.assetid: 41177894-2008-44a6-86f8-bc34c0a48e36
description: El elemento GetMessageTrackingReportResponse contiene la respuesta de la operación de GetMessageTrackingReport.
ms.openlocfilehash: bdb8b97e57f92a32cbdc498d09297920366b58bd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764910"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="ccb28-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="ccb28-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="ccb28-104">El elemento **GetMessageTrackingReportResponse** contiene la respuesta de la [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ccb28-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
```xml
<GetMessageTrackingReportResponse ResponseClass="">
   <MessageText/>
   <ResponseCode/>
   <DescriptiveLinkKey/>
   <MessageXml/>
   <MessageTrackingReport/>
   <Diagnostics/>
   <Errors/>
   <Properties/>
</GetMessageTrackingReportResponse>
```

 <span data-ttu-id="ccb28-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ccb28-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ccb28-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ccb28-106">Attributes and elements</span></span>

<span data-ttu-id="ccb28-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ccb28-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ccb28-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ccb28-108">Attributes</span></span>

|<span data-ttu-id="ccb28-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ccb28-109">**Attribute**</span></span>|<span data-ttu-id="ccb28-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccb28-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ccb28-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ccb28-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ccb28-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb28-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="ccb28-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="ccb28-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ccb28-114">-Éxito</span><span class="sxs-lookup"><span data-stu-id="ccb28-114">-  Success</span></span>  <br/><span data-ttu-id="ccb28-115">-Advertencia</span><span class="sxs-lookup"><span data-stu-id="ccb28-115">-  Warning</span></span>  <br/><span data-ttu-id="ccb28-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ccb28-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ccb28-117">Valores de atributo de ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ccb28-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ccb28-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ccb28-118">**Value**</span></span>|<span data-ttu-id="ccb28-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccb28-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ccb28-120">**Operación correcta**</span><span class="sxs-lookup"><span data-stu-id="ccb28-120">**Success**</span></span> <br/> |<span data-ttu-id="ccb28-121">Describe una solicitud que se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccb28-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ccb28-122">**Warning**</span><span class="sxs-lookup"><span data-stu-id="ccb28-122">**Warning**</span></span> <br/> | <span data-ttu-id="ccb28-123">Describe una solicitud que no se procesó.</span><span class="sxs-lookup"><span data-stu-id="ccb28-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ccb28-124">Es posible que se devuelve una advertencia si se produjo un error mientras procesaba un elemento en la solicitud y no se podrían procesar los elementos subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="ccb28-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="ccb28-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="ccb28-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="ccb28-126">-El almacén de Exchange está sin conexión durante el proceso por lotes.</span><span class="sxs-lookup"><span data-stu-id="ccb28-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ccb28-127">-Active sirve de dominio de Active Directory (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ccb28-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ccb28-128">-Buzones se han movido.</span><span class="sxs-lookup"><span data-stu-id="ccb28-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ccb28-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ccb28-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ccb28-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="ccb28-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ccb28-131">-Se superó una cuota.</span><span class="sxs-lookup"><span data-stu-id="ccb28-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ccb28-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ccb28-132">**Error**</span></span> <br/> | <span data-ttu-id="ccb28-133">Describe una solicitud que no se cumplen los requisitos.</span><span class="sxs-lookup"><span data-stu-id="ccb28-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ccb28-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="ccb28-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="ccb28-135">Elementos o atributos no válidos</span><span class="sxs-lookup"><span data-stu-id="ccb28-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="ccb28-136">-Los atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="ccb28-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ccb28-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="ccb28-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ccb28-138">-Un atributo o un elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="ccb28-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ccb28-139">-Un intento de acceso no autorizado por cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="ccb28-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ccb28-140">-Un error del lado del servidor en respuesta a una llamada de cliente válida</span><span class="sxs-lookup"><span data-stu-id="ccb28-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ccb28-141">Puede encontrar información sobre el error en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ccb28-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ccb28-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ccb28-142">Child elements</span></span>

|<span data-ttu-id="ccb28-143">**Element**</span><span class="sxs-lookup"><span data-stu-id="ccb28-143">**Element**</span></span>|<span data-ttu-id="ccb28-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccb28-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ccb28-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ccb28-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ccb28-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ccb28-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ccb28-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ccb28-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ccb28-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ccb28-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ccb28-150">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ccb28-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ccb28-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ccb28-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ccb28-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ccb28-153">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="ccb28-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-154">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ccb28-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="ccb28-155">Contiene un solo mensaje que se devuelve en una [operación de GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="ccb28-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="ccb28-156">Diagnósticos</span><span class="sxs-lookup"><span data-stu-id="ccb28-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="ccb28-157">Proporciona información de rendimiento y control de tiempo que se usa para la creación de informes en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="ccb28-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-158">Errors</span><span class="sxs-lookup"><span data-stu-id="ccb28-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ccb28-159">Contiene un contenedor de propiedades para almacenar los errores que se devuelven a través del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="ccb28-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="ccb28-160">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="ccb28-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="ccb28-161">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ccb28-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ccb28-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ccb28-162">Parent elements</span></span>

<span data-ttu-id="ccb28-163">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccb28-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ccb28-164">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ccb28-164">Text value</span></span>

<span data-ttu-id="ccb28-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ccb28-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ccb28-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ccb28-166">Remarks</span></span>

<span data-ttu-id="ccb28-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ccb28-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ccb28-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ccb28-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ccb28-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccb28-169">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ccb28-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ccb28-170">Schema Name</span></span>  <br/> |<span data-ttu-id="ccb28-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ccb28-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ccb28-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ccb28-172">Validation File</span></span>  <br/> |<span data-ttu-id="ccb28-173">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="ccb28-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ccb28-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ccb28-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="ccb28-175">False</span><span class="sxs-lookup"><span data-stu-id="ccb28-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ccb28-176">Ver también</span><span class="sxs-lookup"><span data-stu-id="ccb28-176">See also</span></span>

- [<span data-ttu-id="ccb28-177">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ccb28-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="ccb28-178">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="ccb28-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

