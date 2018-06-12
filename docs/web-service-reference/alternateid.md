---
title: AlternateId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AlternateId
api_type:
- schema
ms.assetid: 9c01fdc3-4adf-4e23-bc33-45d2a45ea08b
description: El elemento AlternateId describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta.
ms.openlocfilehash: e4d29087b63b52638dd93e4e3b643cdee39a5b97
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763428"
---
# <a name="alternateid"></a><span data-ttu-id="8d252-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="8d252-103">AlternateId</span></span>

<span data-ttu-id="8d252-104">El elemento **AlternateId** describe un identificador para convertir en una solicitud y los resultados de un identificador convertido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d252-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="8d252-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="8d252-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d252-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="8d252-106">Attributes and elements</span></span>

<span data-ttu-id="8d252-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="8d252-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d252-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="8d252-108">Attributes</span></span>

|<span data-ttu-id="8d252-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="8d252-109">**Attribute**</span></span>|<span data-ttu-id="8d252-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d252-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d252-111">Id</span><span class="sxs-lookup"><span data-stu-id="8d252-111">Id</span></span>  <br/> |<span data-ttu-id="8d252-112">Describe el identificador de origen en una solicitud de [operación de ConvertId](convertid-operation.md) y el identificador de destino en una respuesta de la [operación de ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8d252-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="8d252-113">Format</span><span class="sxs-lookup"><span data-stu-id="8d252-113">Format</span></span>  <br/> |<span data-ttu-id="8d252-114">Describe el formato de origen en una solicitud de [operación de ConvertId](convertid-operation.md) y se describe el formato de destino en una respuesta de la [operación de ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8d252-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="8d252-115">Se describe el formato de destino mediante el atributo **DestinationFormat** del elemento [ConvertId](convertid.md) en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d252-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="8d252-116">Este atributo es del tipo **IdFormatType**.</span><span class="sxs-lookup"><span data-stu-id="8d252-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="8d252-117">Buz?n de correo</span><span class="sxs-lookup"><span data-stu-id="8d252-117">Mailbox</span></span>  <br/> |<span data-ttu-id="8d252-118">Describe la dirección de Protocolo Simple de transferencia de correo (SMTP) principal de buzón de correo que contiene los identificadores para traducir.</span><span class="sxs-lookup"><span data-stu-id="8d252-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="8d252-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="8d252-119">IsArchive</span></span>  <br/> |<span data-ttu-id="8d252-120">Indica si el identificador representa una carpeta o elemento archivado.</span><span class="sxs-lookup"><span data-stu-id="8d252-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="8d252-121">Un valor de **true** indica que el identificador representa una carpeta o elemento archivado.</span><span class="sxs-lookup"><span data-stu-id="8d252-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="8d252-122">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="8d252-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="8d252-123">Valores de atributos de formato</span><span class="sxs-lookup"><span data-stu-id="8d252-123">Format attribute values</span></span>

|<span data-ttu-id="8d252-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8d252-124">**Value**</span></span>|<span data-ttu-id="8d252-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d252-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8d252-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="8d252-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="8d252-127">Describe identificadores producidos por servicios Web de Exchange en la versión inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="8d252-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="8d252-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="8d252-128">EwsId</span></span>  <br/> |<span data-ttu-id="8d252-129">Describe identificadores producidos por los servicios Web Exchange comenzando con Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="8d252-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="8d252-130">Propiedad EntryId</span><span class="sxs-lookup"><span data-stu-id="8d252-130">EntryId</span></span>  <br/> |<span data-ttu-id="8d252-131">Describe identificadores de MAPI, como se muestra en la propiedad de **entrada del objeto** .</span><span class="sxs-lookup"><span data-stu-id="8d252-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="8d252-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="8d252-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="8d252-133">Describe una representación codificada en hexadecimal de la propiedad de **entrada del objeto** .</span><span class="sxs-lookup"><span data-stu-id="8d252-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="8d252-134">Éste es el formato de los identificadores de eventos de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="8d252-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="8d252-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="8d252-135">StoreId</span></span>  <br/> |<span data-ttu-id="8d252-136">Describe identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="8d252-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="8d252-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="8d252-137">OwaId</span></span>  <br/> |<span data-ttu-id="8d252-138">Se describe un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="8d252-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="8d252-139">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="8d252-139">Child elements</span></span>

<span data-ttu-id="8d252-140">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d252-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8d252-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="8d252-141">Parent elements</span></span>

|<span data-ttu-id="8d252-142">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d252-142">**Element**</span></span>|<span data-ttu-id="8d252-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8d252-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d252-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="8d252-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="8d252-145">Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="8d252-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="8d252-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="8d252-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="8d252-147">Contiene los identificadores de origen para convertir.</span><span class="sxs-lookup"><span data-stu-id="8d252-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8d252-148">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="8d252-148">Text value</span></span>

<span data-ttu-id="8d252-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="8d252-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d252-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d252-150">Remarks</span></span>

<span data-ttu-id="8d252-151">El elemento **AlternateId** describe dos identificadores, el identificador de origen que se convierte en la solicitud de la [operación de ConvertId](convertid-operation.md) y el identificador convertido en el elemento [ConvertIdResponse](convertidresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="8d252-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="8d252-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="8d252-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d252-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="8d252-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="8d252-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8d252-154">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d252-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="8d252-155">Schema Name</span></span>  <br/> |<span data-ttu-id="8d252-156">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="8d252-156">Messages schema</span></span>  <br/> |<span data-ttu-id="8d252-157">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="8d252-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d252-158">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="8d252-158">Validation File</span></span>  <br/> |<span data-ttu-id="8d252-159">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="8d252-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="8d252-160">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d252-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d252-161">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="8d252-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d252-162">False</span><span class="sxs-lookup"><span data-stu-id="8d252-162">False</span></span>  <br/> |<span data-ttu-id="8d252-163">False</span><span class="sxs-lookup"><span data-stu-id="8d252-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d252-164">Ver también</span><span class="sxs-lookup"><span data-stu-id="8d252-164">See also</span></span>

- [<span data-ttu-id="8d252-165">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="8d252-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="8d252-166">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="8d252-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="8d252-167">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="8d252-167">Converting Identifiers</span></span>](http://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

