---
title: GetClientAccessTokenResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45ca2500-ceab-4c98-9576-cb9e158e5896
description: El elemento GetClientAccessTokenResponseMessage especifica el mensaje de respuesta para una solicitud de GetClientAccessToken.
ms.openlocfilehash: e842353dfe91fa7df410203b53e22d5ec53e1e39
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526686"
---
# <a name="getclientaccesstokenresponsemessage"></a><span data-ttu-id="4a5b0-103">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4a5b0-103">GetClientAccessTokenResponseMessage</span></span>

<span data-ttu-id="4a5b0-104">El elemento **GetClientAccessTokenResponseMessage** especifica el mensaje de respuesta para una solicitud de **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="4a5b0-104">The **GetClientAccessTokenResponseMessage** element specifies the response message for a **GetClientAccessToken** request.</span></span> 
  
```XML
<GetClientAccessTokenResponseMessage ResponseClass=" Success | Warning | Error ">
    <Token/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetClientAccessTokenResponseMessage>
```

 <span data-ttu-id="4a5b0-105">**GetClientAccessTokenResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-105">**GetClientAccessTokenResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4a5b0-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="4a5b0-106">Attributes and elements</span></span>

<span data-ttu-id="4a5b0-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4a5b0-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="4a5b0-108">Attributes</span></span>

|<span data-ttu-id="4a5b0-109">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-109">**Attribute**</span></span>|<span data-ttu-id="4a5b0-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a5b0-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4a5b0-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="4a5b0-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="4a5b0-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="4a5b0-113">ResponseClass</span></span>

|<span data-ttu-id="4a5b0-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-114">**Value**</span></span>|<span data-ttu-id="4a5b0-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4a5b0-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="4a5b0-116">Success</span></span>  <br/> |<span data-ttu-id="4a5b0-117">Indica que se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="4a5b0-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="4a5b0-118">Warning</span></span>  <br/> |<span data-ttu-id="4a5b0-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="4a5b0-120">Error</span><span class="sxs-lookup"><span data-stu-id="4a5b0-120">Error</span></span>  <br/> |<span data-ttu-id="4a5b0-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4a5b0-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4a5b0-122">Child elements</span></span>

|<span data-ttu-id="4a5b0-123">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-123">**Element**</span></span>|<span data-ttu-id="4a5b0-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a5b0-125">Token (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="4a5b0-125">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md) <br/> |<span data-ttu-id="4a5b0-126">Especifica un token de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-126">Specifies a client access token.</span></span>  <br/> |
|[<span data-ttu-id="4a5b0-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="4a5b0-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="4a5b0-128">Actualmente no está en uso y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="4a5b0-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="4a5b0-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="4a5b0-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="4a5b0-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="4a5b0-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="4a5b0-132">Proporciona información de respuesta de error adicional.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="4a5b0-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="4a5b0-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="4a5b0-134">Proporciona información de estado sobre la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4a5b0-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="4a5b0-135">Parent elements</span></span>

|<span data-ttu-id="4a5b0-136">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-136">**Element**</span></span>|<span data-ttu-id="4a5b0-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4a5b0-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4a5b0-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="4a5b0-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="4a5b0-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="4a5b0-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4a5b0-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4a5b0-140">Remarks</span></span>

<span data-ttu-id="4a5b0-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="4a5b0-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="4a5b0-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4a5b0-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="4a5b0-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4a5b0-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="4a5b0-144">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="4a5b0-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="4a5b0-145">Schema Name</span></span>  <br/> |<span data-ttu-id="4a5b0-146">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="4a5b0-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="4a5b0-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="4a5b0-147">Validation File</span></span>  <br/> |<span data-ttu-id="4a5b0-148">messages. xsd</span><span class="sxs-lookup"><span data-stu-id="4a5b0-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="4a5b0-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="4a5b0-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="4a5b0-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a5b0-150">See also</span></span>



- [<span data-ttu-id="4a5b0-151">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="4a5b0-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

