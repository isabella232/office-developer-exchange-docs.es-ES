---
title: Operación GetItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Busque información sobre la operación de EWS de GetItem.
localization_priority: Priority
ms.openlocfilehash: 8871dde183974454fc27dbddda489e6b0a70f3aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463331"
---
# <a name="getitem-operation"></a><span data-ttu-id="a0328-103">Operación GetItem</span><span class="sxs-lookup"><span data-stu-id="a0328-103">GetItem operation</span></span>

<span data-ttu-id="a0328-104">Busque información sobre la operación de EWS de **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="a0328-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="a0328-105">La operación **GetItem** obtiene elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="a0328-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="a0328-106">Uso de la operación GetItem</span><span class="sxs-lookup"><span data-stu-id="a0328-106">Using the GetItem operation</span></span>

<span data-ttu-id="a0328-107">La operación **GetItem** devuelve muchas propiedades de elemento.</span><span class="sxs-lookup"><span data-stu-id="a0328-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="a0328-108">Las propiedades que se devuelven en una respuesta **GetItem** varían en función de la forma solicitada, las propiedades adicionales solicitadas y el tipo de elemento devuelto.</span><span class="sxs-lookup"><span data-stu-id="a0328-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="a0328-109">Los elementos de [mensaje](message-ex15websvcsotherref.md) representan mensajes de correo electrónico y todos los demás elementos que no son fuertemente tipados por el esquema de servicios web Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="a0328-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="a0328-110">Elementos como IPM. Uso compartido e IPM. InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="a0328-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="a0328-111">Exchange no devuelve el elemento de [elemento](item.md) base en las respuestas.</span><span class="sxs-lookup"><span data-stu-id="a0328-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="a0328-112">La operación **GetItem** no devuelve datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="a0328-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="a0328-113">Devuelve los metadatos de un archivo o elemento adjunto.</span><span class="sxs-lookup"><span data-stu-id="a0328-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="a0328-114">Para devolver un dato adjunto, use la [operación GetAttachment](getattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="a0328-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="a0328-115">Encabezados SOAP de la operación GetItem</span><span class="sxs-lookup"><span data-stu-id="a0328-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="a0328-116">La operación **GetItem** puede usar los encabezados SOAP que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a0328-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="a0328-117">Encabezado \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="a0328-117">\*\*\*\*Header\*\*\*\*</span></span>|<span data-ttu-id="a0328-118">\*\*\*\*Element\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0328-118">\*\*\*\*Element\*\*\*\*</span></span>|<span data-ttu-id="a0328-119">\*\*\*\*Descripción\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a0328-119">\*\*\*\*Description\*\*\*\*</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0328-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="a0328-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="a0328-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="a0328-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="a0328-122">Especifica la resolución de los valores de datos/tiempo en respuestas del servidor, en segundos o en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a0328-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="a0328-123">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="a0328-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="a0328-124">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="a0328-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="a0328-125">Identifica al usuario que está suplantando la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="a0328-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="a0328-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="a0328-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="a0328-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="a0328-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="a0328-128">Identifica la referencia cultural, tal y como se define en RFC 3066, "etiquetas para la identificación de idiomas", que se va a usar para obtener acceso al buzón.</span><span class="sxs-lookup"><span data-stu-id="a0328-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="a0328-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="a0328-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="a0328-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="a0328-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="a0328-131">Identifica la versión del esquema para la solicitud de operación.</span><span class="sxs-lookup"><span data-stu-id="a0328-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="a0328-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="a0328-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="a0328-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="a0328-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="a0328-134">Identifica la versión del servidor que respondió a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a0328-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="a0328-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="a0328-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="a0328-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="a0328-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="a0328-137">Identifica la zona horaria que se va a usar para todas las respuestas del servidor.</span><span class="sxs-lookup"><span data-stu-id="a0328-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="a0328-138">En esta sección</span><span class="sxs-lookup"><span data-stu-id="a0328-138">In This Section</span></span>

[<span data-ttu-id="a0328-139">Operación GetItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="a0328-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="a0328-140">Operación GetItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="a0328-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="a0328-141">Operación GetItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="a0328-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="a0328-142">Operación GetItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="a0328-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="a0328-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0328-143">See also</span></span>



[<span data-ttu-id="a0328-144">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="a0328-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

