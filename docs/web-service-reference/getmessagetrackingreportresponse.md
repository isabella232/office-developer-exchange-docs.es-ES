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
description: El elemento GetMessageTrackingReportResponse contiene la respuesta para la operación GetMessageTrackingReport.
ms.openlocfilehash: 15e1f5c91c07dbaad224fb0cd3bc89f444a18087
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460571"
---
# <a name="getmessagetrackingreportresponse"></a><span data-ttu-id="5e3ac-103">GetMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="5e3ac-103">GetMessageTrackingReportResponse</span></span>

<span data-ttu-id="5e3ac-104">El elemento **GetMessageTrackingReportResponse** contiene la respuesta para la [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5e3ac-104">The **GetMessageTrackingReportResponse** element contains the response for the [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>
  
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

 <span data-ttu-id="5e3ac-105">**GetMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-105">**GetMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5e3ac-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="5e3ac-106">Attributes and elements</span></span>

<span data-ttu-id="5e3ac-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5e3ac-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="5e3ac-108">Attributes</span></span>

|<span data-ttu-id="5e3ac-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-109">**Attribute**</span></span>|<span data-ttu-id="5e3ac-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e3ac-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="5e3ac-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-112">Describes the status of the response.</span></span> <br/><br/><span data-ttu-id="5e3ac-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="5e3ac-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="5e3ac-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="5e3ac-114">-  Success</span></span>  <br/><span data-ttu-id="5e3ac-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="5e3ac-115">-  Warning</span></span>  <br/><span data-ttu-id="5e3ac-116">-Error</span><span class="sxs-lookup"><span data-stu-id="5e3ac-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="5e3ac-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="5e3ac-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="5e3ac-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-118">**Value**</span></span>|<span data-ttu-id="5e3ac-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5e3ac-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-120">**Success**</span></span> <br/> |<span data-ttu-id="5e3ac-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="5e3ac-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-122">**Warning**</span></span> <br/> | <span data-ttu-id="5e3ac-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-123">Describes a request that was not processed.</span></span> <span data-ttu-id="5e3ac-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span><br/><br/> <span data-ttu-id="5e3ac-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="5e3ac-125">The following are examples of sources of warnings:</span></span>  <br/><br/><span data-ttu-id="5e3ac-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="5e3ac-127">-El dominio de Active Directory atiende (AD DS) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-127">-  Active Directory Domain Serves (AD DS) is offline.</span></span>  <br/><span data-ttu-id="5e3ac-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="5e3ac-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="5e3ac-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="5e3ac-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="5e3ac-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-132">**Error**</span></span> <br/> | <span data-ttu-id="5e3ac-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="5e3ac-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="5e3ac-134">The following are examples of sources of errors:</span></span>  <br/>  <span data-ttu-id="5e3ac-135">Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="5e3ac-135">Invalid attributes or elements</span></span>  <br/><br/><span data-ttu-id="5e3ac-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="5e3ac-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="5e3ac-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="5e3ac-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="5e3ac-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="5e3ac-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="5e3ac-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="5e3ac-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="5e3ac-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="5e3ac-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="5e3ac-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="5e3ac-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5e3ac-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5e3ac-142">Child elements</span></span>

|<span data-ttu-id="5e3ac-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-143">**Element**</span></span>|<span data-ttu-id="5e3ac-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="5e3ac-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5e3ac-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="5e3ac-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="5e3ac-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="5e3ac-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="5e3ac-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="5e3ac-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="5e3ac-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="5e3ac-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="5e3ac-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="5e3ac-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-154">MessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5e3ac-154">MessageTrackingReport</span></span>](messagetrackingreport.md) <br/> |<span data-ttu-id="5e3ac-155">Contiene un solo mensaje que se devuelve en una [operación GetMessageTrackingReport](getmessagetrackingreport-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5e3ac-155">Contains a single message that is returned in a [GetMessageTrackingReport operation](getmessagetrackingreport-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-156">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="5e3ac-156">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="5e3ac-157">Proporciona información de tiempo y rendimiento que se usa para la creación de informes en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-157">Provides timing and performance information that is used for reporting in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-158">Errores</span><span class="sxs-lookup"><span data-stu-id="5e3ac-158">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="5e3ac-159">Contiene un contenedor de propiedades donde se almacenan los errores que se devuelven a través del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-159">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="5e3ac-160">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="5e3ac-160">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="5e3ac-161">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-161">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5e3ac-162">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="5e3ac-162">Parent elements</span></span>

<span data-ttu-id="5e3ac-163">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-163">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="5e3ac-164">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="5e3ac-164">Text value</span></span>

<span data-ttu-id="5e3ac-165">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-165">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5e3ac-166">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e3ac-166">Remarks</span></span>

<span data-ttu-id="5e3ac-167">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="5e3ac-167">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5e3ac-168">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="5e3ac-168">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5e3ac-169">Namespace</span><span class="sxs-lookup"><span data-stu-id="5e3ac-169">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="5e3ac-170">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="5e3ac-170">Schema Name</span></span>  <br/> |<span data-ttu-id="5e3ac-171">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="5e3ac-171">Messages schema</span></span>  <br/> |
|<span data-ttu-id="5e3ac-172">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="5e3ac-172">Validation File</span></span>  <br/> |<span data-ttu-id="5e3ac-173">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="5e3ac-173">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="5e3ac-174">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="5e3ac-174">Can be Empty</span></span>  <br/> |<span data-ttu-id="5e3ac-175">Falso</span><span class="sxs-lookup"><span data-stu-id="5e3ac-175">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5e3ac-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e3ac-176">See also</span></span>

- [<span data-ttu-id="5e3ac-177">Operación GetMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="5e3ac-177">GetMessageTrackingReport operation</span></span>](getmessagetrackingreport-operation.md)
- [<span data-ttu-id="5e3ac-178">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="5e3ac-178">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

