---
title: CreateAttachmentResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateAttachmentResponse
api_type:
- schema
ms.assetid: cf6bd8bb-5317-4a03-bd75-297dd359b5da
description: El elemento CreateAttachmentResponse define una respuesta a una solicitud de CreateAttachment.
ms.openlocfilehash: dfc86516c5737296bc32330583fa63c36e9e63a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19763914"
---
# <a name="createattachmentresponse"></a><span data-ttu-id="9bbbe-103">CreateAttachmentResponse</span><span class="sxs-lookup"><span data-stu-id="9bbbe-103">CreateAttachmentResponse</span></span>

<span data-ttu-id="9bbbe-104">El elemento **CreateAttachmentResponse** define una respuesta a una solicitud de CreateAttachment.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-104">The **CreateAttachmentResponse** element defines a response to a CreateAttachment request.</span></span> 
  
```xml
<CreateAttachmentResponse>
   <ResponseMessages/>
</CreateAttachmentResponse>
```

 <span data-ttu-id="9bbbe-105">**CreateAttachmentResponseType**</span><span class="sxs-lookup"><span data-stu-id="9bbbe-105">**CreateAttachmentResponseType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9bbbe-106">Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="9bbbe-106">Attributes and elements</span></span>

<span data-ttu-id="9bbbe-107">Las secciones siguientes describen los atributos, elementos secundarios y elementos primarios.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9bbbe-108">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bbbe-108">Attributes</span></span>

<span data-ttu-id="9bbbe-109">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9bbbe-110">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="9bbbe-110">Child elements</span></span>

|<span data-ttu-id="9bbbe-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9bbbe-111">**Element**</span></span>|<span data-ttu-id="9bbbe-112">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="9bbbe-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9bbbe-113">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="9bbbe-113">ResponseMessages</span></span>](responsemessages.md) <br/> |<span data-ttu-id="9bbbe-114">Contiene los mensajes de respuesta para una solicitud de servicios Web de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-114">Contains the response messages for an Exchange Web Services request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9bbbe-115">Elementos principales</span><span class="sxs-lookup"><span data-stu-id="9bbbe-115">Parent elements</span></span>

<span data-ttu-id="9bbbe-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9bbbe-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9bbbe-117">Remarks</span></span>

<span data-ttu-id="9bbbe-118">El esquema que describe este elemento se encuentra en el directorio virtual de EWS del equipo que está ejecutando MicrosoftExchange Server 2007 que tenga instalado el rol de servidor de acceso de cliente.</span><span class="sxs-lookup"><span data-stu-id="9bbbe-118">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9bbbe-119">Información del elemento</span><span class="sxs-lookup"><span data-stu-id="9bbbe-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9bbbe-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9bbbe-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="9bbbe-121">Nombre de esquema</span><span class="sxs-lookup"><span data-stu-id="9bbbe-121">Schema name</span></span>  <br/> |<span data-ttu-id="9bbbe-122">Esquema de mensajes</span><span class="sxs-lookup"><span data-stu-id="9bbbe-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="9bbbe-123">Archivo de validación</span><span class="sxs-lookup"><span data-stu-id="9bbbe-123">Validation file</span></span>  <br/> |<span data-ttu-id="9bbbe-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="9bbbe-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="9bbbe-125">Puede estar vacío</span><span class="sxs-lookup"><span data-stu-id="9bbbe-125">Can be empty</span></span>  <br/> |<span data-ttu-id="9bbbe-126">False</span><span class="sxs-lookup"><span data-stu-id="9bbbe-126">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9bbbe-127">Ver también</span><span class="sxs-lookup"><span data-stu-id="9bbbe-127">See also</span></span>



[<span data-ttu-id="9bbbe-128">Operación CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="9bbbe-128">CreateAttachment operation</span></span>](createattachment-operation.md)
  
[<span data-ttu-id="9bbbe-129">CreateAttachment</span><span class="sxs-lookup"><span data-stu-id="9bbbe-129">CreateAttachment</span></span>](createattachment.md)


- [<span data-ttu-id="9bbbe-130">Elementos XML de EWS de Exchange</span><span class="sxs-lookup"><span data-stu-id="9bbbe-130">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

