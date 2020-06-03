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
description: El elemento AlternateId describe un identificador que se va a convertir en una solicitud y los resultados de un identificador convertido en la respuesta.
ms.openlocfilehash: 26df68bd814c2d323630c6bb40b4c31745017c71
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527456"
---
# <a name="alternateid"></a><span data-ttu-id="58268-103">AlternateId</span><span class="sxs-lookup"><span data-stu-id="58268-103">AlternateId</span></span>

<span data-ttu-id="58268-104">El elemento **AlternateId** describe un identificador que se va a convertir en una solicitud y los resultados de un identificador convertido en la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58268-104">The **AlternateId** element describes an identifier to convert in a request and the results of a converted identifier in the response.</span></span> 
  
```XML
<AlternateId Id="" Format="" Mailbox="" IsArchive=""/>
```

 <span data-ttu-id="58268-105">**AlternateIdType**</span><span class="sxs-lookup"><span data-stu-id="58268-105">**AlternateIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="58268-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="58268-106">Attributes and elements</span></span>

<span data-ttu-id="58268-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="58268-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="58268-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="58268-108">Attributes</span></span>

|<span data-ttu-id="58268-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="58268-109">**Attribute**</span></span>|<span data-ttu-id="58268-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58268-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58268-111">Id</span><span class="sxs-lookup"><span data-stu-id="58268-111">Id</span></span>  <br/> |<span data-ttu-id="58268-112">Describe el identificador de origen en una solicitud de [operación ConvertId](convertid-operation.md) y describe el identificador de destino en una respuesta de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="58268-112">Describes the source identifier in a [ConvertId operation](convertid-operation.md) request and describes the destination identifier in a [ConvertId operation](convertid-operation.md) response.</span></span>  <br/> |
|<span data-ttu-id="58268-113">Formato</span><span class="sxs-lookup"><span data-stu-id="58268-113">Format</span></span>  <br/> |<span data-ttu-id="58268-114">Describe el formato de origen en una solicitud de [operación ConvertId](convertid-operation.md) y describe el formato de destino en una respuesta de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="58268-114">Describes the source format in a [ConvertId operation](convertid-operation.md) request and describes the destination format in a [ConvertId operation](convertid-operation.md) response.</span></span> <span data-ttu-id="58268-115">El formato de destino se describe mediante el atributo **DestinationFormat** del elemento [ConvertId](convertid.md) en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58268-115">The destination format is described by the **DestinationFormat** attribute of the [ConvertId](convertid.md) element in the request.</span></span> <span data-ttu-id="58268-116">Este atributo es del tipo **IdFormatType**.</span><span class="sxs-lookup"><span data-stu-id="58268-116">This attribute is of type **IdFormatType**.</span></span>  <br/> |
|<span data-ttu-id="58268-117">Buzón de correo</span><span class="sxs-lookup"><span data-stu-id="58268-117">Mailbox</span></span>  <br/> |<span data-ttu-id="58268-118">Describe la dirección del Protocolo simple de transferencia de correo (SMTP) principal del buzón que contiene los identificadores que se van a traducir.</span><span class="sxs-lookup"><span data-stu-id="58268-118">Describes the mailbox primary Simple Mail Transfer Protocol (SMTP) address that contains the identifiers to translate.</span></span>  <br/> |
|<span data-ttu-id="58268-119">IsArchive</span><span class="sxs-lookup"><span data-stu-id="58268-119">IsArchive</span></span>  <br/> |<span data-ttu-id="58268-120">Indica si el identificador representa un elemento o una carpeta archivados.</span><span class="sxs-lookup"><span data-stu-id="58268-120">Indicates whether the identifier represents an archived item or folder.</span></span> <span data-ttu-id="58268-121">Un valor de **true** indica que el identificador representa un elemento o una carpeta archivados.</span><span class="sxs-lookup"><span data-stu-id="58268-121">A value of **true** indicates that the identifier represents an archived item or folder.</span></span> <span data-ttu-id="58268-122">Este atributo es opcional.</span><span class="sxs-lookup"><span data-stu-id="58268-122">This attribute is optional.</span></span>  <br/> |
   
#### <a name="format-attribute-values"></a><span data-ttu-id="58268-123">Valores de atributo de formato</span><span class="sxs-lookup"><span data-stu-id="58268-123">Format attribute values</span></span>

|<span data-ttu-id="58268-124">**Valor**</span><span class="sxs-lookup"><span data-stu-id="58268-124">**Value**</span></span>|<span data-ttu-id="58268-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58268-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58268-126">EwsLegacyId</span><span class="sxs-lookup"><span data-stu-id="58268-126">EwsLegacyId</span></span>  <br/> |<span data-ttu-id="58268-127">Describe los identificadores producidos por los servicios Web de Exchange en la versión de lanzamiento inicial de Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="58268-127">Describes identifiers that are produced by Exchange Web Services in the initial release version of Exchange 2007.</span></span>  <br/> |
|<span data-ttu-id="58268-128">EwsId</span><span class="sxs-lookup"><span data-stu-id="58268-128">EwsId</span></span>  <br/> |<span data-ttu-id="58268-129">Describe los identificadores que crean los servicios Web de Exchange a partir de Exchange 2007 SP1.</span><span class="sxs-lookup"><span data-stu-id="58268-129">Describes identifiers that are produced by Exchange Web Services starting with Exchange 2007 SP1.</span></span>  <br/> |
|<span data-ttu-id="58268-130">EntryId</span><span class="sxs-lookup"><span data-stu-id="58268-130">EntryId</span></span>  <br/> |<span data-ttu-id="58268-131">Describe los identificadores de MAPI, como en la propiedad **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="58268-131">Describes MAPI identifiers, as in the **PR_ENTRYID** property.</span></span>  <br/> |
|<span data-ttu-id="58268-132">HexEntryId</span><span class="sxs-lookup"><span data-stu-id="58268-132">HexEntryId</span></span>  <br/> |<span data-ttu-id="58268-133">Describe una representación codificada en hexadecimal de la propiedad **PR_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="58268-133">Describes a hexadecimal-encoded representation of the **PR_ENTRYID** property.</span></span> <span data-ttu-id="58268-134">Este es el formato de los identificadores de evento de calendario de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="58268-134">This is the format of availability calendar event identifiers.</span></span>  <br/> |
|<span data-ttu-id="58268-135">StoreId</span><span class="sxs-lookup"><span data-stu-id="58268-135">StoreId</span></span>  <br/> |<span data-ttu-id="58268-136">Describe los identificadores de almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="58268-136">Describes Exchange store identifiers.</span></span>  <br/> |
|<span data-ttu-id="58268-137">OwaId</span><span class="sxs-lookup"><span data-stu-id="58268-137">OwaId</span></span>  <br/> |<span data-ttu-id="58268-138">Describe un identificador de Outlook Web App.</span><span class="sxs-lookup"><span data-stu-id="58268-138">Describes an Outlook Web App identifier.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="58268-139">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="58268-139">Child elements</span></span>

<span data-ttu-id="58268-140">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="58268-140">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="58268-141">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="58268-141">Parent elements</span></span>

|<span data-ttu-id="58268-142">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="58268-142">**Element**</span></span>|<span data-ttu-id="58268-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="58268-143">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="58268-144">ConvertIdResponseMessage</span><span class="sxs-lookup"><span data-stu-id="58268-144">ConvertIdResponseMessage</span></span>](convertidresponsemessage.md) <br/> |<span data-ttu-id="58268-145">Contiene el estado y el resultado de una solicitud de [operación ConvertId](convertid-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="58268-145">Contains the status and result of a [ConvertId operation](convertid-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="58268-146">SourceIds</span><span class="sxs-lookup"><span data-stu-id="58268-146">SourceIds</span></span>](sourceids.md) <br/> |<span data-ttu-id="58268-147">Contiene los identificadores de origen que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="58268-147">Contains the source identifiers to convert.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="58268-148">Valor de texto</span><span class="sxs-lookup"><span data-stu-id="58268-148">Text value</span></span>

<span data-ttu-id="58268-149">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="58268-149">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58268-150">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58268-150">Remarks</span></span>

<span data-ttu-id="58268-151">El elemento **AlternateId** describe dos identificadores, el identificador de origen que se va a convertir en la solicitud de [operación ConvertId](convertid-operation.md) y el identificador convertido en el elemento [ConvertIdResponse](convertidresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="58268-151">The **AlternateId** element describes two identifiers, the source identifier that is to be converted in the [ConvertId operation](convertid-operation.md) request, and the converted identifier in the [ConvertIdResponse](convertidresponse.md) element.</span></span> 
  
<span data-ttu-id="58268-152">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="58268-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="58268-153">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="58268-153">Element information</span></span>

||||
|:-----|:-----|:-----|
|<span data-ttu-id="58268-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="58268-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="58268-155">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="58268-155">Schema Name</span></span>  <br/> |<span data-ttu-id="58268-156">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="58268-156">Messages schema</span></span>  <br/> |<span data-ttu-id="58268-157">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="58268-157">Types schema</span></span>  <br/> |
|<span data-ttu-id="58268-158">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="58268-158">Validation File</span></span>  <br/> |<span data-ttu-id="58268-159">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="58268-159">Messages.xsd</span></span>  <br/> |<span data-ttu-id="58268-160">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="58268-160">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="58268-161">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="58268-161">Can be Empty</span></span>  <br/> |<span data-ttu-id="58268-162">Falso</span><span class="sxs-lookup"><span data-stu-id="58268-162">False</span></span>  <br/> |<span data-ttu-id="58268-163">Falso</span><span class="sxs-lookup"><span data-stu-id="58268-163">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58268-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="58268-164">See also</span></span>

- [<span data-ttu-id="58268-165">Operación ConvertId</span><span class="sxs-lookup"><span data-stu-id="58268-165">ConvertId operation</span></span>](convertid-operation.md)
- [<span data-ttu-id="58268-166">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="58268-166">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)
- [<span data-ttu-id="58268-167">Convertir identificadores</span><span class="sxs-lookup"><span data-stu-id="58268-167">Converting Identifiers</span></span>](https://msdn.microsoft.com/library/a5391746-b6ef-4f48-8fc8-8255258651aa%28Office.15%29.aspx)

