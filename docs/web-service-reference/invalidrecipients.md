---
title: InvalidRecipients
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipients
api_type:
- schema
ms.assetid: e4e7b50e-2fa9-4649-94a6-6002f341ecc4
description: El elemento InvalidRecipients representa los destinatarios de una solicitud de uso compartido de carpetas que no son válidos.
ms.openlocfilehash: 99e0817f0ff873c4732b03cc7d68aa8e0070813c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465565"
---
# <a name="invalidrecipients"></a><span data-ttu-id="c9e20-103">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="c9e20-103">InvalidRecipients</span></span>

<span data-ttu-id="c9e20-104">El elemento **InvalidRecipients** representa los destinatarios de una solicitud de uso compartido de carpetas que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="c9e20-104">The **InvalidRecipients** element represents the recipients of a folder sharing request that are invalid.</span></span> 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 <span data-ttu-id="c9e20-105">**ArrayOfInvalidRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="c9e20-105">**ArrayOfInvalidRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9e20-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c9e20-106">Attributes and elements</span></span>

<span data-ttu-id="c9e20-107">En las siguientes secciones se describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c9e20-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9e20-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c9e20-108">Attributes</span></span>

<span data-ttu-id="c9e20-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="c9e20-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9e20-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c9e20-110">Child elements</span></span>

|<span data-ttu-id="c9e20-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9e20-111">**Element**</span></span>|<span data-ttu-id="c9e20-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9e20-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9e20-113">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="c9e20-113">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="c9e20-114">Contiene la dirección SMTP del destinatario no válido e información sobre por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="c9e20-114">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9e20-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c9e20-115">Parent elements</span></span>

|<span data-ttu-id="c9e20-116">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="c9e20-116">**Element**</span></span>|<span data-ttu-id="c9e20-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c9e20-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9e20-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="c9e20-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="c9e20-119">Define una respuesta a una solicitud de [operación de GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e20-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c9e20-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c9e20-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="c9e20-121">Contiene el estado y el resultado de una sola solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c9e20-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9e20-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c9e20-122">Remarks</span></span>

<span data-ttu-id="c9e20-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c9e20-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9e20-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c9e20-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9e20-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9e20-125">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c9e20-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c9e20-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c9e20-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c9e20-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c9e20-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c9e20-128">Validation File</span></span>  <br/> |<span data-ttu-id="c9e20-129">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="c9e20-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c9e20-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c9e20-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c9e20-131">Falso</span><span class="sxs-lookup"><span data-stu-id="c9e20-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9e20-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="c9e20-132">See also</span></span>



[<span data-ttu-id="c9e20-133">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="c9e20-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="c9e20-134">Elementos XML de EWS en Exchange</span><span class="sxs-lookup"><span data-stu-id="c9e20-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

