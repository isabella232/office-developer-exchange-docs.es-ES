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
description: El elemento InvalidRecipients representa a los destinatarios de una solicitud de uso compartido de carpeta que no son válidos.
ms.openlocfilehash: 02ad8935bde347c563875bf5bfb31968b70d81b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19835966"
---
# <a name="invalidrecipients"></a><span data-ttu-id="c0722-103">InvalidRecipients</span><span class="sxs-lookup"><span data-stu-id="c0722-103">InvalidRecipients</span></span>

<span data-ttu-id="c0722-104">El elemento **InvalidRecipients** representa a los destinatarios de una solicitud de uso compartido de carpeta que no son válidos.</span><span class="sxs-lookup"><span data-stu-id="c0722-104">The **InvalidRecipients** element represents the recipients of a folder sharing request that are invalid.</span></span> 
  
```XML
<InvalidRecipients>
   <InvalidRecipient/>
</InvalidRecipients>
```

 <span data-ttu-id="c0722-105">**ArrayOfInvalidRecipientsType**</span><span class="sxs-lookup"><span data-stu-id="c0722-105">**ArrayOfInvalidRecipientsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c0722-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="c0722-106">Attributes and elements</span></span>

<span data-ttu-id="c0722-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="c0722-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c0722-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="c0722-108">Attributes</span></span>

<span data-ttu-id="c0722-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="c0722-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c0722-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="c0722-110">Child elements</span></span>

|<span data-ttu-id="c0722-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0722-111">**Element**</span></span>|<span data-ttu-id="c0722-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0722-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0722-113">InvalidRecipient</span><span class="sxs-lookup"><span data-stu-id="c0722-113">InvalidRecipient</span></span>](invalidrecipient.md) <br/> |<span data-ttu-id="c0722-114">Contiene la dirección SMTP del destinatario no válido y la información acerca de por qué el destinatario no es válido.</span><span class="sxs-lookup"><span data-stu-id="c0722-114">Contains the SMTP address of the invalid recipient and information about why the recipient is invalid.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c0722-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="c0722-115">Parent elements</span></span>

|<span data-ttu-id="c0722-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c0722-116">**Element**</span></span>|<span data-ttu-id="c0722-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0722-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c0722-118">GetSharingMetadataResponse</span><span class="sxs-lookup"><span data-stu-id="c0722-118">GetSharingMetadataResponse</span></span>](getsharingmetadataresponse.md) <br/> |<span data-ttu-id="c0722-119">Define una respuesta a una solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c0722-119">Defines a response to a [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="c0722-120">GetSharingMetadataResponseMessage</span><span class="sxs-lookup"><span data-stu-id="c0722-120">GetSharingMetadataResponseMessage</span></span>](getsharingmetadataresponsemessage.md) <br/> |<span data-ttu-id="c0722-121">Contiene el estado y el resultado de una única solicitud de [operación GetSharingMetadata](getsharingmetadata-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="c0722-121">Contains the status and result of a single [GetSharingMetadata operation](getsharingmetadata-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0722-122">Notas</span><span class="sxs-lookup"><span data-stu-id="c0722-122">Remarks</span></span>

<span data-ttu-id="c0722-123">El esquema que describe este elemento se encuentra en el directorio virtual IIS que hospeda los servicios Web Exchange.</span><span class="sxs-lookup"><span data-stu-id="c0722-123">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c0722-124">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="c0722-124">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c0722-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0722-125">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="c0722-126">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="c0722-126">Schema Name</span></span>  <br/> |<span data-ttu-id="c0722-127">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="c0722-127">Messages schema</span></span>  <br/> |
|<span data-ttu-id="c0722-128">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="c0722-128">Validation File</span></span>  <br/> |<span data-ttu-id="c0722-129">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="c0722-129">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="c0722-130">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="c0722-130">Can be Empty</span></span>  <br/> |<span data-ttu-id="c0722-131">False</span><span class="sxs-lookup"><span data-stu-id="c0722-131">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c0722-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="c0722-132">See also</span></span>



[<span data-ttu-id="c0722-133">Operación GetSharingMetadata</span><span class="sxs-lookup"><span data-stu-id="c0722-133">GetSharingMetadata operation</span></span>](getsharingmetadata-operation.md)


- [<span data-ttu-id="c0722-134">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="c0722-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

