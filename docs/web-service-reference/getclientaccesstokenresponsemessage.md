---
title: GetClientAccessTokenResponseMessage
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 45ca2500-ceab-4c98-9576-cb9e158e5896
description: El elemento GetClientAccessTokenResponseMessage especifica el mensaje de respuesta de una solicitud de GetClientAccessToken.
ms.openlocfilehash: 16fe684dd48f77156ed88d02a6ae7b8f3312cd87
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19764772"
---
# <a name="getclientaccesstokenresponsemessage"></a><span data-ttu-id="90b3c-103">GetClientAccessTokenResponseMessage</span><span class="sxs-lookup"><span data-stu-id="90b3c-103">GetClientAccessTokenResponseMessage</span></span>

<span data-ttu-id="90b3c-104">El elemento **GetClientAccessTokenResponseMessage** especifica el mensaje de respuesta de una solicitud de **GetClientAccessToken** .</span><span class="sxs-lookup"><span data-stu-id="90b3c-104">The **GetClientAccessTokenResponseMessage** element specifies the response message for a **GetClientAccessToken** request.</span></span> 
  
```XML
<GetClientAccessTokenResponseMessage ResponseClass=" Success | Warning | Error ">
    <Token/>
    <MessageText/>
    <ResponseCode/>
    <DescriptiveLinkKey/>
    <MessageXml/>
</GetClientAccessTokenResponseMessage>
```

 <span data-ttu-id="90b3c-105">**GetClientAccessTokenResponseMessageType**</span><span class="sxs-lookup"><span data-stu-id="90b3c-105">**GetClientAccessTokenResponseMessageType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="90b3c-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="90b3c-106">Attributes and elements</span></span>

<span data-ttu-id="90b3c-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="90b3c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90b3c-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="90b3c-108">Attributes</span></span>

|<span data-ttu-id="90b3c-109">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="90b3c-109">**Attribute**</span></span>|<span data-ttu-id="90b3c-110">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90b3c-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90b3c-111">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="90b3c-111">ResponseClass</span></span>  <br/> |<span data-ttu-id="90b3c-112">Indica la clase de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90b3c-112">Indicates the class of the response.</span></span>  <br/> |
   
#### <a name="responseclass"></a><span data-ttu-id="90b3c-113">ResponseClass</span><span class="sxs-lookup"><span data-stu-id="90b3c-113">ResponseClass</span></span>

|<span data-ttu-id="90b3c-114">**Valor**</span><span class="sxs-lookup"><span data-stu-id="90b3c-114">**Value**</span></span>|<span data-ttu-id="90b3c-115">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90b3c-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90b3c-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="90b3c-116">Success</span></span>  <br/> |<span data-ttu-id="90b3c-117">Indica éxito.</span><span class="sxs-lookup"><span data-stu-id="90b3c-117">Indicates success.</span></span>  <br/> |
|<span data-ttu-id="90b3c-118">Advertencia</span><span class="sxs-lookup"><span data-stu-id="90b3c-118">Warning</span></span>  <br/> |<span data-ttu-id="90b3c-119">Indica una advertencia.</span><span class="sxs-lookup"><span data-stu-id="90b3c-119">Indicates a warning.</span></span>  <br/> |
|<span data-ttu-id="90b3c-120">Error</span><span class="sxs-lookup"><span data-stu-id="90b3c-120">Error</span></span>  <br/> |<span data-ttu-id="90b3c-121">Indica un error.</span><span class="sxs-lookup"><span data-stu-id="90b3c-121">Indicates an error.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="90b3c-122">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="90b3c-122">Child elements</span></span>

|<span data-ttu-id="90b3c-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="90b3c-123">**Element**</span></span>|<span data-ttu-id="90b3c-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90b3c-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90b3c-125">Símbolo (token) (ClientAccessTokenType)</span><span class="sxs-lookup"><span data-stu-id="90b3c-125">Token (ClientAccessTokenType)</span></span>](token-clientaccesstokentype.md) <br/> |<span data-ttu-id="90b3c-126">Especifica un token de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="90b3c-126">Specifies a client access token.</span></span>  <br/> |
|[<span data-ttu-id="90b3c-127">DescriptiveLinkKey</span><span class="sxs-lookup"><span data-stu-id="90b3c-127">DescriptiveLinkKey</span></span>](descriptivelinkkey.md) <br/> |<span data-ttu-id="90b3c-128">Actualmente no utilizado y reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="90b3c-128">Currently unused and reserved for future use.</span></span>  <br/> |
|[<span data-ttu-id="90b3c-129">MessageText</span><span class="sxs-lookup"><span data-stu-id="90b3c-129">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="90b3c-130">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90b3c-130">Provides a text description of the status of the response.</span></span>  <br/> |
|[<span data-ttu-id="90b3c-131">MessageXml</span><span class="sxs-lookup"><span data-stu-id="90b3c-131">MessageXml</span></span>](messagexml.md) <br/> |<span data-ttu-id="90b3c-132">Proporciona información de la respuesta de error adicionales.</span><span class="sxs-lookup"><span data-stu-id="90b3c-132">Provides additional error response information.</span></span>  <br/> |
|[<span data-ttu-id="90b3c-133">ResponseCode</span><span class="sxs-lookup"><span data-stu-id="90b3c-133">ResponseCode</span></span>](responsecode.md) <br/> |<span data-ttu-id="90b3c-134">Proporciona información de estado acerca de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90b3c-134">Provides status information about the request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="90b3c-135">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="90b3c-135">Parent elements</span></span>

|<span data-ttu-id="90b3c-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="90b3c-136">**Element**</span></span>|<span data-ttu-id="90b3c-137">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="90b3c-137">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="90b3c-138">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="90b3c-138">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="90b3c-139">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange (EWS).</span><span class="sxs-lookup"><span data-stu-id="90b3c-139">Contains the response messages for an Exchange Web Services (EWS) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90b3c-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="90b3c-140">Remarks</span></span>

<span data-ttu-id="90b3c-141">Este elemento se introdujo en Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="90b3c-141">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="90b3c-142">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="90b3c-142">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="90b3c-143">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="90b3c-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90b3c-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="90b3c-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="90b3c-145">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="90b3c-145">Schema Name</span></span>  <br/> |<span data-ttu-id="90b3c-146">Esquema de mensaje</span><span class="sxs-lookup"><span data-stu-id="90b3c-146">Message schema</span></span>  <br/> |
|<span data-ttu-id="90b3c-147">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="90b3c-147">Validation File</span></span>  <br/> |<span data-ttu-id="90b3c-148">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="90b3c-148">messages.xsd</span></span>  <br/> |
|<span data-ttu-id="90b3c-149">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="90b3c-149">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="90b3c-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="90b3c-150">See also</span></span>



- [<span data-ttu-id="90b3c-151">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="90b3c-151">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

