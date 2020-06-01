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
ms.openlocfilehash: a72ae3b20f2cae3d37a90da36b816e6f3265c716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462918"
---
# <a name="findmessagetrackingreportresponse"></a><span data-ttu-id="ae92f-103">FindMessageTrackingReportResponse</span><span class="sxs-lookup"><span data-stu-id="ae92f-103">FindMessageTrackingReportResponse</span></span>

<span data-ttu-id="ae92f-104">El elemento **FindMessageTrackingReportResponse** contiene el estado y el resultado de una única solicitud de [operación FindMessageTrackingReport](findmessagetrackingreport-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="ae92f-104">The **FindMessageTrackingReportResponse** element contains the status and result of a single [FindMessageTrackingReport operation](findmessagetrackingreport-operation.md) request.</span></span> 
  
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

 <span data-ttu-id="ae92f-105">**FindMessageTrackingReportResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="ae92f-105">**FindMessageTrackingReportResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ae92f-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ae92f-106">Attributes and elements</span></span>

<span data-ttu-id="ae92f-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="ae92f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ae92f-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="ae92f-108">Attributes</span></span>

|<span data-ttu-id="ae92f-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="ae92f-109">**Attribute**</span></span>|<span data-ttu-id="ae92f-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae92f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae92f-111">**ResponseClass**</span><span class="sxs-lookup"><span data-stu-id="ae92f-111">**ResponseClass**</span></span> <br/> | <span data-ttu-id="ae92f-112">Describe el estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae92f-112">Describes the status of the response.</span></span><br/><br/> <span data-ttu-id="ae92f-113">Los siguientes valores son válidos para este atributo:</span><span class="sxs-lookup"><span data-stu-id="ae92f-113">The following values are valid for this attribute:</span></span>  <br/><br/><span data-ttu-id="ae92f-114">-Correcto</span><span class="sxs-lookup"><span data-stu-id="ae92f-114">-  Success</span></span>  <br/><span data-ttu-id="ae92f-115">-ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="ae92f-115">-  Warning</span></span>  <br/><span data-ttu-id="ae92f-116">-Error</span><span class="sxs-lookup"><span data-stu-id="ae92f-116">-  Error</span></span>  <br/> |
   
#### <a name="responseclass-attribute-values"></a><span data-ttu-id="ae92f-117">Valores del atributo ResponseClass</span><span class="sxs-lookup"><span data-stu-id="ae92f-117">ResponseClass attribute values</span></span>

|<span data-ttu-id="ae92f-118">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ae92f-118">**Value**</span></span>|<span data-ttu-id="ae92f-119">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae92f-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ae92f-120">**Success**</span><span class="sxs-lookup"><span data-stu-id="ae92f-120">**Success**</span></span> <br/> |<span data-ttu-id="ae92f-121">Describe una solicitud que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="ae92f-121">Describes a request that is fulfilled.</span></span>  <br/> |
|<span data-ttu-id="ae92f-122">**Advertencia**</span><span class="sxs-lookup"><span data-stu-id="ae92f-122">**Warning**</span></span> <br/> | <span data-ttu-id="ae92f-123">Describe una solicitud que no se ha procesado.</span><span class="sxs-lookup"><span data-stu-id="ae92f-123">Describes a request that was not processed.</span></span> <span data-ttu-id="ae92f-124">Se puede devolver una advertencia si se produjo un error al procesar un elemento de la solicitud y no se pudieron procesar los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="ae92f-124">A warning may be returned if an error occurred while an item in the request was processing and subsequent items could not be processed.</span></span> <br/><br/><span data-ttu-id="ae92f-125">Los siguientes son ejemplos de fuentes de advertencias:</span><span class="sxs-lookup"><span data-stu-id="ae92f-125">The following are examples of sources of warnings:</span></span> <br/> <br/><span data-ttu-id="ae92f-126">-El almacén de Exchange está sin conexión durante el lote.</span><span class="sxs-lookup"><span data-stu-id="ae92f-126">-  The Exchange store is offline during the batch.</span></span>  <br/><span data-ttu-id="ae92f-127">-Los servicios de dominio de Active Directory (AD DS) están sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ae92f-127">-  Active Directory Domain Services (AD DS) is offline.</span></span>  <br/><span data-ttu-id="ae92f-128">-Se movieron los buzones.</span><span class="sxs-lookup"><span data-stu-id="ae92f-128">-  Mailboxes were moved.</span></span>  <br/><span data-ttu-id="ae92f-129">-La base de datos de mensajes (MDB) está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="ae92f-129">-  The message database (MDB) is offline.</span></span>  <br/><span data-ttu-id="ae92f-130">-Una contraseña ha expirado.</span><span class="sxs-lookup"><span data-stu-id="ae92f-130">-  A password is expired.</span></span>  <br/><span data-ttu-id="ae92f-131">-Se ha superado la cuota.</span><span class="sxs-lookup"><span data-stu-id="ae92f-131">-  A quota has been exceeded.</span></span>  <br/> |
|<span data-ttu-id="ae92f-132">**Error**</span><span class="sxs-lookup"><span data-stu-id="ae92f-132">**Error**</span></span> <br/> | <span data-ttu-id="ae92f-133">Describe una solicitud que no se puede cumplir.</span><span class="sxs-lookup"><span data-stu-id="ae92f-133">Describes a request that cannot be fulfilled.</span></span> <br/><br/><span data-ttu-id="ae92f-134">Los siguientes son ejemplos de orígenes de errores:</span><span class="sxs-lookup"><span data-stu-id="ae92f-134">The following are examples of sources of errors:</span></span>  <br/><br/><span data-ttu-id="ae92f-135">-Atributos o elementos no válidos</span><span class="sxs-lookup"><span data-stu-id="ae92f-135">-  Invalid attributes or elements</span></span>  <br/><span data-ttu-id="ae92f-136">-Atributos o elementos que están fuera del intervalo</span><span class="sxs-lookup"><span data-stu-id="ae92f-136">-  Attributes or elements that are out of range</span></span>  <br/><span data-ttu-id="ae92f-137">-Una etiqueta desconocida</span><span class="sxs-lookup"><span data-stu-id="ae92f-137">-  An unknown tag</span></span>  <br/><span data-ttu-id="ae92f-138">-Un atributo o elemento que no es válido en el contexto</span><span class="sxs-lookup"><span data-stu-id="ae92f-138">-  An attribute or element that is not valid in the context</span></span>  <br/><span data-ttu-id="ae92f-139">-Un intento de acceso no autorizado por parte de cualquier cliente</span><span class="sxs-lookup"><span data-stu-id="ae92f-139">-  An unauthorized access attempt by any client</span></span>  <br/><span data-ttu-id="ae92f-140">-Un error del servidor en respuesta a una llamada válida del lado cliente</span><span class="sxs-lookup"><span data-stu-id="ae92f-140">-  A server-side failure in response to a valid client-side call</span></span>  <br/><br/>  <span data-ttu-id="ae92f-141">La información sobre el error se puede encontrar en los elementos [ResponseCode](responsecode.md) y [MessageText](messagetext.md) .</span><span class="sxs-lookup"><span data-stu-id="ae92f-141">Information about the error can be found in the [ResponseCode](responsecode.md) and [MessageText](messagetext.md) elements.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ae92f-142">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ae92f-142">Child elements</span></span>

|<span data-ttu-id="ae92f-143">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="ae92f-143">**Element**</span></span>|<span data-ttu-id="ae92f-144">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ae92f-144">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ae92f-145">MessageText</span><span class="sxs-lookup"><span data-stu-id="ae92f-145">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="ae92f-146">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ae92f-146">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-147">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="ae92f-147">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="ae92f-148">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ae92f-148">Provides an error code that identifies the specific error that the request encountered.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-149">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="ae92f-149">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="ae92f-150">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="ae92f-150">Currently unused and reserved for future use.</span></span> <span data-ttu-id="ae92f-151">Este elemento contiene un valor de 0.</span><span class="sxs-lookup"><span data-stu-id="ae92f-151">This element contains a value of 0.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-152">MessageXml</span><span class="sxs-lookup"><span data-stu-id="ae92f-152">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="ae92f-153">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="ae92f-153">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-154">Diagnóstico</span><span class="sxs-lookup"><span data-stu-id="ae92f-154">Diagnostics</span></span>](diagnostics.md) <br/> |<span data-ttu-id="ae92f-155">Contiene la información que se usará para generar varios informes estadísticos para la característica de seguimiento en un centro de datos.</span><span class="sxs-lookup"><span data-stu-id="ae92f-155">Contains information that will be used to produce various statistical reports for the tracking feature in a DataCenter.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-156">MessageTrackingSearchResults</span><span class="sxs-lookup"><span data-stu-id="ae92f-156">MessageTrackingSearchResults</span></span>](messagetrackingsearchresults.md) <br/> |<span data-ttu-id="ae92f-157">Contiene y matriz de mensajes que coinciden con los requisitos de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae92f-157">Contains and array of messages that match the search requirements.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-158">ExecutedSearchScope</span><span class="sxs-lookup"><span data-stu-id="ae92f-158">ExecutedSearchScope</span></span>](executedsearchscope.md) <br/> |<span data-ttu-id="ae92f-159">Contiene el ámbito de la búsqueda que se ha realizado para obtener los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="ae92f-159">Contains the scope of the search that was performed to get the search results.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-160">Errores</span><span class="sxs-lookup"><span data-stu-id="ae92f-160">Errors</span></span>](errors-ex15websvcsotherref.md) <br/> |<span data-ttu-id="ae92f-161">Contiene un contenedor de propiedades donde se almacenan los errores que se devuelven a través del servicio Web.</span><span class="sxs-lookup"><span data-stu-id="ae92f-161">Contains a property bag to store errors that are returned through the Web service.</span></span>  <br/> |
|[<span data-ttu-id="ae92f-162">Propiedades (ArrayOfTrackingPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="ae92f-162">Properties (ArrayOfTrackingPropertiesType)</span></span>](properties-arrayoftrackingpropertiestype.md) <br/> |<span data-ttu-id="ae92f-163">Contiene una lista de una o varias propiedades de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="ae92f-163">Contains a list of one or more tracking properties.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ae92f-164">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="ae92f-164">Parent elements</span></span>

<span data-ttu-id="ae92f-165">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ae92f-165">None.</span></span>
  
## <a name="text-value"></a><span data-ttu-id="ae92f-166">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="ae92f-166">Text value</span></span>

<span data-ttu-id="ae92f-167">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ae92f-167">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae92f-168">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ae92f-168">Remarks</span></span>

<span data-ttu-id="ae92f-169">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="ae92f-169">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ae92f-170">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="ae92f-170">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae92f-171">Namespace</span><span class="sxs-lookup"><span data-stu-id="ae92f-171">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="ae92f-172">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="ae92f-172">Schema Name</span></span>  <br/> |<span data-ttu-id="ae92f-173">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="ae92f-173">Messages schema</span></span>  <br/> |
|<span data-ttu-id="ae92f-174">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="ae92f-174">Validation File</span></span>  <br/> |<span data-ttu-id="ae92f-175">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="ae92f-175">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="ae92f-176">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="ae92f-176">Can be Empty</span></span>  <br/> |<span data-ttu-id="ae92f-177">Falso</span><span class="sxs-lookup"><span data-stu-id="ae92f-177">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ae92f-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae92f-178">See also</span></span>

- [<span data-ttu-id="ae92f-179">Operación FindMessageTrackingReport</span><span class="sxs-lookup"><span data-stu-id="ae92f-179">FindMessageTrackingReport operation</span></span>](findmessagetrackingreport-operation.md)
- [<span data-ttu-id="ae92f-180">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="ae92f-180">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

