---
title: GetItem Operation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GetItem
api_type:
- schema
ms.assetid: e3590b8b-c2a7-4dad-a014-6360197b68e4
description: Busque información sobre la EWS GetItem operación.
ms.openlocfilehash: 9b63032b2eaa3bf26027a42e38bfa06bedcbac86
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19764892"
---
# <a name="getitem-operation"></a><span data-ttu-id="16622-103">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="16622-103">GetItem operation</span></span>

<span data-ttu-id="16622-104">Obtenga información acerca de la operación de EWS **GetItem** .</span><span class="sxs-lookup"><span data-stu-id="16622-104">Find information about the **GetItem** EWS operation.</span></span> 
  
<span data-ttu-id="16622-105">La operación **GetItem** obtiene los elementos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="16622-105">The **GetItem** operation gets items from the Exchange store.</span></span> 
  
## <a name="using-the-getitem-operation"></a><span data-ttu-id="16622-106">Mediante la operación GetItem</span><span class="sxs-lookup"><span data-stu-id="16622-106">Using the GetItem operation</span></span>

<span data-ttu-id="16622-107">La operación **GetItem** devuelve muchas propiedades de elemento.</span><span class="sxs-lookup"><span data-stu-id="16622-107">The **GetItem** operation returns many item properties.</span></span> <span data-ttu-id="16622-108">Las propiedades que se devuelven en una respuesta **GetItem** varían en función de la forma solicitada, propiedades adicionales solicitadas y el tipo de elemento devuelven.</span><span class="sxs-lookup"><span data-stu-id="16622-108">The properties that are returned in a **GetItem** response vary based on the requested shape, requested additional properties, and the type of item returned.</span></span> 
  
<span data-ttu-id="16622-109">Elementos del [mensaje](message-ex15websvcsotherref.md) representan los mensajes de correo electrónico y todos los otros elementos que no están fuertemente tipados por el esquema de Exchange Web Services (EWS).</span><span class="sxs-lookup"><span data-stu-id="16622-109">[Message](message-ex15websvcsotherref.md) elements represent email messages and all other items that are not strongly typed by the Exchange Web Services (EWS) schema.</span></span> <span data-ttu-id="16622-110">Elementos como IPM. Uso compartido y IPM.InfoPath se devuelven como elementos del [mensaje](message-ex15websvcsotherref.md) .</span><span class="sxs-lookup"><span data-stu-id="16622-110">Items such as IPM.Sharing and IPM.InfoPath are returned as [Message](message-ex15websvcsotherref.md) elements.</span></span> <span data-ttu-id="16622-111">Exchange no devuelve [el elemento de base](item.md) de las respuestas.</span><span class="sxs-lookup"><span data-stu-id="16622-111">Exchange does not return the base [Item](item.md) element in responses.</span></span> 
  
<span data-ttu-id="16622-112">La operación **GetItem** no devuelve datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="16622-112">The **GetItem** operation does not return attachments.</span></span> <span data-ttu-id="16622-113">Devuelven los metadatos sobre un elemento adjunto o un archivo.</span><span class="sxs-lookup"><span data-stu-id="16622-113">It does return metadata about an attached item or file.</span></span> <span data-ttu-id="16622-114">Para devolver un dato adjunto, use la [operación GetAttachment](getattachment-operation.md).</span><span class="sxs-lookup"><span data-stu-id="16622-114">To return an attachment, use the [GetAttachment operation](getattachment-operation.md).</span></span>
  
## <a name="getitem-operation-soap-headers"></a><span data-ttu-id="16622-115">Encabezados SOAP de GetItem operación</span><span class="sxs-lookup"><span data-stu-id="16622-115">GetItem operation SOAP headers</span></span>

<span data-ttu-id="16622-116">La operación **GetItem** puede usar los encabezados SOAP que se enumeran en la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="16622-116">The **GetItem** operation can use the SOAP headers that are listed in the following table.</span></span> 
  
|<span data-ttu-id="16622-117">Encabezado \*\*\*</span><span class="sxs-lookup"><span data-stu-id="16622-117">****Header****</span></span>|<span data-ttu-id="16622-118">****Element****</span><span class="sxs-lookup"><span data-stu-id="16622-118">****Element****</span></span>|<span data-ttu-id="16622-119">****Descripción****</span><span class="sxs-lookup"><span data-stu-id="16622-119">****Description****</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="16622-120">**DateTimePrecision**</span><span class="sxs-lookup"><span data-stu-id="16622-120">**DateTimePrecision**</span></span> <br/> |[<span data-ttu-id="16622-121">DateTimePrecision</span><span class="sxs-lookup"><span data-stu-id="16622-121">DateTimePrecision</span></span>](datetimeprecision.md) <br/> |<span data-ttu-id="16622-122">Especifica la resolución de los valores de fecha y hora en las respuestas desde el servidor, en segundos o en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="16622-122">Specifies the resolution of data/time values in responses from the server, either in seconds or in milliseconds.</span></span>  <br/> |
|<span data-ttu-id="16622-123">**Suplantación**</span><span class="sxs-lookup"><span data-stu-id="16622-123">**Impersonation**</span></span> <br/> |[<span data-ttu-id="16622-124">ExchangeImpersonation</span><span class="sxs-lookup"><span data-stu-id="16622-124">ExchangeImpersonation</span></span>](exchangeimpersonation.md) <br/> |<span data-ttu-id="16622-125">Identifica el usuario que está realizando la suplantación de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="16622-125">Identifies the user whom the client application is impersonating.</span></span>  <br/> |
|<span data-ttu-id="16622-126">**MailboxCulture**</span><span class="sxs-lookup"><span data-stu-id="16622-126">**MailboxCulture**</span></span> <br/> |[<span data-ttu-id="16622-127">MailboxCulture</span><span class="sxs-lookup"><span data-stu-id="16622-127">MailboxCulture</span></span>](mailboxculture.md) <br/> |<span data-ttu-id="16622-128">Identifica la referencia cultural, como se define en RFC 3066, "Etiquetas para la identificación de idiomas," que se utilizará para acceder al buzón.</span><span class="sxs-lookup"><span data-stu-id="16622-128">Identifies the culture, as defined in RFC 3066, "Tags for the Identification of Languages", to be used to access the mailbox.</span></span>  <br/> |
|<span data-ttu-id="16622-129">**RequestVersion**</span><span class="sxs-lookup"><span data-stu-id="16622-129">**RequestVersion**</span></span> <br/> |[<span data-ttu-id="16622-130">RequestServerVersion</span><span class="sxs-lookup"><span data-stu-id="16622-130">RequestServerVersion</span></span>](requestserverversion.md) <br/> |<span data-ttu-id="16622-131">Identifica la versión del esquema para la solicitud de la operación.</span><span class="sxs-lookup"><span data-stu-id="16622-131">Identifies the schema version for the operation request.</span></span>  <br/> |
|<span data-ttu-id="16622-132">**ServerVersion**</span><span class="sxs-lookup"><span data-stu-id="16622-132">**ServerVersion**</span></span> <br/> |[<span data-ttu-id="16622-133">ServerVersionInfo</span><span class="sxs-lookup"><span data-stu-id="16622-133">ServerVersionInfo</span></span>](serverversioninfo.md) <br/> |<span data-ttu-id="16622-134">Identifica la versión del servidor que ha respondido a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="16622-134">Identifies the version of the server that responded to the request.</span></span>  <br/> |
|<span data-ttu-id="16622-135">**TimeZoneContext**</span><span class="sxs-lookup"><span data-stu-id="16622-135">**TimeZoneContext**</span></span> <br/> |[<span data-ttu-id="16622-136">TimeZoneContext</span><span class="sxs-lookup"><span data-stu-id="16622-136">TimeZoneContext</span></span>](timezonecontext.md) <br/> |<span data-ttu-id="16622-137">Identifica la zona horaria que se usará para todas las respuestas desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="16622-137">Identifies the time zone to be used for all responses from the server.</span></span>  <br/> |
   
## <a name="in-this-section"></a><span data-ttu-id="16622-138">En esta sección</span><span class="sxs-lookup"><span data-stu-id="16622-138">In This Section</span></span>

[<span data-ttu-id="16622-139">Operación GetItem (mensaje de correo electrónico)</span><span class="sxs-lookup"><span data-stu-id="16622-139">GetItem operation (email message)</span></span>](getitem-operation-email-message.md)
  
[<span data-ttu-id="16622-140">Operación GetItem (elemento de calendario)</span><span class="sxs-lookup"><span data-stu-id="16622-140">GetItem operation (calendar item)</span></span>](getitem-operation-calendar-item.md)
  
[<span data-ttu-id="16622-141">Operación GetItem (tarea)</span><span class="sxs-lookup"><span data-stu-id="16622-141">GetItem operation (task)</span></span>](getitem-operation-task.md)
  
[<span data-ttu-id="16622-142">Operación GetItem (contacto)</span><span class="sxs-lookup"><span data-stu-id="16622-142">GetItem operation (contact)</span></span>](getitem-operation-contact.md)
  
## <a name="see-also"></a><span data-ttu-id="16622-143">Ver también</span><span class="sxs-lookup"><span data-stu-id="16622-143">See also</span></span>



[<span data-ttu-id="16622-144">Referencia EWS para Exchange</span><span class="sxs-lookup"><span data-stu-id="16622-144">EWS reference for Exchange</span></span>](ews-reference-for-exchange.md)

