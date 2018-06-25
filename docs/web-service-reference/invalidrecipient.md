---
title: InvalidRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: El elemento InvalidRecipient contiene la dirección SMTP del destinatario no válido y la información acerca de por qué el destinatario no es válido.
ms.openlocfilehash: 800056666e486e9337dcd1c2786f7e6db1e060bb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2018
ms.locfileid: "19835961"
---
# <a name="invalidrecipient"></a><span data-ttu-id="b02cc-103">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="b02cc-103">InvalidRecipient</span></span>

<span data-ttu-id="b02cc-104">El elemento **InvalidRecipient** contiene la dirección SMTP del destinatario no válido y la información acerca de por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="b02cc-104">The **InvalidRecipient** element contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span> 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 <span data-ttu-id="b02cc-105">**InvalidRecipientType**</span><span class="sxs-lookup"><span data-stu-id="b02cc-105">**InvalidRecipientType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b02cc-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="b02cc-106">Attributes and elements</span></span>

<span data-ttu-id="b02cc-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="b02cc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b02cc-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="b02cc-108">Attributes</span></span>

<span data-ttu-id="b02cc-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="b02cc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b02cc-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="b02cc-110">Child elements</span></span>

|<span data-ttu-id="b02cc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b02cc-111">**Element**</span></span>|<span data-ttu-id="b02cc-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b02cc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b02cc-113">SmtpAddress</span><span class="sxs-lookup"><span data-stu-id="b02cc-113">SmtpAddress</span></span>](smtpaddress.md) <br/> |<span data-ttu-id="b02cc-114">Contiene la dirección SMTP del destinatario no válido.</span><span class="sxs-lookup"><span data-stu-id="b02cc-114">Contains the SMTP address of the invalid recipient.</span></span> <span data-ttu-id="b02cc-115">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="b02cc-115">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="b02cc-116">ResponseCode (InvalidRecipientResponseCodeType)</span><span class="sxs-lookup"><span data-stu-id="b02cc-116">ResponseCode (InvalidRecipientResponseCodeType)</span></span>](responsecode-invalidrecipientresponsecodetype.md) <br/> |<span data-ttu-id="b02cc-117">Proporciona un código de error que identifica el error específico que ha encontrado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b02cc-117">Provides an error code that identifies the specific error that the request encountered.</span></span> <span data-ttu-id="b02cc-118">Se requiere este elemento.</span><span class="sxs-lookup"><span data-stu-id="b02cc-118">This element is required.</span></span>  <br/> |
|[<span data-ttu-id="b02cc-119">MessageText</span><span class="sxs-lookup"><span data-stu-id="b02cc-119">MessageText</span></span>](messagetext.md) <br/> |<span data-ttu-id="b02cc-120">Proporciona una descripción de texto del estado de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b02cc-120">Provides a text description of the status of the response.</span></span> <span data-ttu-id="b02cc-121">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="b02cc-121">This element is optional.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b02cc-122">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="b02cc-122">Parent elements</span></span>

|<span data-ttu-id="b02cc-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="b02cc-123">**Element**</span></span>|<span data-ttu-id="b02cc-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b02cc-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b02cc-125">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="b02cc-125">InvalidRecipients</span></span>](invalidrecipients.md) <br/> |<span data-ttu-id="b02cc-126">Representa a los destinatarios de una solicitud de uso compartido de carpeta que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="b02cc-126">Represents the recipients of a folder sharing request that are invalid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b02cc-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b02cc-127">Remarks</span></span>

<span data-ttu-id="b02cc-128">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="b02cc-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b02cc-129">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="b02cc-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b02cc-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b02cc-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b02cc-131">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="b02cc-131">Schema Name</span></span>  <br/> |<span data-ttu-id="b02cc-132">Esquema de tipos</span><span class="sxs-lookup"><span data-stu-id="b02cc-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="b02cc-133">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="b02cc-133">Validation File</span></span>  <br/> |<span data-ttu-id="b02cc-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b02cc-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b02cc-135">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="b02cc-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="b02cc-136">False</span><span class="sxs-lookup"><span data-stu-id="b02cc-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b02cc-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="b02cc-137">See also</span></span>



[<span data-ttu-id="b02cc-138">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="b02cc-138">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="b02cc-139">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="b02cc-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

